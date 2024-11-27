<div style="text-align: center;">
  <h1 style="margin: 0; font-weight: bold;">The Fast Fourier Transform:</h1>
  <h2 style="margin: 0;">A Matrix-Oriented Perspective</h2>
</div>

## The Conjugate Transpose

Let $\mathbb{C}$ denote the complex numbers. For natural numbers $m,n\in\mathbb{N}$, we can discuss *complex matrices* as being elements of the cartesian product of $\mathbb{C}$ and itself $m\times n$ times–written $\mathbb{C}^{m\times n}$ for short. For a natural number $n\in\mathbb{N}$, we can discuss *complex vectors* as being the cartesian product of $\mathbb{C}$ and itself $n\times 1$ times–written $\mathbb{C}^{n\times 1}$ or $\mathbb{C}^{n}$ for short. 

We can write elements of these two sets in an index-oriented way that is useful for discussing matrices. An element in $\mathbb{C}^{m\times n}$ or $\mathbb{C}^{n}$ can be written as $(a_{ij})_{m\times n}\in \mathbb{C}^{m\times n}$ or $(a_{ij})_{n\times1}\in \mathbb{C}^n$, respectively. Since $a_{ij}$ represents a complex number in both of these cases, we have an equivalent way of writing these elements as  $(a_{ij}+ib_{ij})_{m\times n}\in \mathbb{C}^{m\times n}$ or $(a_{j}+ib_{j})_{n\times1}\in \mathbb{C}^n$, respectively–where
$$(\forall(i,j)\in I\times J)((a_{ij},\;b_{ij})\in\mathbb{R}^2)\text{.}$$
Now, we have a strong descriptive footing to describe complex vectors and matrices efficiently. The *conjugate transpose* of a matrix or a vector in $(a_{ij}+ib_{ij})_{m\times n}\in \mathbb{C}^{m\times n}$ can be written
$$(a_{ji}-ib_{ji})_{m\times n}\in \mathbb{C}^{m\times n}\text{.}$$
For $A\in\mathbb{C}^{m\times n}$, we can write the conjugate transpose of $A$ as $A^H$; we use the letter $H$ for Charles Hermite, a french mathematician whose was concerned with such matrices.

### Lemma 1.

For all $m,n\in\mathbb{N}$, the conjugate transposition $A^H\in\mathbb{C}^{n\times m}$ of a matrix $A\in\mathbb{C}^{m\times n}$ has four fundamental properties that hold for all $\lambda\in\mathbb{C}$:
- $(A^H)^H=A$,
- $(A+B)^H=A^H+B^H$,
- $(\lambda A)^H=\overline{\lambda}A^H$,
- $(AB)^H=B^HA^H$.
These are proven though the properties of complex numbers and comparing the matrix entries of flipped indices.

## Defining an Inner Product Space on $\mathbb{C}^n$

With the above objects and operations described, we are ready to define an inner product space on the complex vector space.

### Proposition 1.

$(\mathbb{C}^n,\;\mathbb{F},\;+,\;\cdot)$ is a vector space. We will not prove this; it can easily be shown by testing the vector space axioms on the $n\times 1$ dimensional matrices above.

### Proposition 2.

The algebraic structure $(\mathbb{C}^n,\;\mathbb{F},\;+,\;\cdot,\;\langle\cdot,\;\cdot\rangle)$, with an inner product defined by
$$\langle a,\;b\rangle:(a,b)\mapsto a^Hb\text{, for all }a,b\in\mathbb{C}^n\text{,}$$
is an inner product space.

**Proof.**

In testing all of the requirements, we'll employ the properties from **Lemma 1**. Testing for conjugate symmetry, 
$$\begin{align*}

\overline{\langle b,\;a\rangle}&=\overline{b^Ha}\\
&=b^T\overline{a}\\
&=(a^Hb)^{T}\\
&=a^Hb\\
&=\langle a,\;b\rangle\text{.}

\end{align*}$$
Testing for first-argument linearity, we have
$$\begin{align*}

