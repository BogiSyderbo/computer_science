There exists no real number $x$ such that $x^2=-1$.

This is where we introduce *complex* numbers.

The imaginary number $i$ is defined as:

$$i=\sqrt{-1}$$$$i^2=-1$$
Complex numbers are usually written in the form:
$$z=a+ib$$
where $z\in \mathbb{C}$ and $a,b \in \mathbb{R}$.

$a$ is called the *real* part of $z$:
$$
a=\operatorname{Re}(z) .
$$
$b$ is called the *imaginary part* part of $z$:
$$
b=\operatorname{I} m(z) .
$$
## Math rules for complex numbers
Let $z=a+i b$ and $w=c+i d$ be two complex numbers, then these rules apply:
-  $z+w=(a+c)+i(b+d)$
-  $z-w=(a-c)+i(b-d)$
-  $z \cdot w=(a c-b d)+i(a d+b c)$
- $\frac{z}{w}=\frac{a+i b}{c+i d}=\frac{a c+b d}{c^2+d^2}+i \frac{b c-a d}{c^2+d^2} \quad (w \neq 0)$
- $z^{-1}=\frac{a}{a^2+b^2}-i \frac{b}{a^2+b^2} \quad(z \neq 0)$
## Algebraic properties of complex numbers
- Commutativity: $z_1+z_2=z_2+z_1$ and $z_1 z_2=z_2 z_1$
- Associativity: $\left(z_1+z_2\right)+z_3=z_1+\left(z_2+z_3\right)$ and $\left(z_1 z_2\right) z_3=z_1\left(z_2 z_3\right)$
- Distributive: $z_1\left(z_2+z_3\right)=z_1 z_2+z_1 z_3$
- Zero and unit-elements: $z_1+0=z_1$ and $z_1 \cdot 1=z_1$
- Opposite values: $\forall z\exists-z: z+(-z)=0$
- Inverse numbers: $\forall z \neq 0\exists\mathrm{w}:z w=1$

# Conjugate
![[Pasted image 20230906213251.png]]
## Math rules for complex conjugate
If $z$ and $w$ are *complex numbers*, then it applies that:
- $\bar{z}+\bar{w}=\overline{z+w}$
- $\bar{z}-\bar{w}=\overline{z-w}$
- $\bar{z} \bar{w}=\overline{z w}$
- $\frac{\bar{z}}{\bar{w}}=\overline{\left(\frac{z}{w}\right)} \quad(w \neq 0)$


# Geometric representation of complex numbers
Complex numbers can be represented as *vectors* for simplicity.
![[2023.09.05#Geometric representation]]


## Polar form
We can also represent complex numbers in *polar form*.

In this representation, the vector is given with *polar coordinates* ($r,\theta$) which consists of a length $r$ and an angle $\theta$.
![[Pasted image 20230906213706.png]]


There is a simple connection between *Cartesian coordinates* ($a,b$) and *polar coordinates*:
$$a=r\cos \theta$$
$$b=r\sin\theta$$

If we think of the vector $(a,b)$ as the complex number $z=a+ib$, the *polar form* of $z$ is:
$$z=r\cos\theta+ir\sin\theta$$
If we want to convert from *Cartesian coordinates* to *polar coordinates* we can use following rules:
$$
r=\sqrt{a^2+b^2}, \quad \cos \theta=\frac{a}{r}, \quad \sin \theta=\frac{b}{r}
$$
$r$ is called the *modulus* for a complex number *z*:
$$
r=|z| .
$$
and we can also observe that:
$$
|z|=\sqrt{a^2+b^2} .
$$
$$
|z|^2=a^2+b^2=z \bar{z} .
$$

### Multiplication
![[Pasted image 20230906214636.png]]
We can multiply to complex number by multiplying the *modulus* of both and adding the arguments.

$$
\begin{gathered}
z=|z|(\cos\theta+i\sin\theta)
\\
w=|w|(\cos\phi+i\sin\phi)
\end{gathered}
$$
We can multiply these complex numbers:
$$
z\cdot w=|z||w|(\cos\theta+i\sin\theta)(\cos\phi+i\sin\phi) = |zw|(\cos(\theta+\phi)+\sin(\theta+\phi))
$$

### Triangle inequality for complex numbers
$$
|z+w| \leq|z|+|w| .
$$
![[Pasted image 20230906215327.png]]
# Complex exponentials
If $z=a+i b$ is a complex number, we define
$$
e^z=e^a(\cos b+i \sin b) .
$$
$e^z$ is a complex number with modulus $e^a$ and argument $b$.

$$\forall z,w \in \mathbb{C}, e^{z+w}=e^z\cdot e^w$$

# De Moivres formula
$$
\forall n\in\mathbb{N}, (\cos \theta+i \sin \theta)^n=\cos (n \theta)+i \sin (n \theta)
$$
**Proof**:
$$
(\cos \theta+i \sin \theta)^n=\left(e^{i \theta}\right)^n=e^{i n \theta}=\cos (n \theta)+i \sin (n \theta)
$$
