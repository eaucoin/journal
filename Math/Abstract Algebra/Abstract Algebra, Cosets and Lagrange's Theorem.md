
## Definition.

Suppose that $(H,\;\star)\leq(G,\;\star)\;\wedge\;a\in G$.
- **Right Coset:** $Ha=\{h\star a\;|\;h\in H\}$
- **Left Coset:** $aH=\{a\star h\;|\;h\in H\}$

## Theorem 1.

Suppose that $(H,\;\star)\leq(G,\;\star)\;\wedge\;(a,\;b)\in G^2$.

| Left Cosets                             | Right Cosets                            |
| --------------------------------------- | --------------------------------------- |
| $H=1_GH$                                | $H=H1_G$                                |
| $aH=H\iff a\in H$                       | $Ha=H\iff a\in H$                       |
| $aH=bH\iff b^{-1}\star a\in H$          | $Ha=Hb\iff a\star b^{-1}\in H$          |
| $a\in bH\implies aH=bH$                 | $a\in Hb\implies Ha=Hb$                 |
| $aH=bH\;\veebar\;aH\cap bH=\varnothing$ | $Ha=Hb\;\veebar\;Ha\cap Hb=\varnothing$ |
 
## Lemma.

Suppose that $(H,\;\star)\leq(G,\;\star)$.
- $(\forall a\in G)(|H|=|Ha|=|aH|)$
- The map $Ha\rightarrow a^{-1}H$ is a bijection $\{Ha\;|\;a\in G\}\rightarrow\{bH\;|\;b\in G\}$


## Definition. 

$$\begin{align*}(H,\;\star)\leq(G,\;\star)\implies|G:H|&=|\{aH\;|\;a\in G\}|\\&=|\{Ha\;|\;a\in G\}|\\&=\text{the index of }H\text{ in }G\end{align*}$$

## Theorem 2.

Suppose that $(H,\;\star)\leq(G,\;\star)$ and $(G,\;\star)$ is finite.
- $|H|$ divides $|G|$
- $|G:H|=\frac{|G|}{|H|}$

## Corollary 1.

$$\begin{align*}&(G,\;\star)\text{ is finite}\;\wedge\;g\in G\\\implies&o(g)\bigg||G|\end{align*}$$
## Corollary 2.

Let $(G,\;\star)$ be a group. 
$$|G|=n\implies (\forall g\in G)(g^n=1)$$

## Corollary 3.
*Groups of Prime Cardinality Are Cyclic.*

Let $(G,\;\star)$ be a group and $p$ be a prime number.
$$|G|=p\implies (\exists g\in G)(G=\langle g \rangle)$$

## Corollary 4.

$$\begin{align*}(H,\;\star)&,\;(K,\;\star)\leq(G,\;\star)\;\wedge\;\gcd(|H|,|K|)=1\\\\\implies H&\cap K=\{1_G\}\end{align*}$$

## Definition.

The dihedral group, called $D_n$ is of the form 
$$D_n=\{1,a,a^2,\dots,a^{n-1},b,ba,ba^2,\dots ba^{n-1}\}\text{,}$$
with the restrictions that
- $o(a)=n$
- $o(b)=2$
- $aba=b$.

By this definition, $|D_n|=2n$, and for all $k\in\mathbb{Z}$,
- $a^kb=ba^{-k}=ba^{n-k}$
- $o(ba^k)=2$

## Theorem 3.

Let $p$ be a prime number.
$$|G|=2p\implies G\text{ is cyclic}\;\veebar\;G\cong D_p$$

## Definition.
*The Euler $\phi$ function.*

$$\phi(n)=|\{k\in\mathbb{Z}\;|\;k<n\;\wedge\;\gcd(k,n)=1\}|$$

## Theorem 4.
*Euler's Theorem.*

$$\begin{align*}(&a,n)\in\mathbb{Z}\times\mathbb{Z}_{\geq 2}\;\wedge\;\gcd(a,n)=1\\\\\implies&a^{\phi(n)}\equiv 1\pmod n\end{align*}$$

## Corollary.
*Fermat's Little Theorem.*

Let $p$ be a prime number.
$$(\forall a\in\mathbb{Z})(a^{p-1}\equiv 0\pmod p)$$


Message message message message. What is the matter with you??????