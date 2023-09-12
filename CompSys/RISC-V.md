RISC-V is an *instruction set architecture*, see [[2023.09.04#Under the covers]]
# Lectures
![[2023.09.06#Reading notes]]

# Cheat sheets
![[Pasted image 20230906124732.png]]
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



