
## Definition 1.

A set $G$ is a group $(G,\;\star)$ iff it satisfies four axioms:

- $(\forall(a,\;b)\in G^2)(a\star b\in G)$
- $(\forall(a,\;b,\;c)\in G^3)((a\star b)\star c=a\star(b\star c))$
- $(\exists u\in G)(\forall a\in G)(u\star a=a\star u=a)$
- $(\forall a\in G)(\exists b\in G)(a\star b=u)$

And it is called abelian if it satisfies the extra axiom:

- $(\forall(a,\;b)\in G^2)(a\star b=b\star a)$

which is to say that it is called abelian if it is commutative.

## Theorem 1.

Let $M$ be a monoid. The subset $M^*$ of the elements in $M$ that are invertible is a group.

## Definition 2.

If $(G_1,\;\star),(G_2,\;\star),\dots,(G_n,\;\star)$ are groups, then $(G_1\times G_2\times\cdots\times G_n,\;\star)$ is a group with the component-wise operation

$$\begin{align*}(\forall(&(g_1,\;g_2,\;\dots,\;g_n),(g_1',\;g_2',\;\dots,\;g_n'))\in (G_1\times G_2\times\cdots\times\ G_n)^2)\\(&(g_1,\;g_2,\;\dots,\;g_n)\star(g_1',\;g_2',\;\dots,\;g_n')=(g_1\star g_1',\;g_2\star g_2',\;\dots,\;g_n\star g_n')\end{align*}$$


## Theorem 2.

$G_1,G_2,\dots,G_n$ are groups $\implies G_1\times G_2\times\cdots\times G_n$ is a group with unity $(1,\;1,\dots,\;1)$ and inverse equality $(g_1,\;g_2,\;\dots,\;g_n)^{-1}=(g_1^{-1},\;g_2^{-1},\;\dots,\;g_n^{-1})$

## Theorem 3.

Let $G$ be a group, with $1,\;g,\;h,\;g_1,\;g_2,\dots,\;g_{n-1},\;g_n\in G$.

- $1^{-1}=1$
- $(g^{-1})^{-1}=g$
- $(gh)^{-1}=h^{-1}g^{-1}$
- $(g_1g_2\dots g_{n-1}g_n)=g_n^{-1}g_{n-1}^{-1}\dots g_2^{-1}g_1^{-1}$
- $(g^n)^{-1}=(g^{-1})^n$

## Theorem 4.

$\begin{align*}(\forall(g,\;h,\;m,\;n)\in G^2\times\mathbb{Z}^2)\\(&g^ng^m=g^{n+m}\\\wedge\;(&g^n)^m=g^{nm}\\\wedge\;(&gh=hg\implies (gh)^n=g^nh^n))\end{align*}$

## Theorem 5.

$\begin{align*}(\forall(g,\;h,\;f)\in G^3)((&gh=gf\implies h=f\\\wedge\;(&hg=fg\implies h=f))\end{align*}$

## Theorem 6.

$\begin{align*}(\forall(&g,\;h)\in G^2)\\((\{&x\;|\;gx=h\}=\{g^{-1}h\}\\\wedge\;(\{&x\;|\;xg=h\}=\{hg^{-1}\}))\end{align*}$
