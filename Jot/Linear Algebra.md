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

\langle \lambda a,\;b\rangle&=(\lambda a)^Hb\\
&=a^H\overline{\lambda}b\\
&=\overline{\lambda}\langle a,\;b\rangle\text{.}

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
2. Suppose that $\lambda$ and $\mu$ are eigenvalues of $A$ whose eigenvectors are $v$ and $w$, respectively. Working as in **(1)**, we can show that
$$\begin{align*}

&Av=\lambda v\;\wedge\;Aw=\lambda w\\
\wedge\;&\langle Av,\;\lambda v\rangle=\langle v,\;A(\lambda v)\rangle\\
\wedge\;&\langle Av,\;\lambda v\rangle=\langle v,\;A(\lambda v)\rangle


\end{align*}$$
