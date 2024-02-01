# Single cycle micro-architecture
![[Pasted image 20240107154439.png]]

The longest clock cycle is determined by the clock frequency. Every instruction is as slow as the slowest instruction.
# Pipelining
*Pipelining* is a method for arranging the execution of instructions like an assembly line.

The classic pipeline usually has five steps:
1. **Fe**: Fetching the instruction
2. **De**: Decoding the instruction
3. **Ex**: Execution (*ALU*)
4. **Me**: Reading from memory
5. **Wb**: Writing back to / updating the registers

We split our single-cycle datapath into several "steps", such that each step can contain one instruction.
![[Pasted image 20240107154830.png]]
Each step should take approximately the same amount of time. This is a *balanced pipeline*.

A simple 5-step pipeline:
![[Pasted image 20240108173324.png]]
Notice how there are *pipeline registers* before the *decoder*, *ALU*, *data cache*, and finally before writing to registers

Here is an example of an execution diagram for four instructions on a five-step pipeline with full-forwarding:
```
						0  1  2  3  4  5  6  7  8
lw   x11,0(x10)         Fe De Ex Me Wb
addi x11,x11,100           Fe De De Ex Me Wb
sw   x11,0(x14)               Fe Fe De Ex Me Wb
addi x10,x10,1                      Fe De Ex Me Wb
```

Instructions are to the left, one for each line, and the program is executed from top to bottom. The time is expressed on top as the amount of clock cycles. 

In a *simple pipeline* every execution has the same *flow* through the pipeline, where each instruction goes through the various stages of the pipeline in a fixed and predetermined sequence.

## Resource limitations

For a *simple pipeline*, each instruction has a resource limitation of 1, which means only one instruction can be run during one clock cycle.

```
                        0  1  2  3  4  5  6  7  8
lw   x11,0(x10)         Fe De Ex Me Wb
addi x11,x11,100           Fe De De Ex Me Wb
sw   x11,0(x14)               Fe Fe De Ex Me Wb
addi x10,x10,1                      Fe De Ex Me Wb
```

In the example above, the second instruction is *stalled* since it can't since it can't perform $\texttt{De}$ in cycle 2 and has to be repeated in cycle 3.

This causes the 3rd instruction to *stall* its $\texttt{Fe}$ since it can only be run once at a time/
## Hazards
*Hazards* occur when multiple instructions try to use the same hardware at once.

*Data hazards* occur when instructions that exhibit data dependence modify data in different stages of a pipeline. Ignoring potential data hazards can result in *race conditions* (also termed race hazards).

*Data hazards* can happen if:
1. read after write (RAW), a true dependency
- An instruction refers to a result that has not yet been calculated or retrieved. This can occur because even though an instruction is executed after a prior instruction, the prior instruction has been processed only partly through the pipeline.
2. write after read (WAR), an anti-dependency
- Because you have to ensure that an instruction does not change a value K before any previous instructions are done using the old value of K.
3. write after write (WAW), an output dependency
- Similar to WAR, but here the previous instruction also changes K.

## Out-of-order execution
**Out of order execution**:
A situation in pipelined execution when an instruction blocked from executing does not cause the following instructions to wait. The processor can execute the instructions in some order that preserves the data flow order of the program after analysing the data flow.


An out-of-order pipeline has these *in-order* steps:
1. **Fe**: Fetching the instruction
2. **De**: Decoding the instruction
3. **Fu**: Fusion
5. **Al**: Allocate
6. **Rn**: Rename
7. **Qu**: Queue
8. **Ca, Cb**: Commit RAT

Additionally, it can also have these *out-of-order* steps:
1. **pk**: Picking an instruction for execution
2. **rd**: Reading the operands from the register
3. **ex**: Execution of the operation in an ALU
4. **ag**: ?
5. **me**: Reading from memory(?)
6. **wr**: Writing the result to a register


The *in-order* steps for a instruction are in the order:
```
Fa Fb Fc De Fu Al Rn Qu ...out-of-order... Ca Cb
```

The *out-of-order* steps for a instruction are in the order:
```
pk,rd,ex,wr
```

The steps for a *load* instruction are:
```
Fa Fb Fc De Fu Al Rn Qu pk rd ag ma mb mc wb Ca Cb
```

The steps for a *store* instruction are:
```
Fa Fb Fc De Fu Al Rn Qu pk rd ag ma mb mc -- Ca Cb   // addresse
-                    Q* -- -- -- -- pk rd st C*      // data
```
De særlige trin "**Q***" og "**C***" bruges kun for data-delen af store instruktionerne. I typiske implementationer vil "**Q***" altid ske samtidigt med "**Qu**" for den operation der beregner af adressen, ligesom "**C***" vil ske samtidigt med "**Ca**"

**Random notes**:
- We stall out of order phases such that in order is in order
- Forwarding from store byte to loadbyte
- When we're using a value which is used in a load or store, we must wait until after ma to enter pk phase
- If two ALU operations consecutively try to use the same operand, stall out of order