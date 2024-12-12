
Problem 1(a): When is a non-empty set a group? Give examples.

A non-empty set $G$ together with a binary operation $*$ is a group if and only if the following four axioms are satisfied:

1. **Closure:** For all $a, b \in G$, the result of the operation $a * b$ is also in $G$.  This ensures that the operation is well-defined on the set.

2. **Associativity:** For all $a, b, c \in G$, the order in which the operation is applied does not matter: $(a * b) * c = a * (b * c)$.

3. **Identity Element:** There exists a special element $1 \in G$, called the identity element (or unity), such that for every $a \in G$, $1 * a = a * 1 = a$.  The identity element acts neutrally under the operation.

4. **Inverse Elements:** For every $a \in G$, there exists an element $a^{-1} \in G$, called the inverse of $a$, such that $a * a^{-1} = a^{-1} * a = 1$.  The inverse "undoes" the operation.

If, in addition to these four axioms, the operation is commutative (that is, $a * b = b * a$ for all $a, b \in G$), the group is called an **abelian group**.

A group $G$ is called **cyclic** if there exists an element $g \in G$, called a generator, such that every element of $G$ can be expressed as a power of $g$ (written $g^k$ for some integer $k$ if the operation is written multiplicatively) or a multiple of $g$ (written $kg$ if the operation is additive).


Here are three examples of groups:

* **Cyclic Group:** $(\mathbb{Z}_4, +)$, the integers modulo 4 under addition.  This group is cyclic because the element 1 is a generator. We can obtain all elements of $\mathbb{Z}_4 = \{0, 1, 2, 3\}$ as multiples of 1 (modulo 4): 0 (0 * 1), 1 (1 * 1), 2 (2 * 1), 3 (3 * 1). Note that we use multiples because our group is under addition.

* **Abelian but Not Cyclic Group:** $(\mathbb{Z}_2 \times \mathbb{Z}_2, +)$, the Klein four-group under component-wise addition. This group is abelian because addition modulo 2 is commutative. It is not cyclic because there is no single element that generates the entire group. Each non-identity element generates a subgroup of order 2 (itself and the identity). $\mathbb{Z}_2 \times \mathbb{Z}_2 = \{(0,0), (1,0), (0,1), (1,1)\}$. Adding (1,0) to itself yields (0,0), so its order is two. Same for (0,1) and (1,1).

* **Non-Abelian Group:** $(S_3, \circ)$, the symmetric group on three elements under the operation of composition. $S_3$ consists of all permutations of the set {1, 2, 3}.  It is non-abelian because the operation of composition is not commutative. For example, $(1\;2) \circ (1\;3) = (1\;3\;2)$, while $(1\;3) \circ (1\;2) = (1\;2\;3)$, where we use cycle notation for permutations.




Problem 1(b): When is a non-empty subset *H* of a group *G* a subgroup? How many different subgroups does *S₃* have? Enumerate them.

A non-empty subset $H$ of a group $G$ is a subgroup of $G$ (denoted $H \le G$) if $H$ itself forms a group under the same operation as $G$.  This means $H$ must satisfy the four group axioms using the operation inherited from $G$.  

The **Subgroup Test** provides a more efficient way to check if a subset is a subgroup: A nonempty subset $H$ of $G$ is a subgroup if and only if:

1. The identity element of $G$ is in $H$.
2. For all $a, b \in H$, $a * b \in H$ ($H$ is closed under the operation of $G$).
3. For all $a \in H$, $a^{-1} \in H$ ($H$ is closed under taking inverses).

When $H$ is a finite set, the **Finite Subgroup Test** simplifies this even further: a nonempty finite subset $H$ of $G$ is a subgroup if and only if it is closed under the operation of *G*.


The symmetric group $S_3$ has six subgroups:

