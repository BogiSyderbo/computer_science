# Quadratic equations
Quadratic equations are equations for polynomials of 2nd degree.
![[Pasted image 20230902175821.png]]
![[2. Equations#Quadratic equations]]
![[2. Equations#Solving quadratic equations#General solution]]

# $n$-th degree polynomials
![[4. Functions#Function types#$n$-th degree polynomials]]
![[4. Functions#Factoring polynomials]]

# Polynomial division
*Polynomial division* is a method for dividing a polynomial by another polynomial.

Suppose $P(x)$ and $Q(x)$ are polynomials and that the degree of $Q(x)$ is at least one, then there are polynomials $K(x), R(x)$ where the degree of $R(x)$ is less than the degree of $Q(x)$, such that $$ P(x)=K(x) Q(x)+R(x) \quad \forall \quad x $$Note that if the degree of $P(x)$ is less than the degree of $Q(x)$, we can choose $K(x)=0$ and $R(x)=P(x)$.

In general we can find two polynomials $K(x)\operatorname{and} R(x)$, where $R(x)$ has a lower degree than $Q(x)$, so that $$ \frac{P(x)}{Q(x)}=K(x)+\frac{R(x)}{Q(x)} $$ Multiplying by $Q(x)$, we get $$ P(x)=K(x) Q(x)+R(x) $$
## Long polynomial division algorithm
### Example
1.5.1 in [TLO]