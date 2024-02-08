A a *proposition* or *statement* is a declarative sentence that is either *true* or *false*.

We use propositional variables to represent propositions. e.g. $q, p , r$.

We can combine propositions using logical operations.

# Logical operations:

- **Conjunction (AND/$\land$)**
	*True* if $p, q$ are both *true*
	
- **Disjunction (OR/$\lor$)**
	*True* if at least one of $p, q$ are *true*

- **Negation (NOT/$\neg$)**
	*True* if $p$ is *false*, *false* if $p$ is *true*

- **Exclusive or (XOR/$\oplus$)**
	*True* if exactly one of $p, q$ is true. Otherwise *false*

# Truth tables
A truth table gives the truth value, *true* or *false* (T/F) of a (compound) statement for all possible values of propositional variables.
$$
\begin{array}{|c|c|c|c|c|c|c|}
\hline
p & q & \neg p & \neg q & p \land q & p \lor q & p \oplus q \\ \hline
F & F & T & T & F & F & F \\ \hline
F & T & T & F & F & T & T \\ \hline
T & F & F & T & F & T & T \\ \hline
T & T & F & F & T & T & F \\ \hline
\end{array}
$$
# Implication
$$
\begin{array}{|c|c||c|}
\hline \mathrm{p} & \mathrm{q} & \mathrm{p} \Rightarrow \mathrm{q} \\
\hline \mathrm{F} & \mathrm{F} & \mathrm{T} \\
\mathrm{F} & \mathrm{T} & \mathrm{T} \\
\mathrm{T} & \mathrm{F} & \mathrm{F} \\
\mathrm{T} & \mathrm{T} & \mathrm{T} \\
\hline
\end{array}
$$
If $p$ implies $q$ ($p\Rightarrow q$) then $p$ is called the *hypothesis* and $q$ is called the *conclusion*.

# Contrapositive and converse
Consider implication $p \Rightarrow q$. 

Its *converse* is $q \Rightarrow p$ and its *contrapositive* is $(\neg p) \Rightarrow(\neg q)$.

- Lets find the truth table for the *contrapositive* of $p \Rightarrow q$
- The *contrapositive* statement is $(\neg q) \Rightarrow(\neg p)$

$$
\begin{array}{|c|c|c|c|c|c|}
\hline \mathrm{p} & \mathrm{q} & \neg \mathrm{q} & \neg \mathrm{p} & (\neg \mathrm{q}) \Rightarrow(\neg \mathrm{p}) & \mathrm{p} \Rightarrow \mathrm{q} \\
\hline \mathrm{F} & \mathrm{F} & \mathrm{T} & \mathrm{T} & \mathrm{T} & \mathrm{T} \\
\mathrm{F} & \mathrm{T} & \mathrm{F} & \mathrm{T} & \mathrm{T} & \mathrm{T} \\
\mathrm{T} & \mathrm{F} & \mathrm{T} & \mathrm{F} & \mathrm{F} & \mathrm{F} \\
\mathrm{T} & \mathrm{T} & \mathrm{F} & \mathrm{F} & \mathrm{T} & \mathrm{T} \\
\hline
\end{array}
$$

# Logical equivalence
$$
\begin{array}{|c|c||c|}
\hline \mathrm{p} & \mathrm{q} & \mathrm{p} \Leftrightarrow \mathrm{q} \\
\hline \mathrm{F} & \mathrm{F} & \mathrm{T} \\
\mathrm{F} & \mathrm{T} & \mathrm{F} \\
\mathrm{T} & \mathrm{F} & \mathrm{F} \\
\mathrm{T} & \mathrm{T} & \mathrm{T} \\
\hline
\end{array}
$$

If $p \Leftrightarrow q$ is a true statement, then we say that $p$ and $q$ are (logically) equivalent and write $p \equiv q$.

# Proposition operations
The operations for propositions have the following properties.
**Commutative Properties**
1. $p \vee q \equiv q \vee p$
2. $p \wedge q \equiv q \wedge p$
**Associative Properties**
3. $p \vee(q \vee r) \equiv(p \vee q) \vee r$
4. $p \wedge(q \wedge r) \equiv(p \wedge q) \wedge r$
**Distributive Properties**
5. $p \vee(q \wedge r) \equiv(p \vee q) \wedge(p \vee r)$
6. $p \wedge(q \vee r) \equiv(p \wedge q) \vee(p \wedge r)$
**Idempotent Properties**
7. $p \vee p \equiv p$
8. $p \wedge p \equiv p$
**Properties of Negation**
9. $\neg(\neg p) \equiv p$
10. $\neg(p \vee q) \equiv(\neg p) \wedge(\neg q)$
11. $\neg(p \wedge q) \equiv(\neg p) \vee(\neg q)$