\langle \lambda a+\mu b,\;c\rangle&=(\lambda a+\mu b)^Hc\\
&=\overline{\lambda}a^Hc+\overline{\mu}b^Hc\\
&=\overline{\lambda}\langle a,\;c\rangle+\overline{\mu}\langle a,\;c\rangle\text{.}

\end{align*}$$
Testing, for positive-definiteness,
$$\begin{align*}

\langle a,\;a\rangle&=a^Ha\\\\
&=\bigg(\sum_{j=1}^{n}[(a_j-b_ji)(a_j+b_ji)]\bigg)_{1\times 1}\\\\
&=\bigg(\sum_{j=1}^{n}[a_j^2+b_j^2]\bigg)_{1\times 1}\\\\
&>0\text{ for all }j\in J\\\wedge&=0\iff (\forall j\in J)(a_j=0)\\\\
&\implies(\forall a,b\in \mathbb{C}^n)(\langle a,\;a\rangle>0)\text{, and:}\\&\;\;\;\;\;\;\;\;\;\langle a,\;a\rangle=0\iff a=0\text{.}

\end{align*}$$
With **Proposition 1** and these three properties shown, we have proven that $(\mathbb{C}^n,\;\mathbb{F},\;+,\;\cdot,\;\langle\cdot,\;\cdot\rangle)$ is an inner product space.

## Length in $\mathbb{C}^n$

With our inner product space defined, we can now describe length in $\mathbb{C}^n$. 

### Lemma 2.

The *length* of a vector $x$ in an inner product space is given by the $L^2$ norm, $\langle x,\;x\rangle^{\frac{1}{2}}$. 

### Proposition 3. 

By **Proposition 2** and **Lemma 2**, the length of a vector $x$ in $\mathbb{C}^n$ is given by $(x^Hx)^{\frac{1}{2}}$.

## The Kronecker Delta Function

For $n\in \mathbb{N}$, let $I=\{1,2,\dots,n\}$ be an *index set*. The Kronecker Delta function is a map $\delta:I^2\rightarrow\{0,1\}$ defined by
$$\begin{align*}\delta(i,\;j)&=\begin{cases}

1 & \text{if }i=j\\
0 & \text{if }i\neq j

\end{cases}

\\\\&=\delta_{ij}\text{.}

\end{align*}$$

### Lemma 3.

For $n\in\mathbb{N}$, the Kronecker Delta function maps precisely the indices of the entries of the identity matrix, $I_n$, to their values.

## Hermitian Matrices

For $n\in\mathbb{N}$, a Hermitian matrix of size $n$ is an element of $\mathbb{C}^{n\times n}$ that is equal to its conjugate transpose. In a conventional notation, a matrix $A\in\mathbb{C}^{n\times n}$ is Hermitian if and only if $A^H=A$, and in our index-minded notation, a matrix $(a_{ij}+b_{ij}i)_{n\times n}\in\mathbb{C}^{n\times n}$ is Hermitian if and only if
$$(\forall(i,\;j)\in I^2)(a_{ij}+b_{ij}i=a_{ji}-b_{ji}i)\text{.}$$
Using the properties of **Lemma 1**, we have an equivalence statement that conveys the same meaning. 

### Proposition 4. 

For $n\in\mathbb{N}$, a matrix $A\in\mathbb{C}^{n\times n}$ has the property that $A=A^H$ if and only if 
$$(\forall b,c\in\mathbb{C}^n)(\langle Ab,\;c\rangle=\langle b,\;Ac\rangle)\text{.}$$
**Proof.**

The algebraic properties of **Lemma 1** combined with the inner product developed in **Proposition 2** deliver 
$$\begin{align*}

&\langle Ab,\;c\rangle=\langle b,\;Ac\rangle\\
\iff&(Ab)^Hc=b^HAc\\
\iff&b^HA^Hc=b^HAc\\
\iff&bb^HA^Hcc^H=bb^HAcc^H\\
\iff&||b||^2\cdot||a||^2A^H=||b||^2\cdot||a||^2A\\
\iff& A^H=A\text{.}
\end{align*}$$
This completes the heavy lifting that is required to prove a special property on the eigenvalues of Hermitian matrices.

