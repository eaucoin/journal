
## Definition.

$$\begin{align*}

H\text{ is a normal subgroup of }G\iff&(\forall g\in H)(aH=Ha)\\\\
\iff&H\triangleleft G

\end{align*}$$

## Theorem 1.

For all groups $(G,\;\star)$,
$$(H,\;\star)<(Z(G),\;\star)\implies H\triangleleft G\text{.}$$

## Theorem 2.

$$\begin{align*}

(G,\;\star)\text{ is abelian}\;\wedge\;&(H,\;\star)<(G,\;\star)\\\\

\implies&H\triangleleft G\text{.}

\end{align*}$$

## Theorem 3. 
*Normality Test.*

$$\begin{align*}

&H\triangleleft G\\\\
\iff &(\forall g\in G)(g\star H\star g^{-1}\subseteq H)\\\\
\iff &(\forall g\in G)(g\star H\star g^{-1}=H)\text{.}

\end{align*}$$

## Corollary 1.

If $G=\langle X \rangle$,
$$(H,\;\star)<(G,\;\star)\;\wedge\;H\triangleleft G\iff(\forall x\in X)(x\star H\star x^{-1}\subseteq H)\text{.}$$

## Corollary 2.

Let $G$ be a group. Then
$$(\exists !H\in \mathcal{P}(G))(H<G\;\wedge\;H\cong G)\implies H\triangleleft G\text{.}$$

## Definition.

Suppose that $(H,\;\star)<(G,\;\star)$. Then $H$ is called a *characteristic subgroup* of $G$ iff for all automorphisms $\alpha:G\rightarrow G$,
$$\alpha(H)=H\text{.}$$
We can also write this relationship $\text{CharIn}(H,\;G)$.
## Corollary 3.

$$\begin{align*}

&K\triangleleft G\;\wedge\;H\subseteq K\;\wedge\;\text{CharIn}(H,\;K)\\\\

\implies& H\triangleleft G\text{.}

\end{align*}$$

## Theorem 4.

$$\begin{align*}

&(H,\;\star)<(G,\;\star)\;\wedge\;|G:H|=2\\\\
\implies &H\triangleleft G\text{.}

\end{align*}$$

## Lemma 1.

$$\begin{align*}

&H\triangleleft G\;\wedge\; K\triangleleft G\;\wedge\;H\cap K=\{1\}\\\\\implies &(\forall(h,\;k)\in H\times K)(h\star k=k\star h)

\end{align*}$$

## Definition.

Let $(G,\;\star)$ be a group, with $(H,\;\star)$ and $(K,\;\star)$ subgroups of $(G,\;\star)$. Then the *product* of $H$ and $K$, written $HK$, is
$$HK=\{h\star k\;|\;(h,\;k)\in H\times K\}\text{.}$$

## Lemma 2.

Let $(G,\;\star)$ be a group, with $(H,\;\star)$ and $(K,\;\star)$ subgroups of $(G,\;\star)$. Then, the following statements are equivalent:
- $(HK,\;\star)<(G,\;\star)$,
- $(KH,\;\star)<(G,\;\star)$
- $HK=KH$.

## Theorems 5&6.

Let $(G,\;\star)$ be a group, with $(H,\;\star)$ and $(K,\;\star)$ subgroups of $(G,\;\star)$.
- $H\triangleleft G\;\vee\;K\triangleleft G\implies HK=KH< G$,
- $H\triangleleft G\;\wedge\;K\triangleleft G\implies HK\triangleleft G$,
and:
$$\begin{align*}

&H\triangleleft G\;\wedge\;K\triangleleft G\;\wedge\;H\cap K=\{1\}\\\\
\implies &HK\cong H\times K\text{.}

\end{align*}$$

## Corollary 1.

Let $(G,\;\star)$ be a finite group. Then
$$\begin{align*}

&H<G\;\wedge\;K< G\;\wedge\;H\cap K=\{1\}\\\\
\implies &|HK|=|H||K|\text{.}

\end{align*}$$

## Corollary 2.

Let $(G,\;\star)$ be a finite group. Then
$$\begin{align*}

&H\triangleleft G\;\wedge\;K\triangleleft G\;\wedge\;H\cap K=\{1\}\;\wedge\;|HK|=|H||K|\\\\
\implies &HK\cong H\times K\text{.}

\end{align*}$$

## Definition.

Let $(G,\;\star)$ be a group. Then $G$ is called a *simple* group iff the properties
- $G\neq\{1\}$,
- $\{1\}$ and $G$ are the only normal subgroups of $G$,
are satisfied.

## T