
## Definition.

If $x_n$ is an ordered list of real numbers that are in a set $S$, then $x_n$ is called a *sequence*.

## Definition.

If a sequence $x_n$ approaches a real number $L$ as a natural number $n$ approaches infinity, then we write $x_n\rightarrow L\in \mathbb{R}\text{ as }n\rightarrow \infty$. 

## Definition 1.2.1.

$$\begin{align*}

&x_n\rightarrow L\in\mathbb{R}\text{ as }n\rightarrow\infty\\\\

\iff &\bigg(\forall\epsilon\in\mathbb{R}_{>0}\bigg)\bigg(\exists N\in \mathbb{N}\bigg)\bigg(N\leq n\implies |x_n-L|<\epsilon\bigg)

\end{align*}$$
## Definition. 

There are two mutually exclusive possibilities. The sequence $x_n$ is:
-  *convergent*: $(\exists L\in\mathbb{R})(x_n\rightarrow L)$, or 
- *divergent*.

## Example 1.1.

Let $x_n=\frac{1}{n}$. Then $x_n\rightarrow 0$.

**Proof.** We need to show that there exists $N\in\mathbb{N}$ such that 
$$N\leq n\implies \frac{1}{n}<\epsilon\text{.}$$
Consider the 


We need to show that there exists $n\in\mathbb{N}$ such that $\frac{1}{n}<\epsilon$.
$$\begin{align*}

&\frac{1}{n}<\epsilon
\\\\\iff &1<\epsilon n\text{.}

\end{align*}$$
Then since $1$ and $\epsilon$ are elements of an [[Advanced Calculus, The Real Number System#^3a5710|Archimedian Ordered Field]], the latter statement is indeed the case. 


