$$S_3=\{\epsilon, \sigma, \sigma^2,\tau,\tau\sigma,\tau\sigma^2\}\text{, where } \sigma^3=\tau^2=\epsilon,\;\sigma\tau\sigma=\tau$$
$$C_3=\{1,c,c^2\}\text{, where }c^3=1$$
Define $\alpha(\sigma)=c^2$, $\alpha(\tau)=1$. Then $\alpha(\sigma^2)=\alpha(\sigma)\alpha(\sigma)=c^4=c$, so $\alpha$ as so defined is indeed onto. $\alpha(\sigma^3)$ gives $c^6=1$ as required, and $\alpha(\tau^2)$ gives $1^2$ as required. $\alpha(\sigma\tau\sigma)$ would give $c^4=c$, which is not what we want. However, we may use the fact that $\sigma\tau\sigma=\tau\iff \sigma\tau=\tau\sigma^{-1}$, and that $c^2$ inverts $c$:
- $\alpha(\sigma\tau)=c^2$
- $\alpha(\tau\sigma^{-1})=\alpha(tau)\alpha(\sigma^{-1})=1c^2=c^2$,
so indeed, $\alpha(\sigma\tau)=\alpha(\tau\sigma^{-1})$.

To compute the kernel, let's compute each output of $\alpha$ for each value in $S_3$:

| Input          | Output |
| -------------- | ------ |
| $\epsilon$     | $1$    |
| $\sigma$       | $c^2$  |
| $\sigma^{2}$   | $c$    |
| $\tau$         |        |
| $\tau\sigma$   |        |
| $\tau\sigma^2$ |        |
