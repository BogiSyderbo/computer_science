A _set_ is any well-defined collection of objects called _elements of the set_.

The set of of all positive integers that are less than 5 can be written as:
$${\{1, 2, 3, 4}\}$$
The order of the elements in the set is unimportant. Elements may also be repeated. The above set can also be written as:
$$\{4, 2, 1, 3, 1\}$$
We indicate the fact that $x$ is an element of the set $A$ by writing $x \in A$, and we indicate the fact that $x$ is not an element of $A$ by writing $x \notin A$.

Let $A=\{1,3,5,7\}$. Then $1 \in A$, $3 \in A$, but $2 \notin A$.

The set defined by $\mathrm{P}(x)$, written $\{x \mid \mathrm{P}(x)\}$, is just the collection of all objects for which $\mathrm{P}$ is sensible and true. $\{x \mid \mathrm{P}(x)\}$ is read, "*the set of all $x$ such that $\mathrm{P}(x)$.*" For example:

$\{x \mid x ~ \text {is a positive integer less than } 4\}$ is the set $\{1,2,3\}$,

A set $A$ is called finite if it has $n$ distinct elements, where $n \in \mathbb{N}$. In this case, $n$ is called the *cardinality* of $A$ and is denoted by $|A|$.
# Important sets
**The empty set**:$$\emptyset = \{~\}$$This set contains nothing.

**The universal set**:
$$\mathbb{U}$$
This set contains the set of all possible values.
$$A\oplus\mathbb{U}$$
![[Pasted image 20230822210112.png]]
**The set of all natural numbers**:
$$\mathbb{N}=\{1, 2, 3, ...\}$$
This set contains all whole numbers from 1 and larger.
$$\mathbb{N}_0=\{0, 1, 2, 3, ...\}$$
This set contains all whole numbers and 0.

**The sets of integers**:
This set contains all integers.
$$\mathbb{Z}=\{...,-3, -2, -1, 0, 1, 2, 3,...\}$$
This set contains all positive integers.
$$\mathbb{Z}⁺=\{1, 2, 3,...\}$$
This set contains all negative integers.
$$\mathbb{Z}⁻=\{-1, -2, -3,...\}$$
**The set of rational numbers**:
$$\mathbb{Q}=\{x \mid x\text{ is a rational number } \}$$

Thus $\mathbb{Q}$ consists of numbers that can be written as $\frac{a}{b}$, where $a$ and $b$ are integers and $b$ is not 0 .

**The set of  real numbers**:
$$
\mathbb{R}=\{x \mid x \text { is a real number }\} .
$$
# Subsets
If every element of $A$ is also an element of $B$, that is, if whenever $x \in A$ then $x \in B$, we say that $A$ is a *subset* of $B$ or that $A$ is contained in $B$, and we write:
$$A \subseteq B$$If $A$ is not a subset of $B$, we write: 
$$A \nsubseteq B$$
![[Pasted image 20230822205742.png]]
If $A$ is any set, then $A \subseteq A$.  That is, every set is a subset of itself. 

Let $A$ be a set and let $B=\{A,\{A\}\}$. Then, since $A$ and $\{A\}$ are elements of $B$, we have $A \in B$ and $\{A\} \in B$. It follows that $\{A\} \subseteq B$ and $\{\{A\}\} \subseteq B$. However, it is not true that $A \subseteq B$.
# Operations on sets


# Properties of sets
**Commutative Properties**
1. $A \cup B=B \cup A$
2. $A \cap B=B \cap A$
**Associative Properties**
3. $A \cup(B \cup C)=(A \cup B) \cup C$
4. $A \cap(B \cap C)=(A \cap B) \cap C$
**Distributive Properties**
5. $A \cap(B \cup C)=(A \cap B) \cup(A \cap C)$
6. $A \cup(B \cap C)=(A \cup B) \cap(A \cup C)$
**Idempotent Properties**
7. $A \cup A=A$
8. $A \cap A=A$
**Properties of the Complement**
9. $(\overline{\bar{A}})=A$
10. $A \cup \bar{A}=U$
11. $A \cap \bar{A}=\varnothing$
12. $\bar{\varnothing}=U$
13. $\bar{U}=\{\}$
14. $\overline{A \cup B}=\bar{A} \cap \bar{B}$
15. $\overline{A \cap B}=\bar{A} \cup \bar{B} \quad$
**Properties of a Universal Set**
16. $A \cup U=U$
17. $A \cap U=A$
**Properties of the Empty Set**
18. $A \cup \varnothing=A$ or $A \cup\{\}=A$
19. $A \cap \varnothing=\varnothing$ or $A \cap\{\}=\{\}$
