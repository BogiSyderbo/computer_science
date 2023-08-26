# Cartesian product
The (Cartesian) product of sets $A_{1}, \ldots, A_{n}$ is

$$
A_{1} \times A_{2} \times \cdots \times A_{n}=\left\{\left(a_{1}, \ldots, a_{n}\right) \mid a_{i} \in A_{i}\right\}
$$

Given $n$ finite sets $A_{1}, \ldots, A_{n}$, we have
$$
\left|A_{1} \times A_{2} \times \cdots \times A_{n}\right|=\left|A_{1}\right|\left|A_{2}\right| \cdots\left|A_{n}\right|
$$

# Relations
A *relation* $R$ on set $A$ is a collection of ordered pairs ($a$, $\left.a^{\prime}\right) \in A \times A$. 

**Example:**

$$A=\{2,3,4,5,6,15\}$$
The divisibility relation $R$ of $A$ is:
$$\quad a R b \Leftrightarrow a \mid b$$$$ R = \{(2,2),(2,4),(2,6),(3,3),(3,6),(3,15), (4,4),(5,5),(6,6)(5,15),(15,15)\}$$
That is, $R$ contains every pair where $a\mid b$ is true.

# Transitive and reflexive relations
- **Transitive** if relation $R$ on a set $A$ whenever $(a, b) \in R$ and $(b, c) \in R$, we also have that $(a, c) \in R$
- **Reflexive** if relation $R$ on a set $A$ is $(a, a) \in R$ $\forall$ $a \in A$. We say that $R$ is **irreflexive**, if $(a, a) \notin R$ $\forall$ $a \in A$.
# Symmetric relations
- **symmetric** if $(a, b) \in R$ implies that $(b, a) \in R$
- **asymmetric** if $(a, b) \in R$ implies that $(b, a) \notin R$
- **antisymmetric** if $(a, b) \in R$ and $(b, a) \in R$ then $a=b$.

# Equivalence relation
A relation is an equivalence relation if it is **symmetric**, **transitive**, and **reflexive**.
# Partially ordered sets
A relation $R$ on a set $A$ is called a partial order if $R$ is *reflexive*, *antisymmetric*, and *transitive*.

The set $A$ together with the partial order $R$ is called a a partially ordered set or*poset*, and we will denote this *poset* by $(A, R)$.

The **power set** of a set $S$ is given by $P(S)= \{T:T \subseteq S\}$. Set inclusion, $\subseteq$, is a partial order on $P(S)$, such that ($P(S)$, $\subseteq$). This is because $T \subseteq T~\forall~T \in P(S)$.

**Example:**
Let $\mathbb{Z}^{+}$be the set of positive integers. The usual relation $\leq$ (less than or equal to) is a partial order on $\mathbb{Z}^{+}$, as is $\geq$ (greater than or equal to).

We say that something is a **total linear order** if any two elements of a set $A$ are comparable.
- Posets $(\mathbb{Z}, \leqslant)$ and $(\mathbb{R}, \leqslant)$ are totally ordered.
- Poset $\left(\mathbb{Z}^{+}, \mid\right)$is not totally ordered ($5 \nmid 3$ and $\left.3 \nmid 5\right)$.
- ($P(S)$, $\subseteq$) is not totally ordered

## Maximal and minimal elements
Let $(A, \leqslant)$ be a poset. We say that $z \in A$ is
- a maximal element of $A$ if we cannot find $a \in A$ such that $z<a$
- a minimal element of $A$ if we cannot find $a \in A$ such that $a<z$.

Any finite, nonempty poset $A$ has a maximal and a minimal element.

The minimal element of ($P(S)$, $\subseteq$) is the empty set, the maximal element is the entire set. 
## Greatest and least elements
Let $(A, \leqslant)$ be a poset. We say that $z \in A$ is
- the greatest element of $A$ if $a \leqslant z$ for all $a \in A$.
- the least element of $A$ if $z \leqslant a$ for all $a \in A$.

**Note**: The greatest element of $A$ is always maximal, but the converse doesn't hold.

## Upper and lower bounds
Let $(A, \leqslant)$ be a poset and $B \subseteq A$. We say that $a \in A$ is
- an **upper bound** for $B$ if $b \leqslant a$ for all $b \in B$.
- a **lower bound** for $B$ if $a \leqslant b$ for all $b \in B$.
- the **least upper bound** (**LUB**) for $B$ if $a$ is an upper bound on $B$ and $a \leqslant a^{\prime}$ for any upper bound $a^{\prime}$ of $B$.
- the **greatest lower bound** (**GLB**) for $B$ if $a$ is an lower bound on $B$ and $a^{\prime} \leqslant a$ for any lower bound $a^{\prime}$ of $B$.