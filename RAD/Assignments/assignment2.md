Consider an occupancy problem in which $n$ balls are independently and uniformly distributed in $n$ bins. Show that, for large $n$, the expected number of empty bins approaches $n / e$, where $e$ is the base of the natural logarithm. 

What is the expected number of empty bins when $m$ balls are thrown into $n$ bins? (See Theorem 4.18.)



**Theorem 4.18**: Let $r=m / n$, and $Z$ be the number of empty bins when $m$ balls are thrown randomly into $n$ bins. Then,
$$
\mu=\mathbf{E}[Z]=n\left(1-\frac{1}{n}\right)^m \sim n e^{-r}
$$
and for $\lambda>0$,
$$
\operatorname{Pr}[|Z-\mu| \geq \lambda] \leq 2 \exp \left(-\frac{\lambda^2(n-1 / 2)}{n^2-\mu^2}\right)
$$