### Proposition 5.

Let $A$ be a Hermitian matrix. Then:
1. Eigenvalues of $A$ are real,
2. Eigenvectors of $A$ are pairwise orthogonal.

**Proof.**

1. Suppose that $A$ has an eigenvalue $\lambda$ whose eigenvector is $v$. Then $Av=\lambda v$. Working through this and using **Proposition 4** under the tools of **Lemma 1**, we have that

$$\begin{align*}

&Av=\lambda v\;\wedge\;\langle Av,\;\lambda v\rangle=\langle v,\;A(\lambda v)\rangle\\
\iff&Av=\lambda v\;\wedge\;(Av)^H(\lambda v)=v^HA(\lambda v)\\
\implies& (\lambda v)^H(\lambda v)=\lambda v^H(\lambda v)\\
\iff&\overline{\lambda}\cdot\lambda\cdot||v||^2=\lambda\cdot\lambda\cdot||v||^2\\
\implies&\overline{\lambda}=\lambda\\
\implies&\lambda\in\mathbb{R}\text{.}\\

\end{align*}$$
2. Suppose that $\lambda$ and $\mu$ are distinct eigenvalues of $A$ whose eigenvectors are $v$ and $w$, respectively. Using **Proposition 4**, we can show that

$$\begin{align*}

A&v=\lambda v\;\wedge\;Aw=\mu w\;\\
\wedge\;\langle A&v,\;w\rangle=\langle v,\;Aw\rangle\\
\iff\langle \lambda &v,\;w\rangle=\langle v,\;\mu w\rangle\\
\iff\lambda\langle &v,\;w\rangle=\mu \langle v,\;w\rangle\\
\implies\langle&v,\;w\rangle=0\text{.}

\end{align*}$$

## Unitary Matrices

For $n\in\mathbb{N}$, there exists an equivalent set of statements for a matrix $A\in\mathbb{C}^{n\times n}$ related to the orthogonality of its rows and columns:
- $(\exists A^{-1}\in\mathbb{C}^{n\times n})(AA^{-1}=A^{-1}A=I_n)$,
- $(\forall(i,\;j)\in I^2_{i\neq j})(\langle c_i,\;c_j\rangle=\langle r_i,\;r_j\rangle=0)$, where $c_k$ and $r_k$ are the $k$th column and row vectors of $A$, respectively. 

We can encapsulate this notion through the definition of a unitary matrix: for $n\in\mathbb{N}$, an element in $U\in\mathbb{C}^{n\times n}$ is called *unitary* if and only if 
$$UU^H=U^HU=I\text{.}$$
Said another way, $U$ is unitary if and only if it is inverted by its Hermitian transpose, $U^H$, under the operation of production.

## The Discrete Fourier Transform

Suppose that we have an instrument that measures some kind of time-periodic phenomena. The instrument takes $n$ measurements at evenly-spaced time steps, say $t_0$, then $t_1$, up to the last step of a period at $t_{n-1}$. At each of these time steps, the instrument reads $f(t_0)$, then $f(t_1)$, up to the last step of the period at $f(t_{n-1})$.

Reframe these time steps in terms of the period of a trigonometric function: starting at $0$ radians, take evenly-spaced steps, $n-1$ times, toward $2\pi$: we start with $\frac{0}{n}(2\pi)$ radians, then $\frac{1}{n}(2\pi)$ radians, up to the last step of the period at $\frac{n-1}{n}(2\pi)$ radians. If we took another step, we'd be in a redundant position in the unit circle, one already covered by previous steps. 

This is the idea of a root of unity: when multiplied by the imaginary unit $i$ and then exponentiated, these positions on the unit circle are the set of the $n$th *roots of unity*, written
$$\begin{align*}

