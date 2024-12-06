
## Definition.

Let $G$ and $H$ be groups and $\alpha$ a homomorphism between them. The *image* of $\alpha$, written $\text{im}(\alpha)$, is defined by
$$\begin{align*}

\text{im}(\alpha)&=\alpha(G)\\\\
&=\{\alpha(g)\;|\;a\in G\}\text{.}

\end{align*}$$

The *kernel* of $\alpha$, written $\text{ker}(\alpha)$, is defined by
$$\text{ker}(\alpha)=\{k\in G\;|\;\alpha(G)=1\}\text{.}$$

## Theorem 1.

Let $G$ and $H$ be groups and $\alpha$ a homomorphism between them. Then
- $\alpha(G)$ is a subgroup of $H$, and
- $\text{ker}(\alpha)$ is a normal subgroup of $G$.

## Theorem 2.

$$\begin{align*}

&K\triangleleft G\;\wedge\;\phi:G\rightarrow G/K\\\\

\implies &K=\text{ker}(\phi)\text{.}

\end{align*}$$

## Theorem 3.

Let $G$ and $H$ be groups and $\alpha$ a homomorphism between them. Then $\alpha$ is one-to-one iff $\text{ker}(\alpha)=\{1\}$.

## Theorem 4.
*Isomorphism Theorem.*

Let $G$ and $H$ be groups and $\alpha$ a homomorphism between them. Then
$$\text{im}(\alpha)\cong G/\text{ker}(\alpha)\text{.}$$

## Reminder.

Let $G$ be a group and $a\in G$. Then the map
$$\sigma_{a}:G\rightarrow G;\;\sigma(g)=aga^{-1}$$
is called the *inner automorphism of $G$ about $a$*. Then the set $\text{inn}(G)$ is another set that we can define, each element being a set of $2$-tuples that model the inputs and outputs of $\sigma_a$. 

## Theorem 5.

$$G\text{ is a group }\implies G/Z(G)\cong\text{inn}(G)\text{.}$$