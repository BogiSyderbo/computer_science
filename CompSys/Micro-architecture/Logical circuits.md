# Logic gates

Logical gates are the *primitives* that make up all of the functionality in a processor.

Examples of gates include:
- AND
- OR
- Inverter

**AND**
![[Pasted image 20240107145057.png]]



| A | B | A AND B |
| ---- | ---- | ---- |
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |
**OR**
![[Pasted image 20240107145112.png]]



| A | B | A OR B |
| ---- | ---- | ---- |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

**Inverter**
![[Pasted image 20240107145135.png]]


| A | NOT A |
| ---- | ---- |
| 0 | 1 |
| 1 | 0 |

## CMOS

*PMOS* conducts when the gate-source voltage is low compared to the source terminal. 

It turns off when the gate-source voltage is high compared to the source terminal.
![[Pasted image 20240107132243.png]]
*NMOS* conducts when the gate-source voltage is high compared to the source terminal.

It turns off (acts like an open switch) when the gate-source voltage is low or negative compared to the source terminal.
![[Pasted image 20240107132720.png]]
### Inverter (CMOS)
An *inverter* will output a *negation* of the data it receives. In other words, it will output no voltage if given voltage and vice versa.
![[Pasted image 20240107132901.png]]
When the input to the inverter is at logic level 1:

- The NMOS transistor, which conducts when the input is high, is turned on. It allows a path to ground, creating a low resistance between its source and drain terminals.

- Simultaneously, the PMOS transistor, which turns off when the input is high, is in an off state due to the high input. It prevents the connection between the power supply and the output.

When the input to an inverter circuit is at logic level 0:

- The NMOS transistor, which conducts when the input is high, is turned off because the input is low. This prevents the path to ground, creating a high resistance between its source and drain terminals.

- At the same time, the PMOS transistor, which turns on when the input is low, is activated due to the low input. It establishes a connection between the power supply and the output.

### Or-gate (CMOS)
![[Pasted image 20240107144609.png]]


# Digital logic
## Multiplexor (mux)
A *mux* is used for choosing between different results.
![[Pasted image 20240107145650.png]]
It is the closest thing to a *conditional statement* in hardware.

A two input *mux*:
![[Pasted image 20240107145430.png]]
The *mux* has two data inputs (*A* and *B*), which are labeled 0 and 1, and one selector input (*S*), as well as an output *C*.

Logic table:

| $S$ | $A$ | $B$ | $C$    |
| --- | --- | --- | --- |
| 0   | 0   | 0   | 0   |
| 0   | 0   | 1   | 0   |
| 0   | 1   | 0   | 1   |
| 0   | 1   | 1   | 1   |
| 1   | 0   | 0   | 0   |
| 1   | 0   | 1   | 1   |
| 1   | 1   | 0   | 0   |
| 1   | 1   | 1   | 1   |
Or, more simply:

| $S$ | $C$    |
| --- | --- |
| 0   | A   |
| 1   | B   |


A 1-bit *mux* can be arrayed 32 times to select between two different 32-bit inputs:
![[Pasted image 20240107145912.png]]

## Arithmetic Logic Unit (ALU)
An *ALU* is a circuit that performs basic arithmetic and bit-wise operations.

**Proto-ALU**, the 1-bit logical unit for *AND*, *OR*:
![[Pasted image 20240107151511.png]]

A 1-bit *ALU* that performs *AND*, *OR*. and addition (see [adder](#Adder)):
![[Pasted image 20240107155830.png]]
When adding two numbers, if the sum of the bits in a column exceeds the base of the number system, a carry is generated. CarryIn allows the ALU to take into account any carry from a previous bit addition or to input a carry, if needed, for multi-bit addition operations.

*CarryIn* is the carry signal fed into an *ALU* for addition, considering any carry from previous bit additions.

*CarryOut* is the carry signal produced by an *ALU* during addition, indicating if there's a carry beyond the most significant bit.


A 32-bit *ALU* constructed from 32 1-bit *ALUs* which allows for the addition of 32-bit numbers. **CarryOut** of the less significant bit is connected to the **CarryIn** of the more significant bit. This organization is called *ripple carry*:
![[Pasted image 20240107160037.png]]

A 1-bit *ALU* that performs *AND*, *OR*, and *addition* on $a$ and $b$ with a 
![[Pasted image 20240107160813.png]]
By selecting $b$ (Binvert = 1) and setting *CarryIn* to 1 in the least significant bit of the *ALU*, we get *two’s complement* subtraction of $b$ from a instead of addition of $b$ to $a$.

In this way we can achieve *subtraction* by negating and then adding.


### Adder
A **full-adder**, which is a 1-bit adder with 3 inputs and 2 outputs.
![[Pasted image 20240107155441.png]]
![[Pasted image 20240107155737.png]]
![[Pasted image 20240107155635.png]]