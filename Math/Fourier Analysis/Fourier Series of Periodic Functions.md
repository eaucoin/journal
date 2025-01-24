## Definition.

Let $u:\mathbb{R}^{n}\rightarrow \mathbb{R}$. Then the **Laplacian** of $u$ is written $\nabla^{2}u$ and defined as
$$\nabla^{2}u=\partial_{x_1}^{2}u+\partial_{x_2}^{2}u+\dots\partial_{x_n}^{2}u\text{.}$$ ^79a81f

## Definition. 
*Defining three Equations.*

Let:
- $\mathbb{R}_{t}$ be a time line,
- $\mathbb{R}_{s}$ be a space line,
- $u:\mathbb{R}_{t}\times\mathbb{R}_{s}^{3}\rightarrow \mathbb{R}$,
- $c$ be a real constant.
Then we have the following defined equations:
$$\begin{align*}

\text{1.}\textbf{ Wave: }&\partial_{t}^{2}u=c^2\nabla^2u\\\\
\text{2.}\textbf{ Heat: }&\partial_tu=k\nabla^{2}u\\\\
\text{3.}\textbf{ Laplace: }&\;\;\;0=\nabla^2u
\end{align*}$$

## Definition.
*Generalized form of the three equations.*

Let $F:\mathbb{R}_{t}\times\mathbb{R}_{s}^{3}\rightarrow \mathbb{R}$. Then a generalized form of the [[Fourier Series of Periodic Functions#^79a81f|three equations above]] take:
$$\begin{align*}

\text{1.}\textbf{ Wave: }&\partial_{t}^{2}u-c^2\nabla^2u=F(\textbf{x},\;t)\\\\
\text{2.}\textbf{ Heat: }&\;\partial_tu-k\nabla^{2}u=F(\textbf{x},\;t)\\\\
\text{3.}\textbf{ Laplace: }&\;\;\;\;\;\;\;\;\;\;\;\;\nabla^2u=F(\textbf{x},\;t)
\end{align*}$$
It can also be said that these are the *inhomogenous* forms for the [[Fourier Series of Periodic Functions#^79a81f|three equations above]]. 

# Definition.
*The Schrodinger Equation*.

Let:
- $\mathbb{R}_{t}$ be a time line,
- $\mathbb{R}_{s}$ be a space line,
- $u:\mathbb{R}_{t}\times\mathbb{R}_{s}^{3}\rightarrow \mathbb{R}$,
- $V:\mathbb{R}_{s}^{3}\rightarrow \mathbb{R}$,
- $m$ be a real parameter representing mass,
- $\hbar$ be Planck's constant.

Then the *Schrodinger Equation* is defined as 
$$i\hbar\;\partial_{t} u+\frac{\hbar^{2}}{2m}\nabla^{2}u=V(\textbf{x})u\text{.}$$

## Definition.
*The $D^{\alpha}$ operator.* ^50927c

Let:
- $(\alpha_1,\;\alpha_2,\dots,\;\alpha_n)\in\mathbb{N}^{n}$,
- $(x_1,\;x_2,\dots,\;x_n)\in\mathbb{R}^{n}$,
- $|\alpha|=\alpha_1+\alpha_2+\dots+\alpha_n$,
- $\partial_x^k$ be the $k$th partial derivative operator with respect to the independent variable $x$.

Then the $D^{\alpha}$ operator is defined by 
$$D^{\alpha}=\partial^{\alpha_1}_{x_1}\partial^{\alpha_2}_{x_2}\dots\partial^{\alpha_n}_{x_n}$$

## Definition.
*The Linear Differential Operator.*

Take the assumptions of the [[Fourier Series of Periodic Functions#^50927c|definition above]]. For a function $u:\mathbb{R}^{n}\rightarrow\mathbb{R}$, the *Linear Differential Operator* $L(u)$ of order $m$ is defined by
$$L(u)=\sum_{|\alpha|\leq m}u_\alpha(D^{\alpha}u)$$

## Remark.

The index of the sum of a *Linear Differential Operator* is of importance. On a basic level, we are summing over the combinations of multi-indices whose sum is less than or equal to $m$. Whether any two combinations are distinct is governed by some rules of the partial derivative. Most notably,
- Repeated partial derivatives with respect to a single partial derivative commute, but:
- Partial derivatives of distinct variables do not commute.

## Definition.

Let $L(u)$ be a linear differential operator

