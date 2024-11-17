
## Definition 1.

Let $G$ be a set, and suppose that $(G,\;\star)$ is a [[Abstract Algebra, Introduction to Groups|group]]. A set $H$ is called a subgroup of $(G,\;\star)$ iff $(H,\;\star)$ is a group. We may also write $(H,\;\star)\leq (G,\;\star)$ to denote the subgroup relationship.

## Theorem 1.

Let $H\subseteq G$. Then $(H,\;\star) \leq(G,\;\star)$ iff:

- $1_G\in H$
- $(\forall(h_1,\;h_2)\in H^2)(h_1\star h_2\in H)$
- $(\forall h\in H)(\exists h'\in H)(h\star h'=1_G)$

## Theorem 2.

Let $(G,\;\star)$ be a group. Suppose that $H$ is a *finite subset* of $G$. Then
$$(H,\;\star)\leq(G,\;\star)\iff(\forall(h_1,\;h_2)\in H^2)(h_1\star h_2\in H)$$

## Definition 2.

Let $(G,\;\star)$ be a group. The set 
$$Z(G)=\{z\in G\;|\;(\forall g\in G)(z\star g=g\star z)\}$$
is called the center of $(G,\;\star)$.

## Theorem 3.

$(G,\;\star)$ is a group $\implies (Z(G),\;\star)\leq(G,\;\star)\;\wedge\;(Z(G),\;\star)$ is abelian

## Theorem 4.

$$(H,\;\star),\;(K,\;\star)\leq(G,\;\star)\implies (H\cap K,\;\star)\leq(G,\;\star)$$

## Theorem 5.

$$(H,\;\star)\leq(G,\;\star)\implies(\forall g_1\in G)((\{g_1g_2g_1^{-1}\;|\;g_2\in G\},\;\star)\leq(G,\;\star))$$

