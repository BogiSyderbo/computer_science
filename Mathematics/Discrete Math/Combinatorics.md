# General multiplication rule
![[SS/SSB3/Lectures/Week 1/2024.02.05#Combinatorics|2024.02.05]]

$n_{1}n_{2}...n_{k}=\prod_{i=1}^{k}n_{i}$

# Sequences, sets, multisets
**Sequences (string)** is an ordered collection of elements.
$(1,2,3,4,4,5)$

**Set** is an unordered collection of elements without repetitions
$\{4,1, 2, 6,3, 7,5\}$

**Multiset** an unordered collection of possibly repeating elements
$[2, 1, 2]$

$$
\begin{array}{l|c|c} 
& \text { with repetitions } & \text { without repetitions } \\
\hline \text { ordered } & 1 \text { (sequences) } & 2 \text { (sequences w/o repetitions) } \\
\hline \text { unordered } & 3 \text { (multisets) } & 4 \text { (sets) }
\end{array}
$$
 Any *set* with $n$ elements has $2^{n}$ different subsets.

In how many ways can we choose $r$ elements from an $n$-element set
$$
\begin{array}{l|c|c} 
& \text { with repetitions } & \text { without repetitions } \\
\hline \text { ordered } & n^r & { }_n P_r \\
\hline \text { unordered } & n+r-1 C_r & { }_n C_T
\end{array}
$$

## Sequences
Let $\mathbb{A}$ be an $n$-element set. The number of length-$r$ sequences that can be formed from elements of $\mathbb{A}$, allowing repetitions, is $n^{r}$

### Permutations

${ }_n P_r$ is called the number of permutations of $n$ objects taken $r$ at a time.
$$
{ }_n P_r=\frac{n !}{(n-r) !}
$$

Let $\mathbb{A}$ be an $n$-element set and let $1 \leq r \leq n$. The number of length-$r$ sequences that can be formed from elements of $\mathbb{A}$, without repetition, is ${n} P_{r}=n \cdot (n-1) ... (n-r+1)$

There are:
$$
{ }_n P_n=n \cdot(n-1) \cdot(n-2) \cdots 2 \cdot 1=n !
$$
different ways to permute the elements of $\mathbb{A}$.

## Sets

### Combinations without repeats
Any *set* with $n$ elements has
$$
{ }_n C_r=\frac{n !}{r !(n-r) !}
$$
subsets of size $r$, where $0 \leqslant r \leqslant n$.

${ }_n C_r$ is called the number of *combinations* of $n$ objects taken $r$ at a time

Many texts use symbol $\left(\begin{array}{l}n \\ r\end{array}\right)$ instead of ${ }_n C_r$.

### Combinations with repeats

# Pigenhole principle