1. $\{\epsilon\}$ (The trivial subgroup, always a subgroup of any group)
2. $\{\epsilon, (1\;2)\}$
3. $\{\epsilon, (1\;3)\}$
4. $\{\epsilon, (2\;3)\}$
5. $\{\epsilon, (1\;2\;3), (1\;3\;2)\}$ (This is the alternating group $A_3$, consisting of all even permutations in $S_3$)
6. $S_3$ (Every group is a subgroup of itself)



Problem 1(c): When is $H$ a normal subgroup? How many normal subgroups of $S_3$ and $S_4$ respectively?

A subgroup $H$ of a group $G$ is called a **normal subgroup** (denoted $H \trianglelefteq G$) if the left and right cosets of $H$ are equal for every element in $G$.  That is, $gH = Hg$ for all $g \in G$. This is equivalent to the condition $gHg^{-1} = H$ for all $g \in G$ (meaning conjugating H by any element of G leaves H unchanged) or $gHg^{-1} \subseteq H$ for all $g \in G$.

An important result is that any subgroup of index 2 is normal.  That is, if $H \le G$ and $|G:H| = 2$ (meaning there are only two cosets of $H$ in $G$), then $H$ is a normal subgroup of $G$.


* **Normal Subgroups of $S_3$:**  $S_3$ has three normal subgroups:
    1. $\{\epsilon\}$ (The trivial subgroup is always normal)
    2. $A_3 = \{\epsilon, (1\;2\;3), (1\;3\;2)\}$ (Normal because it has index 2 in $S_3$: $|S_3| = 6$ and $|A_3| = 3$)
    3. $S_3$ itself (A group is always a normal subgroup of itself)

* **Normal Subgroups of $S_4$:** $S_4$ has four normal subgroups:
    1. $\{\epsilon\}$
    2. $K = \{\epsilon, (1\;2)(3\;4), (1\;3)(2\;4), (1\;4)(2\;3)\}$ (the Klein four-group). This is normal because conjugating any element of *K* by a permutation in *S₄* yields an element still in *K*.
    3. $A_4$ (the alternating group, normal because $|S_4:A_4|=2$).
    4. $S_4$.



Problem 1(d): Write down a group G, a normal subgroup K of G, and a subgroup H of G which is not normal.

We can use $S_3$ as our example here:

* **G:** $S_3$
* **K:** $A_3 = \{\epsilon, (1 2 3), (1 3 2)\}$. This is a normal subgroup of *S₃* because it has index 2.
* **H:** $\{\epsilon, (1 2)\}$.  This subgroup is not normal. For example, if we take $g=(1 3)$, then $(1\;3)H = \{(1\;3), (1\;2\;3)\}$, while $H(1\;3) = \{(1\;3), (1\;3\;2)\}$.  Since $gH \ne Hg$, $H$ is not normal in $S_3$.




Problem 1(e): If $H \trianglelefteq G$ and $|H|=2$, show that $H \subseteq Z(G)$.

Let $H$ be a normal subgroup of $G$ with $|H| = 2$. This means $H$ consists of the identity element $1$ and one other element, say $h$ ($h \ne 1$).  So $H = \{1, h\}$. Since the order of H is 2, h must have order 2; thus $h^2 = hh = 1$, or $h = h^{-1}$. 

Since $H$ is normal in $G$, we know that for any $g \in G$, $gHg^{-1} = H$. In particular, $ghg^{-1} \in H$ for all $g \in G$.
There are two possibilities:

1. $ghg^{-1} = 1$.  If this were true, then multiplying on the right by $g$ gives $gh=g$. By cancellation (multiplying on the left by $g^{-1}$), we have $h=1$.  But $h \ne 1$ by assumption, so this case cannot occur.

2. $ghg^{-1} = h$.  Multiplying on the right by $g$ gives $gh = hg$.

Since $gh=hg$ holds for all $g \in G$, we have that $h$ is in the center of $G$, denoted $Z(G)$. Therefore $H = \{1, h\} \subseteq Z(G)$, which is what we wanted to show.



# Group Theory and Ring Theory Problems and Solutions


