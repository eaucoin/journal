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

## Defining an Inner Product Space on $\mathbb{C}^n$

With the above objects and operations described, we are ready to define an inner product space $(\mathbb{C}^n,\;\mathbb{C},\;+,\;\cdot,\;\langle\cdot,\;\cdot\rangle)$. 

### Proposition 1.

$(\mathbb{C}^n,\;\mathbb{C},\;+,\;\cdot)$ is a vector space. We will not prove this; it can easily be shown by testing the vector space axioms on the $n\times 1$ dimensional matrices above.

### Proposition 2.

The algebraic structure $(\mathbb{C}^n,\;\mathbb{F},\;+,\;\cdot,\;\langle\cdot,\;\cdot\rangle)$, with an inner product defined by
$$\langle a,\;b\rangle:(a,b)\mapsto a^Hb\text{, for all }a,b\in\mathbb{C}^n\text{,}$$
is an inner product space.

**Proof.**

Denote $a,b,c\in\mathbb{C}^n$ as $(a_{j}+b_{j}i)_{n\times 1}\in\mathbb{C}^n$, $(c_{j}+d_{j}i)_{n\times 1}\in\mathbb{C}^n$, and $(e_j+f_ji)_{n\times 1}$ respectively. Then $a^H=(a_{j}-b_{j}i)_{n\times 1}$. Testing for conjugate symmetry, 
$$\begin{align*}

\overline{\langle b,\;a\rangle}&=\overline{b^Ha}\\&
=(\overline{\sum_{j=1}^{n}[(c_j-d_ji)(a_j+b_ji)}])_{1\times 1}\\&
=(\overline{\sum_{j=1}^{n}[a_jc_j+b_jd_j+i(b_jc_j-a_jd_j)]})_{1\times 1}\\&
=(\sum_{j=1}^{n}[a_jc_j+b_jd_j-i(b_jc_j-a_jd_j)])_{1\times 1}\text{, and}

\end{align*}$$
$$\begin{align*}

\langle a,\;b\rangle&=a^Hb\\&
=(\sum_{j=1}^{n}[(a_j-b_ji)(c_j+d_ji)])_{1\times 1}\\&
=(\sum_{j=1}^{n}[a_jc_j+b_jd_j+i(a_jd_j-b_jc_j)])_{1\times 1}\\&
=(\sum_{j=1}^{n}[a_jc_j+b_jd_j-i(b_jc_j-a_jd_j)])_{1\times 1}\\&
=\overline{\langle b,\;a\rangle}\text{.}

\end{align*}$$
Testing for first-argument linearity, we have
$$\begin{align*}

\langle\psi a+\phi b,\;c\rangle&=(\sum_{j=1}^{n}[(\psi(a_j+b_ji)+\phi(c_j+d_ji))(e_j+f_ji)])_{1\times 1}\\

&=(\sum_{j=1}^{n}[(\psi(a_j+b_ji)(e_j+f_ji)+\phi(c_j+d_ji)(e_j+f_ji))])_{1\times 1}\\

&=(\sum_{j=1}^{n}[\psi(a_j+b_ji)(e_j+f_ji)])_{1\times 1}+(\sum_{j=1}^{n}[\phi(c_j+d_ji)(e_j+f_ji)])_{1\times 1}\\

&=\psi(\sum_{j=1}^{n}[(a_j+b_ji)(e_j+f_ji)])_{1\times 1}+\phi(\sum_{j=1}^{n}[(c_j+d_ji)(e_j+f_ji)])_{1\times 1}\\

&=\psi\langle a,\;c\rangle+\phi\langle b,\;c\rangle\text{.}

\end{align*}$$
If for all $j\in J$, $a_j,b_j\neq 0$, then
$$\begin{align*}

\langle a,\;a\rangle&=(\sum_{j=1}^{n}[(a_j+b_ji)(a_j+b_ji)])_{1\times 1}\\
&=(\sum_{j=1}^{n}[a_j^2-b_j^2+2a_jb_ji])_{1\times 1}\text{,}

\end{align*}$$
which implies that the imaginary part is never zero; therefore, we have positive-definiteness.

With **Proposition 1** and these three properties shown, we have proven that $(\mathbb{C}^n,\;\mathbb{F},\;+,\;\cdot,\;\langle\cdot,\;\cdot\rangle)$ is an inner product space.

## Length in $\mathbb{C}^n$

With our inner product space defined, we can now describe length in $\mathbb{C}^n$. 

### Lemma 1.

The *length* of a vector $x$ in an inner product space is given by the $L^2$ norm, $\langle x,\;x\rangle^{\frac{1}{2}}$. 

### Proposition 3. 

By **Proposition 2** and **Lemma 1**, the length of a vector $x$ in $\mathbb{C}^n$ is given by $(x^Hx)^{\frac{1}{2}}$.

## The Kronecker Delta Function

$et $I=\{1,2,\dots,n\}$ be an *index set*. The Kronecker Delta function is a map $\delta:I^2\rightarrow\{0,1\}$ defined by
$$\begin{align*}\delta(i,\;j)&=\begin{cases}

1 & \text{if }i=j\\
0 & \text{if }i\neq j

\end{cases}

\\\\&=\delta_{ij}\text{.}

\end{align*}$$

## Hermitian Matrices

For $n\in\mathbb{N}$, a Hermitian matrix of size $n$ is an element of $\mathbb{C}^{n\times n}$ that is equal to its conjugate transpose. In a conventional notation, a matrix $A\in\mathbb{C}^{n\times n}$ is Hermitian if and only if $A^H=A$, and in our index-minded notation, a matrix $(a_{ij}+b_{ij}i)_{n\times n}\in\mathbb{C}^{n\times n}$ is Hermitian if and only if
$$(\forall(i,\;j)\in I^2)(a_{ij}+b_{ij}i=a_{ji}-b_{ji}i)\text{.}$$

### Lemma 2.

The conjugate transposition $A^H\in\mathbb{C}^{n\times n}$ of a matrix $A\in\mathbb{C}^{n\times n}$ has four fundamental properties:
- $(A^H)^H=A$
- $(A+B)^H=A^H+B^H$
- 