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
## Complex numbers and real numbers
$$
i^{-1}=-i
$$
$$
\frac{1}{i}=-i
$$
$$
\frac{i}{1}=i
$$

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
The *arguments* of a complex number are defined as 
$$
\begin{gathered}
z=a+ib
\\
arg(z)=\tan^{-1}(\frac{a}{b})
\end{gathered}
$$
![[Pasted image 20230906214636.png]]
We can multiply to complex number by multiplying the *modulus* of both and adding the *arguments.*

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
# Complex polynomials
Let $z\in\mathbb{C}$ , and let $n\in \mathbb{N}$ . 
$w\in\mathbb{C}$ is an $n$-th root to $z$ such that
$$
w^n=z .
$$
If $n=2$ then $w$ is a *quadratic root*, and if $n=3$, $w$ is a *cubic root*.



Let $z=r e^{i \theta}\in\mathbb{C}, z\neq 0$ , and $n\in \mathbb{N}$ . $z$ has exactly $n~n$-th roots $w_0, w_1, w_2, \ldots, w_{n-1}$ given with
$$
w_k=r^{1 / n} e^{i(\theta+2 k \pi) / n}=r^{1 / n}\left(\cos \frac{\theta+2 k \pi}{n}+i \sin \frac{\theta+2 k \pi}{n}\right) .
$$

How to find the quadratic roots of a complex number
$$
z^2=w
$$
$$
z^2=(-1)^k\sqrt{|w|}e^{i\frac{\phi}{2}}
$$

For complex numbers:
$$
a,b,c\in\mathbb{C}
$$
That make up the polynomial:
$$
P(z)=az^2+bz+c
$$
The roots $\rho$ are given with:
$$
\rho_{\pm}=\frac{-b\pm\sqrt{b^2-4ac}}{2a}
$$
and
$$
P(z)=a(z-\rho_+)(z-\rho_-)
$$

## **d'Alembert–Gauss theorem**
Let
$$
P(z)=c_n z^n+c_{n-1} z^{n-1}+c_{n-2} z^{n-2}+\ldots c_1 z+c_0
$$
be a complex $n$-th root polynomial. Then there exists $\rho_1,\rho_2,\cdots,\rho_n$
$$
P(z)=c_n\left(z-\rho_1\right)\left(z-\rho_2\right) \ldots\left(z-\rho_n\right)
$$