## Problem 2(a): What is a cyclic group? Give examples.

A group $G$ is called **cyclic** if there exists an element $g \in G$, called a **generator**, such that every element of $G$ can be expressed as a power of $g$ (written $g^k$ for some integer $k$, when the group operation is denoted multiplicatively) or a multiple of $g$ (written $kg$, when the group operation is additive). We denote a cyclic group generated by g as $\langle g \rangle$.  In other words, $G = \langle g \rangle = \{g^k \mid k \in \mathbb{Z}\}$ (multiplicative notation) or $G = \langle g \rangle = \{kg \mid k \in \mathbb{Z}\}$ (additive notation).

Examples:

* **Finite Cyclic Group:** $(\mathbb{Z}_n, +)$, the integers modulo $n$ under addition, is a finite cyclic group. The element 1 is a generator, as every element $k \in \mathbb{Z}_n$ can be written as $k \cdot 1$ (modulo n). For example, consider $\mathbb{Z}_{6}=\{0, 1, 2, 3, 4, 5\}$:
$0 \equiv 0 \cdot 1 \pmod{6}$
$1 \equiv 1 \cdot 1 \pmod{6}$
$2 \equiv 2 \cdot 1 \pmod{6}$
$3 \equiv 3 \cdot 1 \pmod{6}$
$4 \equiv 4 \cdot 1 \pmod{6}$
$5 \equiv 5 \cdot 1 \pmod{6}$

* **Infinite Cyclic Group:** $(\mathbb{Z}, +)$, the integers under addition.  The element 1 is a generator since any integer $k$ can be represented as $k \cdot 1$, a multiple of 1. The group is infinite because all integer multiples of 1 are distinct elements.

* **Non-Cyclic Group:** The Klein four-group $K_4 = \{1, a, b, ab\}$, where $a^2 = b^2 = 1$ and $ab = ba$, is not cyclic. This is because no single element in $K_4$ generates the entire group. Each non-identity element generates a subgroup of order 2 (itself and the identity).


## Problem 2(b): State the Fundamental Theorem of Finite Cyclic Groups.

The Fundamental Theorem of Finite Cyclic Groups (Theorem 9 §2.4) describes the subgroups of a finite cyclic group:

Let $G = \langle g \rangle$ be a cyclic group of order $n$.
1. **Every subgroup of G is cyclic.**  More precisely, if $H$ is a subgroup of $G$, then $H = \langle g^d \rangle$ for some divisor $d$ of $n$.
2. **Unique Subgroups:** For each positive divisor $k$ of $n$, the group $G$ has exactly one subgroup of order $k$, namely $\langle g^{n/k} \rangle$. This means the subgroups of a finite cyclic group are in one-to-one correspondence with the divisors of the group order.


## Problem 2(c): Let $G$ be a finite cyclic group and $H$ be a subgroup of $G$. Show that $H$ is cyclic.

Let $G$ be a finite cyclic group of order $n$, say $G = \langle g \rangle$. This means $g^n = 1$ (multiplicative notation), and every element of $G$ can be written as $g^k$ for some $0 \le k < n$.
Let $H$ be a subgroup of $G$.  If $H = \{1\}$, then $H$ is trivially cyclic (generated by 1).  Suppose $H \ne \{1\}$. Consider the set $S = \{k \in \mathbb{Z}^+ \mid g^k \in H\}$. Since $H$ contains elements other than the identity and $G$ is cyclic, $S$ is a non-empty set of positive integers.

By the Well-Ordering Principle, $S$ contains a smallest positive integer, say $m$. We will show that $H = \langle g^m \rangle$, thus proving $H$ is cyclic.

* $\langle g^m \rangle \subseteq H$: Since $g^m \in H$ and $H$ is a subgroup, all powers of $g^m$ must also be in $H$, which means $\langle g^m \rangle \subseteq H$.

