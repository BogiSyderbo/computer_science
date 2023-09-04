A matrix is a rectangular array of numbers arranged in $m$ horizontal rows and $n$ vertical columns:
$$
\mathbf{A}=\left[\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1 n} \\
a_{21} & a_{22} & \cdots & a_{2 n} \\
\vdots & \vdots & & \vdots \\
a_{m 1} & a_{m 2} & \cdots & a_{m n}
\end{array}\right]
$$
The $i$th row of $\mathbf{A}$ is $\left[\begin{array}{llll}a_{i 1} & a_{i 2} & \cdots & a_{i n}\end{array}\right], 1 \leq i \leq m$, and the $j$ th column of $\mathbf{A}$ $\left[\begin{array}{c}a_{1 j} \\ a_{2 j} \\ \vdots \\ a_{m j}\end{array}\right], 1 \leq j \leq n$. We say that $\mathbf{A}$ is $\boldsymbol{m}$ by $\boldsymbol{n}$, written $m \times n$.

If $m=n$ (same number of rows and columns), we say $\mathbf{A}$ is a *square matrix* of order $n$ and that the numbers $a_{11}, a_{22}, \ldots, a_{n n}$ form the *main diagonal* of $\mathbf{A}$.

We refer to the number $a_{i j}$, which is in the $i$th row and $j$th column of $\mathbf{A}$ as the $i, j$th element of $\mathbf{A}$ or as the $(i, j)$ entry of $\mathbf{A}$, and we often write (1) as $\mathbf{A}=\left[a_{i j}\right]$.


# Basic properties of matrices
The following theorem gives some basic properties of matrix addition; the proofs are omitted:
$\mathbf{A}+\mathbf{B}=\mathbf{B}+\mathbf{A}$
$(\mathbf{A}+\mathbf{B})+\mathbf{C}=\mathbf{A}+(\mathbf{B}+\mathbf{C})$
$\mathbf{A}+\mathbf{0}=\mathbf{0}+\mathbf{A}=\mathbf{A}$

If $\mathbf{A}=\left[a_{i j}\right]$ is an $m \times p$ matrix and $\mathbf{B}=\left[b_{i j}\right]$ is a $p \times n$ matrix, then the product of $\mathbf{A}$ and $\mathbf{B}$, denoted $\mathbf{A B}$, is the $m \times n$ matrix $\mathbf{C}=\left[c_{i j}\right]$ defined by
$$
c_{i j}=a_{i 1} b_{1 j}+a_{i 2} b_{2 j}+\cdots+a_{i p} b_{p j} \quad 1 \leq i \leq m, 1 \leq j \leq n .
$$
![[Pasted image 20230828110420.png]]
