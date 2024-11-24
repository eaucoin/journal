<div style="text-align: center;">
  <h1 style="margin: 0; font-weight: bold;">The Fast Fourier Transform:</h1>
  <h2 style="margin: 0;">A Matrix-Oriented Perspective</h2>
</div>

## The Conjugate Transpose

Let $\mathbb{C}$ denote the complex numbers. For natural numbers $m,n\in\mathbb{N}$, we can discuss *complex matrices* as being elements of the cartesian product of $\mathbb{C}$ and itself $m\times n$ times–written $\mathbb{C}^{m\times n}$ for short. For a natural number $n\in\mathbb{N}$, we can discuss *complex vectors* as being the cartesian product of $\mathbb{C}$ and itself $n\times 1$ times–written $\mathbb{C}^{n\times 1}$ or $\mathbb{C}^{n}$ for short. 

We can write elements of these two sets in an index-oriented way that is useful for discussing matrices. An element in $\mathbb{C}^{m\times n}$ or $\mathbb{C}^{n}$ can be written as $(a_{ij})_{m\times n}\in \mathbb{C}^{m\times n}$ or $(a_{ij})_{n\times1}\in \mathbb{C}^n$, respectively. Since $a_{ij}$ represents a complex number in both of these cases, we have an equivalent way of writing these elements as  $(a_{ij}+ib_{ij})_{m\times n}\in \mathbb{C}^{m\times n}$ or $(a_{ij}+ib_{ij})_{n\times1}\in \mathbb{C}^n$, respectively–where
$$(\forall(i,j)\in I\times J)((a_{ij},\;b_{ij})\in\mathbb{R}^2)\text{.}$$
Now, we have a strong descriptive footing to describe complex vectors and matrices efficiently. The *conjugate transpose* of a matrix or a vector in $(a_{ij}+ib_{ij})_{m\times n}\in \mathbb{C}^{m\times n}$ can be written
$$(a_{ji}-ib_{ji})_{m\times n}\in \mathbb{C}^{m\times n}\text{.}$$
For $A\in\mathbb{C}^{m\times n}$, we can write the conjugate transpose of $A$ as $A^H$; we use the letter $H$ for Charles Hermite, a french mathematician whose was concerned with such matrices.

## Defining an Inner Product Space on $\mathbb{C}^n$