* $H \subseteq \langle g^m \rangle$: Let $g^k \in H$.  Using the division algorithm, we can write $k = qm + r$ for some integers $q$ and $r$ with $0 \le r < m$. Now
$g^k = g^{qm+r} = (g^m)^q g^r$.
Since $g^k \in H$ and $g^m \in H$ (and thus $(g^m)^q \in H$), we must have $g^r = (g^m)^{-q}g^k \in H$.  Since $0 \le r < m$ and $m$ was the *smallest* positive integer with $g^m \in H$, we must have $r=0$.  Therefore, $k=qm$, and $g^k = (g^m)^q \in \langle g^m \rangle$.  This proves $H \subseteq \langle g^m \rangle$.

Since $\langle g^m \rangle \subseteq H$ and $H \subseteq \langle g^m \rangle$, we have $H = \langle g^m \rangle$, proving that $H$ is cyclic.


## Problem 2(d): Write down the subgroup lattice of $\mathbb{Z}/12\mathbb{Z}$.

The group $\mathbb{Z}/12\mathbb{Z}$ (the integers modulo 12 under addition) is a cyclic group of order 12, often written as $\mathbb{Z}_{12}$. By the Fundamental Theorem of Finite Cyclic Groups, the subgroups of $\mathbb{Z}_{12}$ correspond to the divisors of 12, which are 1, 2, 3, 4, 6, and 12.  We use additive notation. Recall that each $x$ in $\mathbb{Z}/12\mathbb{Z}$ is actually a coset $12\mathbb{Z}+x$, and we write it as $\bar{x}$ for convenience.

The subgroups and their orders are:

* $\langle \bar{0} \rangle = \{\bar{0}\}$ (order 1)
* $\langle \bar{6} \rangle = \{\bar{0}, \bar{6}\}$ (order 2)
* $\langle \bar{4} \rangle = \{\bar{0}, \bar{4}, \bar{8}\}$ (order 3)
* $\langle \bar{3} \rangle = \{\bar{0}, \bar{3}, \bar{6}, \bar{9}\}$ (order 4)
* $\langle \bar{2} \rangle = \{\bar{0}, \bar{2}, \bar{4}, \bar{6}, \bar{8}, \bar{10}\}$ (order 6)
* $\langle \bar{1} \rangle = \mathbb{Z}_{12}$ (order 12)

The subgroup lattice diagram, where a line upwards indicates containment:

```tikz
\begin{tikzpicture}[scale=1.0, node distance=1.5cm] \node (G) {$\mathbb{Z}/12\mathbb{Z} = \langle 1 \rangle$}; \node (2) [below of=G] {$\langle 2 \rangle$}; \node (3) [below left of=2] {$\langle 3 \rangle$}; \node (4) [below right of=2] {$\langle 4 \rangle$}; \node (6) [below left of=4] {$\langle 6 \rangle$}; \node (0) [below of=6] {$\langle 0 \rangle$}; \draw (G) -- (2); \draw (2) -- (3); \draw (2) -- (4); \draw (3) -- (6); \draw (4) -- (6); \draw (6) -- (0); \end{tikzpicture}```
```tikz
\begin{document}
	\begin{tikzpicture}
		[scale=1.0, node distance=1.5cm] 
		\node (G) {$\mathbb{Z}/12\mathbb{Z} = \langle 1 \rangle$}; 
		\node (2) [below of=G] {$\langle 2 \rangle$}; 
		\node (3) [below left of=2] {$\langle 3 \rangle$}; 
		\node (4) [below right of=2] {$\langle 4 \rangle$}; 
		\node (6) [below left of=4] {$\langle 6 \rangle$}; 
		\node (0) [below of=6] {$\langle 0 \rangle$}; 
		\draw (G) -- (2); 
		\draw (2) -- (3); 
		\draw (2) -- (4); 
		\draw (3) -- (6); 
		\draw (4) -- (6); 
		\draw (6) -- (0); 
	\end{tikzpicture}
\end{document}
```
