
## Definition.

Let $(G,\;\star)$ and $(H,\;\cdot)$ be groups, and $\alpha:G\rightarrow H$. Then
$$\alpha\textbf{ is a homomorphism}\iff (\forall(a,\;b)\in G^2)(\alpha(a\star b)=\alpha(a)\cdot \alpha(b))$$
## Theorem 1.

If $\alpha:G\rightarrow H$ is a group homomorphism, then
- $\alpha(1_G)=1_G$
- $(\forall g\in G)(\alpha(g^{-1})=\alpha(g)^{-1})$
- $(\forall(g,\;k)\in G\times\mathbb{Z})(\alpha(g^k)=\alpha(g)^k)$

### Corollary 1.

Let $\alpha:G\rightarrow H$ be a group homomorphism. If $g\in G$ has finite order $o(g)$, then
- $\alpha(g)$ has finite order.
- $o(\alpha(g))\big|o(g)$

### Corollary 2.

Let $\alpha:G\rightarrow H$ be a group homomorphism and $\alpha(G)=\{\alpha(G)\;|\;g\in G\}$,
$$\implies \alpha(G)\text{ is a subgroup of } H\text{.}$$

## Theorem 2.

Let $(G,\;\star)$ and $(H,\;\cdot)$ be groups, and let $\alpha$ and $\beta$ be homomorphisms between them.
$$G=\langle X\rangle\implies(\forall x\in X)(\alpha=\beta\iff \alpha(x)=\beta(x))$$

## Definition.

Let $(G,\;\star)$ and $(H,\;\cdot)$ be groups, and let $\alpha:G\rightarrow H$ be a homomorphism. Then
$$\begin{align*}\alpha\text{ is an isomorphism}\iff &\alpha\text{ is a bijection}\\\iff&G\cong H\\\iff&\alpha:G\xrightarrow\sim H\end{align*}$$

## Theorem 3.

Let $(G,\;\star)$, $(H,\;\times)$, and $(K,\;\cdot)$ be groups.
- $1_G:G\xrightarrow\sim G$
- $\sigma:G\xrightarrow\sim H\implies \sigma^{-1}:G\xrightarrow\sim H$
- $\sigma:G\xrightarrow\sim H\;\wedge\;\tau:H\xrightarrow\sim K\implies \tau\circ\sigma:G\xrightarrow{\sim}K$

## Corollary 1.

The $\cong$ relation is an equivalence relation--that is, it is reflexive, symmetric, and transitive.

## Definition.

Let $(G,\;\star)$ be a group, and $\alpha:G\xrightarrow{\sim}G$. Then $\alpha$ is called an automorphism.

## Definition.

Let $(G,\;\star)$ be a group, and suppose that $a\in G$. The mapping $\sigma_a:G\rightarrow G$ with the property that 
$$(\forall g\in G)(\sigma_a(g)=aga^{-1})$$
is called in inner automorphism of $G$ determined by $a$.

## Theorem 4.

$$\sigma:G\xrightarrow{\sim}G\implies(\forall g\in G)(o(\sigma(g))=o(g))$$

## Theorem 5.
*Cayley's Theorem*

Let $G$ be a group. Then
$$o(G)=n\implies G\cong S_n\text{.}$$

