
## Definition.

Let $K<G$. Then
$$(\forall(a,\;b)\in G^2)(KaKb=Kab)$$
is the definition of the *multiplication on the set of right cosets*. If
$$\begin{align*}

&(\forall(a,\;a_1,\;b,\;b_1)\in G^4)\\&(Ka=Ka_1\;\wedge\;Kb=Kb_1\implies Kab=Ka_1b_1)\text{,}

\end{align*}$$
then it is the case that this multiplication is *well-defined*.

## Lemma.

Suppose that $K<G$; then the statements that
- $K\triangleleft G$,
- $KaKb=Kab$ is a well defined multiplication of right cosets,
are equivalent.

## Theorem 1.

Suppose that $K\triangleleft G$, and write $G/K=\{Ka\;|\;a\in G\}$ for the set of right cosets of $K$ in $G$. Then all of the following statements are true:
- $G/K$ is a group under the operation $KaKb=Kab$,
- $\phi:G\rightarrow G/K$, where $\phi(a)=Ka$ is an onto homomorphism,
- $G$ is abelian $\implies G/K$ is abelian,
- $G=\langle a\rangle$ is cyclic $\implies G/K=\langle Ka\rangle$ is cyclic,
- $|G:K|$ is finite $\implies |G/K|=|G:K|$,
- $G$ is finite $\implies |G/K|=\frac{|G|}{|K|}$.

## Theorem 2.

Let $G$ be a group. If there exists a subgroup $K\subseteq Z(G)$ such that $G/K$ is cyclic, then $G$ is abelian.

## Lemma.

Suppose that $H\triangleleft G$. Then the factor group $G/H$ is abelian iff
$$\begin{align*}

&HaHb=HbHa\\
\iff &Hab=Hba\\
\iff &ab(ba)^{-1}\in H\\
\iff &aba^{-1}b^{-1}\in H\text{.}

\end{align*}$$

## Definition.

Let $G$ be a group. The **