\{z\in\mathbb{C}\;|\;z^n=1\}&=\{e^{\frac{2\pi k}{n}}\in\mathbb{C}\;|\;k<n\}\\\\
&=\bigg\{e^{\frac{2\pi(0)}{n}},e^{\frac{2\pi(1)}{n}},\dots,e^{\frac{2\pi(n-1)}{n}}\bigg\}

\end{align*}$$
The Discrete Fourier Transform employs the idea of approximating a nice, continuous version of $f(t)$ from the information that we have, by assuming that for some $c_0,c_1,\dots,c_{n-1}\in\mathbb{C}$,
$$f(t_i)=\sum_{k=0}^{n-1}c_ke^{t_i\frac{2\pi ki}{n}}\text{,}$$
and removing the index after solving for $c_k$; this suggests that we will need to set up a linear system. Let $\omega=e^{\frac{2\pi i}{n}}$. Then our linear system presents as
$$(\omega^{jk})_{n\times n}(c_j)_{n\times 1}=(f(t_j))_{n\times 1}\text{,}$$
where we may call $(\omega^{(j-1)(k-1)})_{n\times n}$ the *Fourier Matrix*, also written $F_n$, and with all indices starting at $0$. Immediately, we can observe that $F_n$ is symmetric.

### Lemma 4.

$\frac{1}{\sqrt{n}}F_n$ is unitary.

**Proof.**

We make use of element-wise production of matrices.
$$\begin{align*}

&F_n=(\omega^{jk})_{n\times n}\;\wedge\;F_n^H=(\omega^{-jk})_{n\times n}\\\\
\implies&F_nF_n^H=F_n^HF_n=\bigg(\sum_{k=0}^{n-1}\omega^{jk}\omega^{-ik}\bigg)\\\\
&=\bigg(\sum_{k=0}^{n-1}\omega^{k(j-i)}\bigg)

\text{,}

\end{align*}$$
where the $i$ index accounts for the sequential columns of $F^H$. If $i=j$, then $j-i=0$, and each term of the sum is $\omega^0=1$, so the sum is $n$.

If $i\neq j$, then $\alpha=\omega^{k(j-i)}$ is in the set of $n$th roots of unity; taking into account the cyclic nature, we could replace the sum with a static $\alpha$, giving
$$\sum_{j=0}^{n-1}\alpha^k\text{.}$$
This is a finite geometric series. On this subject, we can note that 
$$\begin{align*}

(1-\alpha)(1+\alpha+\alpha^2+\dots+\alpha^{n-1})=&(1+\alpha+\alpha^2+\dots+\alpha^{n-1})\\
&-(\alpha+\alpha^2+\dots+\alpha^n)\\\\

=&\;\;1-\alpha^n\\\\

\iff&\;\frac{1-\alpha^n}{(1-\alpha)}=\sum_{j=0}^{n-1}\alpha^k

\end{align*}$$
But $n$ steps past the first step in our circle leads us to the beginning, at $1$. Therefore, $\alpha^n=1$, so $\frac{1-\alpha^n}{(1-\alpha)}=0$, so $\sum_{j=0}^{n-1}\alpha^k=0$, so $\bigg(\sum_{k=0}^{n-1}\omega^{k(j-i)}\bigg)=0$, for $i\neq j$. 

By **Lemma 3**, we now have that $F_nF_n^H=nI_n$. Then 
$$\begin{align*}

\bigg(\frac{1}{\sqrt{n}}F_n\bigg)\bigg(\frac{1}{\sqrt{n}}F_N\bigg)^H&=\frac{1}{n}F_nF^H_n\\\\
&=\frac{1}{n}\cdot n\cdot I_n\\\\
&=I_n\text{,}

\end{align*}$$
and our fact is proven.

---------

We've therefore found a method for solving a linear system of complex exponentials with $n$ steps per period, spread over the roots of unity, which allow us to approximate $f(t)$. To compute either $(\omega^{jk})_{n\times n}$ or $(f(t_j))_{n\times 1}$, we simply need to multiply by $F$