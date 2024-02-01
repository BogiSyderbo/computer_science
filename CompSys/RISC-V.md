RISC-V is an *instruction set architecture*, see [[2023.09.04#Under the covers]]
# Lectures
![[2023.09.06#Reading notes]]

# Cheat sheets
![[Pasted image 20230906124732.png]]
![[Pasted image 20240118161648.png]]
![[Pasted image 20230906124751.png]]
![[Pasted image 20230906125119.png]]
![[Pasted image 20230906124959.png]]
![[Pasted image 20230906124931.png]]

# C comparisons
**C:**
```C
B[g] = A[f+1] + A[f]
```
**RISC-V:**
Assume that the variables $f$, $g$, $h$, $i$, and $j$ are assigned  to registers $\texttt{x5}$, $\texttt{x6}$, $\texttt{x7}$, $\texttt{x28}$, and $\texttt{x29}$, respectively. Assume that the base address  of the arrays $A$ and $B$ are in registers $\texttt{x10}$ and $\texttt{x11}$, respectively:
```RISC-V
slli x30, x5, 3
add x30, x10, x30
slli x31, x6, 3
add x31, x11, x31

lw x5, 0(x30)
addi x12, x30, 8
lw x30, 0(x12)
add x30, x30, x5
lw x30, 0(x31)
```



## The stack
Let's go through the relevant instructions in the provided assembly code to understand how values are saved to the stack:

1. **Allocate Space on the Stack:**
```
addi sp, sp, -32    # Adjust the stack pointer to allocate space
```    

This instruction decreases the stack pointer (`sp`) by 32 bytes, effectively reserving space for local variables and other data.
    
2. **Save Return Address on the Stack:**
```
sw ra, 28(sp)    # Save return address on the stack
```

The return address is the address to which the program should return after the function call completes. It's stored in the register `ra` (return address), and this instruction saves it to the stack.
    
3. **Save Base Register (s0) on the Stack:**
```
sw s0, 24(sp)    # Save s0 (base register) on the stack
```

The base register (`s0`) is commonly used as a frame pointer to access local variables within the function. This instruction saves the base register to the stack.
    
4. **Set Base Register (s0) to Point to the Top of the Stack Frame:**
```
addi s0, sp, 32    # Set s0 to point to the top of the stack frame
```

    
The base register (`s0`) is set to point to the top of the current stack frame. This allows easy access to local variables and parameters within the function.    
5. **Save Argument (n) on the Stack:**
```
sw a0, -20(s0)    # Save the argument (n) on the stack
```

The argument `n` is passed to the function in register `a0`. This instruction saves the value of `n` to the stack.

```C
|  ...           |
|  Saved values  |
|  (local vars)  |
|  Saved s0      |
|  Saved ra      |  <- sp points here
|  Unused space  |
|  ...           |

```
![[Pasted image 20240115194709.png]]![[Pasted image 20240115194751.png]]
