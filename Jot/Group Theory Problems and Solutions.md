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


---


Problem 2(a): What is a cyclic group? Give examples.

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




Problem 2(b): State the Fundamental Theorem of Finite Cyclic Groups.

The Fundamental Theorem of Finite Cyclic Groups (Theorem 9 §2.4) describes the subgroups of a finite cyclic group:

Let $G = \langle g \rangle$ be a cyclic group of order $n$.
1. **Every subgroup of G is cyclic.**  More precisely, if $H$ is a subgroup of $G$, then $H = \langle g^d \rangle$ for some divisor $d$ of $n$.
2. **Unique Subgroups:** For each positive divisor $k$ of $n$, the group $G$ has exactly one subgroup of order $k$, namely $\langle g^{n/k} \rangle$. This means the subgroups of a finite cyclic group are in one-to-one correspondence with the divisors of the group order.




Problem 2(c): Let $G$ be a finite cyclic group and $H$ be a subgroup of $G$. Show that $H$ is cyclic.

Let $G$ be a finite cyclic group of order $n$, say $G = \langle g \rangle$. This means $g^n = 1$ (multiplicative notation), and every element of $G$ can be written as $g^k$ for some $0 \le k < n$.
Let $H$ be a subgroup of $G$.  If $H = \{1\}$, then $H$ is trivially cyclic (generated by 1).  Suppose $H \ne \{1\}$. Consider the set $S = \{k \in \mathbb{Z}^+ \mid g^k \in H\}$. Since $H$ contains elements other than the identity and $G$ is cyclic, $S$ is a non-empty set of positive integers.

By the Well-Ordering Principle, $S$ contains a smallest positive integer, say $m$. We will show that $H = \langle g^m \rangle$, thus proving $H$ is cyclic.

* $\langle g^m \rangle \subseteq H$: Since $g^m \in H$ and $H$ is a subgroup, all powers of $g^m$ must also be in $H$, which means $\langle g^m \rangle \subseteq H$.

* $H \subseteq \langle g^m \rangle$: Let $g^k \in H$.  Using the division algorithm, we can write $k = qm + r$ for some integers $q$ and $r$ with $0 \le r < m$. Now
$g^k = g^{qm+r} = (g^m)^q g^r$.
Since $g^k \in H$ and $g^m \in H$ (and thus $(g^m)^q \in H$), we must have $g^r = (g^m)^{-q}g^k \in H$.  Since $0 \le r < m$ and $m$ was the *smallest* positive integer with $g^m \in H$, we must have $r=0$.  Therefore, $k=qm$, and $g^k = (g^m)^q \in \langle g^m \rangle$.  This proves $H \subseteq \langle g^m \rangle$.

Since $\langle g^m \rangle \subseteq H$ and $H \subseteq \langle g^m \rangle$, we have $H = \langle g^m \rangle$, proving that $H$ is cyclic.




Problem 2(d): Write down the subgroup lattice of $\mathbb{Z}/12\mathbb{Z}$.

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
\node at (0,4) {Z/12Z = [1]};
\node at (0,3) {[2]};
\node at (-1,2) {[3]};
\node at (1,2) {[4]};
\node at (0,1) {[6]};
\node at (0,0) {[0]};
\draw (0,4) -- (0,3);
\draw (0,3) -- (-1,2);
\draw (0,3) -- (1,2);
\draw (-1,2) -- (0,1);
\draw (1,2) -- (0,1);
\draw (0,1) -- (0,0);
\end{tikzpicture}
\end{document}
```


---


Problem 3(a): What is a permutation group $S_n$? What is the parity of $\tau \in S_n$? $|S_n| =$ ?

A **permutation** of a set is a bijection (a one-to-one and onto function) from the set to itself.  The set of all permutations of the set $\{1, 2, ..., n\}$, denoted $S_n$, forms a group under the operation of function composition. This group is called the **symmetric group** of degree $n$.

The **parity** of a permutation $\tau \in S_n$ is a way of classifying permutations as either even or odd.  A permutation is **even** if it can be written as a product of an even number of transpositions (2-cycles), and **odd** if it can be written as a product of an odd number of transpositions.  The **Parity Theorem** (Theorem 7 §1.4) is crucial here; it states that the parity of a permutation is well-defined—a permutation cannot be both even and odd. This is a surprising result because a given permutation can be written as a product of transpositions in many ways.

The **order** of a group is the number of elements it contains.  The order of the symmetric group $S_n$ is given by $|S_n| = n!$. This is because there are $n$ choices for where to send 1, $n-1$ choices for where to send 2 (since it can't go to the same place as 1), and so on, down to 1 choice for where to send $n$.




Problem 3(b): What is $A_n$? $|A_n| =$ ?

The **alternating group** of degree $n$, denoted $A_n$, is the subgroup of $S_n$ consisting of all *even* permutations.  That is, $A_n$ contains all permutations in $S_n$ that can be expressed as a product of an even number of transpositions.  $A_n$ is a normal subgroup of $S_n$ because it has index 2 (for n>1), meaning $|S_n:A_n| = 2$.


The order of the alternating group is given by:
$|A_n| = \frac{n!}{2}$ for $n \ge 2$.  (Note that A₁ has only one element, the identity permutation; hence |*A₁*| = 1).




Problem 3(c): How to write a permutation in terms of a product of distinct cycles? Write $\tau = (1\;2\;3)(3\;5\;1\;6)$ as a product of disjoint cycles. What is the inverse of $\tau$? What is its order? Is it in $A_6$?

Any permutation can be written as a product of disjoint cycles.  **Disjoint cycles** are cycles that have no elements in common.  To decompose a permutation into disjoint cycles, follow these steps:

1. Start with the smallest element, say 1.
2. Determine where 1 is mapped under the permutation.
3. Determine where that element is mapped, and continue this process until you return to 1.  This completes one cycle.
4. If there are any elements not yet included in a cycle, choose the smallest such element and repeat steps 2 and 3.
5. Continue this process until all elements are included in a cycle.

The resulting product of disjoint cycles represents the original permutation. Disjoint cycles commute, so the order in which the cycles are written does not matter.


Now, let's apply this to $\tau = (1\;2\;3)(3\;5\;1\;6)$:

* 1 → 2 (from (1 2 3))
* 2 → 3 (from (1 2 3))
* 3 → 5 (from (3 5 1 6))
* 5 → 1 (from (3 5 1 6)).  This closes the first cycle: (1 2 3 5).

* 3 → 1 (from (1 2 3)), then 1 → 6 (from (3 5 1 6))
* 6 is fixed by (1 2 3) and goes to itself in (3 5 1 6). Thus, we have the cycle (6), which is equivalent to the identity permutation.

Therefore, $\tau$ as a product of disjoint cycles is (1 2 3 5).

* **Inverse of $\tau$:** To find the inverse of a permutation written as a product of disjoint cycles, simply reverse the order of the elements within each cycle. Thus, $\tau^{-1} = (5\;3\;2\;1)$.

* **Order of $\tau$:** The order of a permutation written as a product of disjoint cycles is the least common multiple (lcm) of the lengths of the cycles.  Since $\tau = (1\;2\;3\;5)$ is a single cycle of length 4, its order is $o(\tau) = \text{lcm}(4) = 4$.  This means $\tau^4 = \epsilon$, where ε is the identity permutation.

* **Is $\tau$ in $A_6$?** To determine if $\tau$ is in $A_6$ (the alternating group of degree 6), we check its parity. A cycle of length $r$ can be written as a product of $r-1$ transpositions.  Since $\tau = (1\;2\;3\;5)$ has length 4, it can be written as a product of $4-1=3$ transpositions:  (1 2)(2 3)(3 5). This is an odd number of transpositions, so $\tau$ is an odd permutation.  Since $A_6$ contains only even permutations, $\tau$ is *not* an element of $A_6$. We can also calculate the parity from the original product: $\tau = (1\;2\;3)(3\;5\;1\;6) = (1\;2)(2\;3)(3\;5)(5\;1)(1\;6)$, which is 5 transpositions, hence τ is odd.


---


Problem 4(a): Let $G$ and $H$ be groups, and $\alpha: G \to H$ be a map. Under what condition is $\alpha$ a homomorphism?

Let $(G, *)$ and $(H, \cdot)$ be groups, where $*$ and $\cdot$ represent their respective binary operations. A map (or function) $\alpha: G \to H$ is called a **homomorphism** if it preserves the group operation. More formally, $\alpha$ is a homomorphism if and only if:

$\alpha(a * b) = \alpha(a) \cdot \alpha(b)$  for all $a, b \in G$.

This means that performing the operation $*$ in $G$ and then applying the map $\alpha$ is the same as applying $\alpha$ to the elements first and then performing the operation $\cdot$ in $H$.  Homomorphisms are structure-preserving maps between groups.




Problem 4(b): What is the kernel of a homomorphism?

Let $\alpha: G \to H$ be a group homomorphism. The **kernel** of $\alpha$, denoted $\text{ker}(\alpha)$, is the set of all elements in $G$ that are mapped by $\alpha$ to the identity element $1_H$ of $H$.  Formally:

$\text{ker}(\alpha) = \{g \in G \mid \alpha(g) = 1_H \}$.

The kernel is a crucial concept in group theory.  It's not just a subset of $G$; it's a normal subgroup. This fact is part of Theorem 1 §2.10. The kernel measures the degree to which the homomorphism $\alpha$ fails to be injective (one-to-one). If the kernel contains only the identity element of $G$, then $\alpha$ is injective.




Problem 4(c): Describe one onto homomorphism from $S_3$ to $C_3$ and compute the kernel of this homomorphism.

Let $S_3$ be the symmetric group on three elements, and let $C_3 = \langle c \rangle = \{1, c, c^2\}$ be the cyclic group of order 3 (where $c^3 = 1$). We want to define a surjective (onto) homomorphism $\alpha: S_3 \to C_3$.

Recall that $S_3$ can be generated by $\sigma = (1\;2\;3)$ and $\tau = (1\;2)$ with the relations $\sigma^3 = \tau^2 = \epsilon$ (the identity permutation) and $\sigma \tau = \tau \sigma^2$.  A homomorphism from $S_3$ is determined by where it sends its generators.  Define $\alpha$ as follows:

* $\alpha(\sigma) = c$
* $\alpha(\tau) = 1$

We extend this definition to all elements of $S_3$:

* $\alpha(\epsilon) = 1$ (homomorphisms always map the identity to the identity)
* $\alpha(\sigma^2) = \alpha(\sigma)^2 = c^2$
* $\alpha(\tau\sigma) = \alpha(\tau)\alpha(\sigma) = 1 \cdot c = c$
* $\alpha(\tau\sigma^2) = \alpha(\tau)\alpha(\sigma^2) = 1 \cdot c^2 = c^2$.

This definition respects the relations of $S_3$:

* $\alpha(\sigma^3) = c^3 = 1 = \alpha(\epsilon)$
* $\alpha(\tau^2) = 1^2 = 1 = \alpha(\epsilon)$
* $\alpha(\sigma\tau) = c \cdot 1 = c$, and $\alpha(\tau\sigma^2) = 1 \cdot c^2 = c^2$. Since $\sigma \tau = \tau \sigma^2$, we must have $\alpha(\sigma\tau) = \alpha(\tau\sigma^2)$. In $S_3$, we have $\sigma\tau = (1\;2\;3)(1\;2) = (2\;3)$ and $\tau\sigma^2 = (1\;2)(1\;3\;2) = (1\;3)$. Their images are $c$ and $c^2$ respectively. $c = c^2$ doesn't hold, but the equation $\sigma\tau = \tau\sigma^2$ is equivalent to $\sigma\tau = \tau\sigma^{-1}$ so we need $\alpha(\sigma\tau)=\alpha(\tau\sigma^{-1})$, and indeed it does.

Since $\alpha$ maps the generators of $S_3$ to elements of $C_3$ and preserves the relations of $S_3$, it is a well-defined homomorphism.  It is surjective (onto) because both $c$ and $c^2$, the non-identity elements of $C_3$, are in the image of $\alpha$.

The kernel of $\alpha$ is the set of elements in $S_3$ that map to the identity in $C_3$:
$\text{ker}(\alpha) = \{\epsilon, \sigma, \sigma^2\} = A_3$.
As expected, the kernel is a normal subgroup of $S_3$.




Problem 4(d): What is an isomorphism?

An **isomorphism** is a bijective homomorphism between two groups (or rings, or other algebraic structures).  For groups, a map $\phi: G \to H$ is an isomorphism if:

1. $\phi$ is a homomorphism: $\phi(ab) = \phi(a)\phi(b)$ for all $a, b \in G$.
2. $\phi$ is injective (one-to-one): If $\phi(a) = \phi(b)$, then $a=b$.
3. $\phi$ is surjective (onto): For every $h \in H$, there exists a $g \in G$ such that $\phi(g) = h$.


If an isomorphism exists between $G$ and $H$, we say the groups are **isomorphic**, written $G \cong H$. Isomorphic groups have the same structure; they are essentially the same group with different labels for the elements.

For rings, the definition is analogous. A map $\sigma: R \to S$ between two rings R and S is a ring isomorphism if:
1. It is a bijection (one-to-one and onto)
2. It preserves both operations: $\sigma(r_1 + r_2) = \sigma(r_1) + \sigma(r_2)$ and  $\sigma(r_1r_2) = \sigma(r_1)\sigma(r_2)$ for all $r_1, r_2$ in R.




Problem 4(e): Is $S_3$ isomorphic to the Dihedral group $D_3 = \langle a, b \mid a^3 = b^2 = 1, aba = b \rangle$?

Yes, $S_3$ is isomorphic to $D_3$. We'll use their presentations to define an isomorphism.

$S_3 = \langle \sigma, \tau \mid \sigma^3 = \tau^2 = \epsilon, \sigma\tau = \tau\sigma^2 \rangle$, where $\sigma = (1\;2\;3)$ and $\tau = (1\;2)$.
$D_3 = \langle a, b \mid a^3 = b^2 = 1, aba = b \rangle$.

Define $\phi: S_3 \to D_3$ by:

* $\phi(\sigma) = a$
* $\phi(\tau) = b$

This mapping extends to a homomorphism because it preserves the relations:

* $\phi(\sigma^3) = a^3 = 1$
* $\phi(\tau^2) = b^2 = 1$
* $\phi(\sigma\tau) = ab$ and $\phi(\tau\sigma^2) = ba^2$. Since $aba=b$ in $D_3$, we have $ab = ba^{-1} = ba^2$.  Thus, $\phi(\sigma\tau) = \phi(\tau\sigma^2)$. The relation $\sigma\tau=\tau\sigma^2$ implies $\sigma\tau = \tau\sigma^{-1}$, so we need $\phi(\sigma)\phi(\tau) = \phi(\tau)\phi(\sigma)^{-1}$, which becomes $ab = ba^2 = ba^{-1}$.


We must show that $\phi$ is a bijection:

* **Injective (One-to-One):** Because $S_3$ and $D_3$ are finite and of the same order (6), it is enough to show that $\phi$ is surjective, as then a counting argument would imply that it must also be injective.

* **Surjective (Onto):** Every element of *D₃* can be written uniquely as *bᵏaᵐ*, where $0 \le k \le 1$ and $0 \le m \le 2$. These elements are distinct, and there are 2 * 3 = 6 of them which is the number of elements in *D₃*, so there are distinct elements 1, a, a², b, ba, ba² in *D₃*. The elements in the presentation of $S_3$ as $\epsilon, \sigma, \sigma^2, \tau, \tau\sigma, \tau\sigma^2$ have respective images 1, a, a², b, ba², ba under $\phi$. This shows every element in *D₃* has a preimage in *S₃*.

Since $\phi$ is a bijective homomorphism, it is an isomorphism, so $S_3 \cong D_3$.




Problem 4(f): Decide whether the map $\alpha: \mathbb{R} \to GL_2(\mathbb{R})$ given by $\alpha(r) = \begin{pmatrix} 1 & r \\ 0 & 1 \end{pmatrix}$ is a group isomorphism.

The map $\alpha$ is *not* an isomorphism $\mathbb{R} \to GL_2(\mathbb{R})$, although it is a homomorphism and is injective.

1. **Homomorphism:**
   $\alpha(r+s) = \begin{pmatrix} 1 & r+s \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & r \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & s \\ 0 & 1 \end{pmatrix} = \alpha(r)\alpha(s)$. So $\alpha$ is a homomorphism from $(\mathbb{R}, +)$ to $(GL_2(\mathbb{R}), \cdot)$.

2. **Injective (One-to-One):**
   If $\alpha(r) = \alpha(s)$, then $\begin{pmatrix} 1 & r \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & s \\ 0 & 1 \end{pmatrix}$, which clearly implies $r = s$.

3. **Surjective (Onto):** The map α is _not_ surjective. For any $r \in \mathbb{R}$, the determinant of $\alpha(r)$ is (1)(1)-(0)(r) = 1. Hence the image of $\mathbb{R}$ under alpha consists of $2 \times 2$ matrices of determinant one. $GL_2(\mathbb{R})$ contains matrices such as $\begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}$, which has determinant 2 and thus cannot be in the image of α. 

Since $\alpha$ is not surjective, it is not an isomorphism. However, it is an isomorphism from $\mathbb{R}$ to the subgroup of $GL_2(\mathbb{R})$ given by $S=\{\begin{pmatrix} 1 & r \\ 0 & 1 \end{pmatrix}\mid r\in\mathbb{R}\}$.
$\alpha: \mathbb{R} \to S$ *is* an isomorphism, as it is a homomorphism, injective, and clearly surjective onto $S$.




Problem 4(g): What is an automorphism of $G$? Give a non-trivial automorphism of $S_3$.

An **automorphism** of a group $G$ is an isomorphism from $G$ to itself.  It is a bijective map $\phi: G \to G$ that preserves the group operation: $\phi(ab) = \phi(a)\phi(b)$ for all $a, b \in G$.

Consider $S_3$ with generators $\sigma = (1\;2\;3)$ and $\tau = (1\;2)$.  A non-trivial automorphism $\phi: S_3 \to S_3$ can be defined by its action on the generators:

* $\phi(\sigma) = \sigma^2 = (1\;3\;2)$ (since $o(\phi(\sigma)) = o(\sigma) = 3$ by Theorem 4 §2.5)
* $\phi(\tau) = \tau = (1\;2)$ (since $o(\phi(\tau)) = o(\tau) = 2$ by Theorem 4 §2.5)


This extends to all of $S_3$ because every element can be expressed in terms of σ and τ. This defines the inner automorphism given by conjugation by (2 3): $\phi(x) = (2\;3)x(2\;3)^{-1}$. It is non-trivial because it's not the identity map. Another nontrivial automorphism can be defined by conjugation by (1 3).




Problem 4(h): State the Isomorphism Theorem for groups.

The **Isomorphism Theorem** (First Isomorphism Theorem) states:  If $\alpha: G \to H$ is a group homomorphism, then the image of $\alpha$ is isomorphic to the quotient group $G/\text{ker}(\alpha)$. Symbolically:

$\alpha(G) \cong G/\text{ker}(\alpha)$.


This theorem is fundamental in group theory, establishing a connection between homomorphisms, normal subgroups, and factor groups. It's used to show that two groups are isomorphic by constructing a homomorphism between them with a known kernel.


---


Problem 5(a): State Lagrange's Theorem.

**Lagrange's Theorem** is a fundamental result in finite group theory. It states: If $G$ is a finite group and $H$ is a subgroup of $G$, then the order of $H$ (denoted $|H|$) divides the order of $G$ (denoted $|G|$).  Furthermore, $|G|/|H| = |G:H|$, where $|G:H|$ represents the index of $H$ in $G$, which is the number of distinct right (or left) cosets of $H$ in $G$.

This theorem has profound implications. For instance, it immediately tells us that a group of prime order has only two subgroups: itself and the trivial subgroup. It restricts the possible sizes of subgroups.




Problem 5(b): Let $G = D_6 = \langle r, s \mid r^6 = s^2 = 1, rsr = s \rangle$ and $H = \langle r^2 \rangle$. Write down all right cosets of $H$ in $G$.

$D_6$ is the dihedral group of order 12, representing the symmetries of a regular hexagon.  It's generated by a rotation $r$ (by $2\pi/6$ radians) and a reflection $s$, satisfying the given relations.  The subgroup $H = \langle r^2 \rangle = \{1, r^2, r^4\}$ has order 3.  The elements of $D_6$ are $\{1, r, r^2, r^3, r^4, r^5, s, sr, sr^2, sr^3, sr^4, sr^5\}$.  A right coset of $H$ in $G$ has the form $Hx = \{hx \mid h \in H \}$ for some $x \in G$.

The right cosets of $H$ in $G$ are:

1. $H1 = H = \{1, r^2, r^4\}$
2. $Hr = \{r, r^3, r^5\}$
3. $Hs = \{s, sr^2, sr^4\}$
4. $Hsr = \{sr, sr^3, sr^5\}$

These cosets partition the group $G$. They are disjoint, and their union is all of G. You can verify this by using the defining relations of $D_6$ and the fact that distinct cosets are disjoint.




Problem 5(c): Show that $H$ is normal in $G$. Compute the Cayley table of the factor group $G/H$ using the cosets.

To show $H = \langle r^2 \rangle$ is normal in $G = D_6$, we can use the normality test: $H \trianglelefteq G$ if and only if $gHg^{-1} \subseteq H$ (or $gHg^{-1} = H$) for all $g \in G$. Since $r$ and $s$ generate $D_6$, it suffices to show that $rHr^{-1} = H$ and $sHs^{-1} = H$.

* $rHr^{-1} = \{rr^kr^{-1} \mid r^k \in H\} = \{r^k \mid r^k \in H\} = H$.
* The relation $rsr = s$ implies $sr = r^{-1}s = r^5s$.  Then $sr^2 = r^{-2}s = r^4s$, and similarly $sr^4 = r^2s$. Also $srs = r^{-1}$, so $s^{-1} = s$.
$sHs^{-1} = \{sr^{2k}s \mid k=0,1,2\}$. Because $sr^2s^{-1} = sr^2s = r^4$ and $sr^4s = r^2$, we have $sHs^{-1} = \{s1s, sr^2s, sr^4s\} = \{1, r^4, r^2\} = H$.

Since $r$ and $s$ generate $D_6$, and both normalize *H*, we have $H \trianglelefteq G$.


Now, let's compute the Cayley table for $G/H$. The cosets are $H$, $Hr$, $Hs$, and $Hsr$. The group operation in $G/H$ is defined by $(Hx)(Hy) = Hxy$.

|     |   H  |  Hr  |  Hs  | Hsr  |
|-----|------|------|------|------|
|  H  |   H  |  Hr  |  Hs  | Hsr  |
|  Hr  |  Hr  |   H  | Hsr  |  Hs  |
|  Hs  |  Hs  | Hsr  |   H  |  Hr  |
| Hsr  | Hsr  |  Hs  |  Hr  |   H  |


Example calculations:

* $(Hr)(Hr) = Hr^2 = H$ (since $r^2 \in H$)
* $(Hs)(Hsr) = Hsr^5 = Hr^{-1}s = Hrs$ so we need to show rs and sr⁵ are in the same coset. $H(rs) = \{rs, r^3s, r^5s\}$ and $H(sr^5) = \{sr^5, r^2sr^5=sr^3, r^4sr^5=sr\}$. Therefore, $(Hs)(Hsr) = Hsr$.
* $(Hs)(Hs) = Hs^2 = H1 = H$
* $(Hsr)(Hsr) = Hsr^5sr = Hs(r^5s)r = H(sr)r = H$ since $s^2=1$ and $sr=r^5s$

Since $|G/H| = 4$ and none of the elements except the identity $H$ has order 4, then $G/H$ is not cyclic and is hence $K_4$, which means $G/H \cong \mathbb{Z}_2 \times \mathbb{Z}_2$.




Problem 5(d): Suppose that $G$ has subgroups of orders 40 and 100. If $|G| \le 300$, determine $|G|$.

By Lagrange's Theorem, the order of a subgroup must divide the order of the group.  Therefore, if $G$ has subgroups of orders 40 and 100, then $|G|$ must be a multiple of both 40 and 100.  The least common multiple of 40 and 100 is:

lcm(40, 100) = lcm($2^3 \cdot 5$, $2^2 \cdot 5^2$) = $2^3 \cdot 5^2 = 200$.

Since $|G|$ must be a multiple of 200 and $|G| \le 300$, the only possibility is $|G| = 200$.




Problem 5(e): Show that $K = \{e,(1\;2)(3\;4),(1\;3)(2\;4),(1\;4)(2\;3)\}$ is normal in $S_4$. Determine the structure of $S_4/K$ using the Cayley table of $S_4/K$.

$K$ is the Klein four-group, a subgroup of $S_4$. To show that $K$ is normal in $S_4$ (denoted $K \trianglelefteq S_4$), we use the normality test. We must show that $\sigma K \sigma^{-1} \subseteq K$ for all $\sigma \in S_4$. Since the transpositions generate $S_4$, it suffices to verify this condition for transpositions.  Let $\sigma = (a\;b)$ be an arbitrary transposition.

Conjugating an element of $K$ by $(a\;b)$ amounts to interchanging $a$ and $b$ in the cycle notation (Lemma 3 §2.8). We'll demonstrate this explicitly for each element of $K$:

* $e$:  $(a\;b)e(a\;b)^{-1} = (a\;b)(a\;b) = e \in K$.
* $(1\;2)(3\;4)$: There are several cases to consider, depending on the values of $a$ and $b$:
    * If $a=1$ and $b=2$, then $(1\;2)(1\;2)(3\;4)(1\;2) = (3\;4)(1\;2) = (1\;2)(3\;4) \in K$.
    * If $a=1$ and $b=3$, then $(1\;3)(1\;2)(3\;4)(1\;3) = (2\;3)(1\;4) = (1\;4)(2\;3) \in K$.
    * If $a=1$ and $b=4$, then $(1\;4)(1\;2)(3\;4)(1\;4) = (2\;4)(1\;3) = (1\;3)(2\;4) \in K$.
    * The other cases are similar, always yielding an element of K.
* $(1\;3)(2\;4)$ and $(1\;4)(2\;3)$:  The calculations are analogous to those for $(1\;2)(3\;4)$, always resulting in an element of $K$.

Since conjugation by any transposition maps elements of $K$ back into $K$, and since transpositions generate $S_4$, we have $K \trianglelefteq S_4$.


Now we determine the structure of $S_4/K$. The order is $|S_4/K| = |S_4|/|K| = 24/4 = 6$. There are two groups of order 6 up to isomorphism: $C_6$ (cyclic) and $S_3$ (non-abelian). We will construct the Cayley table of $S_4/K$ to determine its structure.

We need to find representatives for the six cosets of $K$ in $S_4$.  Let's choose:

* $K_1 = K = \{e, (1\;2)(3\;4), (1\;3)(2\;4), (1\;4)(2\;3)\}$
* $K_2 = K(1\;2\;3) = \{(1\;2\;3), (1\;3\;4), (2\;4\;3), (1\;4\;2)\}$
* $K_3 = K(1\;3\;2) = \{(1\;3\;2), (1\;4\;3), (2\;3\;4), (1\;2\;4)\}$
* $K_4 = K(1\;2) = \{(1\;2), (3\;4), (1\;3\;2\;4), (1\;4\;2\;3)\}$
* $K_5 = K(1\;3) = \{(1\;3), (2\;4), (1\;2\;3\;4), (1\;4\;3\;2)\}$
* $K_6 = K(2\;3) = \{(2\;3), (1\;4), (1\;2\;4\;3), (1\;3\;4\;2)\}$


The Cayley table of *S₄/K* (using simplified notation *Kᵢ* for the cosets):

|     | *K₁* | *K₂* | *K₃* | *K₄* | *K₅* | *K₆* |
|-----|------|------|------|------|------|------|
| *K₁*| *K₁* | *K₂* | *K₃* | *K₄* | *K₅* | *K₆* |
| *K₂*| *K₂* | *K₃* | *K₁* | *K₅* | *K₆* | *K₄* |
| *K₃*| *K₃* | *K₁* | *K₂* | *K₆* | *K₄* | *K₅* |
| *K₄*| *K₄* | *K₆* | *K₅* | *K₁* | *K₃* | *K₂* |
| *K₅*| *K₅* | *K₄* | *K₆* | *K₂* | *K₁* | *K₃* |
| *K₆*| *K₆* | *K₅* | *K₄* | *K₃* | *K₂* | *K₁* |



Let $x = K(1\;2\;3) = K_2$ and $y = K(1\;2) = K_4$.  From the Cayley table:

* $x^2 = K_3$,  $x^3 = K_1$.  So $x$ has order 3.
* $y^2 = K_1$. So $y$ has order 2.
* $xy = K_5$. Thus, $xyx = K_5K_4 = K_3$, and therefore, $xyx = y$, so since every element in *S₄/K* is expressible in terms of *x* and *y* and *S₄/K* has order 6, *S₄/K* is isomorphic to *S₃*.  This is a presentation for *S₃*.


---


Problem 6(a): What is a ring, a commutative ring, a division ring, an integral domain, or a field? Give an example of a division ring which is not commutative. Give an example of an integral domain which is not a field.

* **Ring:** A ring $R$ is a set equipped with two binary operations, addition (+) and multiplication ($\cdot$), satisfying the following axioms:
    1. $(R, +)$ is an abelian group (closure, associativity, identity element 0, additive inverses).
    2. Multiplication is associative: $a \cdot (b \cdot c) = (a \cdot b) \cdot c$ for all $a, b, c \in R$.
    3. Distributive laws: $a \cdot (b + c) = a \cdot b + a \cdot c$ and $(b + c) \cdot a = b \cdot a + c \cdot a$ for all $a, b, c \in R$.
    4. Multiplicative identity (unity): There exists an element $1 \in R$ such that $1 \cdot a = a = a \cdot 1$ for all $a \in R$.

* **Commutative Ring:** A ring is commutative if its multiplication is commutative: $a \cdot b = b \cdot a$ for all $a, b \in R$.

* **Division Ring (Skew Field):** A division ring is a nonzero ring in which every nonzero element has a multiplicative inverse. That is, for every $a \in R$, $a \ne 0$, there exists $a^{-1} \in R$ such that $a \cdot a^{-1} = a^{-1} \cdot a = 1$.

* **Integral Domain:** An integral domain is a commutative ring with unity $1 \ne 0$ that has no zero divisors.  A zero divisor is a nonzero element $a$ such that there exists a nonzero element $b$ with $a \cdot b = 0$.

* **Field:** A field is a commutative division ring. That is, it is a commutative ring with unity $1 \ne 0$ in which every nonzero element has a multiplicative inverse.

* **Example of a Non-Commutative Division Ring:** The **quaternions**, denoted $\mathbb{H}$, form a non-commutative division ring.  $\mathbb{H} = \{a + bi + cj + dk \mid a, b, c, d \in \mathbb{R}\}$, where $i^2 = j^2 = k^2 = ijk = -1$.  Quaternion multiplication is non-commutative; for example, $ij = k$ but $ji = -k$. Every nonzero quaternion has a multiplicative inverse.

* **Example of an Integral Domain that is Not a Field:** The ring of integers $\mathbb{Z}$ is an integral domain because it is commutative, has unity 1, and has no zero divisors. However, it is not a field because most integers (e.g., 2) do not have multiplicative inverses in $\mathbb{Z}$.




Problem 6(b): Let $R = \mathbb{Z}/12\mathbb{Z}$. Find the characteristic and unit group of $R$. Find all idempotents ($e^2 = e$) of $R$. Is $R$ an integral domain?

* **Characteristic:** The characteristic of a ring $R$ is the smallest positive integer $n$ such that $n \cdot 1 = 0$, where 1 is the multiplicative identity of the ring. If no such positive integer exists, the characteristic is 0. In $\mathbb{Z}/12\mathbb{Z}$ (or $\mathbb{Z}_{12}$), we have $12 \cdot 1 \equiv 0 \pmod{12}$, and 12 is the smallest positive integer with this property. Thus, char($\mathbb{Z}_{12}$) = 12.

* **Unit Group:** The unit group of a ring $R$, denoted $R^\times$ or $U(R)$, is the set of all elements in $R$ that have multiplicative inverses. In $\mathbb{Z}_{12}$, an element $a$ has a multiplicative inverse if and only if gcd($a$, 12) = 1. The unit group is $U(\mathbb{Z}_{12}) = \{1, 5, 7, 11\}$. We can verify the inverses:
    * $1 \cdot 1 \equiv 1 \pmod{12}$
    * $5 \cdot 5 \equiv 25 \equiv 1 \pmod{12}$
    * $7 \cdot 7 \equiv 49 \equiv 1 \pmod{12}$
    * $11 \cdot 11 \equiv 121 \equiv 1 \pmod{12}$

* **Idempotents:** An idempotent $e$ is an element of a ring such that $e^2 = e$. In $\mathbb{Z}_{12}$, we seek $e$ such that $e^2 \equiv e \pmod{12}$, or $e^2 - e = e(e-1) \equiv 0 \pmod{12}$. This means $e(e-1)$ must be a multiple of 12. Checking the elements of $\mathbb{Z}_{12}$:
    * $0(0-1)=0$
    * $1(1-1)=0$
    * $4(4-1)=12$
    * $9(9-1)=72$

Therefore, the idempotents of $\mathbb{Z}_{12}$ are 0, 1, 4, and 9.

* **Integral Domain:** An integral domain is a commutative ring with unity $1 \ne 0$ and no zero divisors. $\mathbb{Z}_{12}$ is *not* an integral domain because it has zero divisors.  For example, $3 \cdot 4 = 12 \equiv 0 \pmod{12}$, but neither 3 nor 4 is 0 in $\mathbb{Z}_{12}$.




Problem 6(c): Let $R = \mathbb{Q}(\sqrt{2})$. Is it a field? Find the inverse of $1 + \sqrt{2}$ in $R$.

$\mathbb{Q}(\sqrt{2}) = \{a + b\sqrt{2} \mid a, b \in \mathbb{Q}\}$ is a field.

1. **Commutative Ring with Unity:**  $\mathbb{Q}(\sqrt{2})$ inherits the properties of a commutative ring with unity 1 from the field of real numbers.

2. **Inverses:** Let $x = a + b\sqrt{2}$ be a nonzero element of $\mathbb{Q}(\sqrt{2})$ (so $a$ and $b$ are not both zero). To find its inverse, we look for $y = c + d\sqrt{2}$ such that $xy = 1$.
$(a + b\sqrt{2})(c + d\sqrt{2}) = ac + 2bd + (ad + bc)\sqrt{2} = 1$.
This gives the equations: $ac + 2bd = 1$ and $ad + bc = 0$. Solving for $c$ and $d$, we get $c = a/(a^2 - 2b^2)$ and $d = -b/(a^2 - 2b^2)$.  Note that $a^2 - 2b^2 \ne 0$ because $a$ and $b$ are rational, and $\sqrt{2}$ is irrational (so $a^2 - 2b^2 = 0$ if and only if $a=b=0$, which we assumed is not the case). Thus, the inverse of $a + b\sqrt{2}$ is $\frac{a}{a^2-2b^2}-\frac{b}{a^2-2b^2}\sqrt{2}$ = $\frac{a - b\sqrt{2}}{a^2 - 2b^2}$.

Specifically, for $1 + \sqrt{2}$ (*a* = 1, *b* = 1), the inverse is $\frac{1 - \sqrt{2}}{1 - 2} = -1 + \sqrt{2}$.




Problem 6(d): Let $R = \mathbb{Q} \times \mathbb{Q}$ with component-wise operations. What is $R^\times$? Give two different idempotents of $R$.

* **Units ($R^\times$):**  An element $(a, b) \in \mathbb{Q} \times \mathbb{Q}$ has an inverse $(c, d)$ if and only if $(a, b)(c, d) = (ac, bd) = (1, 1)$. This happens if and only if $a \ne 0$ and $b \ne 0$. Thus, $R^\times = \mathbb{Q}^\times \times \mathbb{Q}^\times = \{(a, b) \mid a, b \in \mathbb{Q}, a \ne 0, b \ne 0 \}$.

* **Idempotents:** An element $(e_1, e_2)$ is idempotent if $(e_1, e_2)^2 = (e_1^2, e_2^2) = (e_1, e_2)$. This requires $e_1^2 = e_1$ and $e_2^2 = e_2$ in $\mathbb{Q}$. The only idempotents in $\mathbb{Q}$ are 0 and 1.  Thus, the idempotents in $R$ are (0, 0), (1, 0), (0, 1), and (1, 1). Two distinct idempotents are (1, 0) and (0, 1).




Problem 6(e): Let $\mathbb{H} = \{a+bi+cj+dk \mid a,b,c,d \in \mathbb{R}, i^2 = j^2 = k^2 = ijk = -1\}$. Is $\mathbb{H}$ a ring, a division ring, an integral domain? Give two different idempotents of $\mathbb{H}$. Compute $(1+i+j+k)^2$, $(1-3i+k)(2+j)$, and $(2+j)(1-3i+k)$. What is the inverse of $1+2i-2k$?

* **Ring:** $\mathbb{H}$ is a ring. (See the detailed explanation in the previous response).

* **Division Ring:** $\mathbb{H}$ is a division ring because every nonzero quaternion has an inverse.  If $q = a + bi + cj + dk \ne 0$, then $q^{-1} = \frac{a - bi - cj - dk}{a^2 + b^2 + c^2 + d^2}$, which is also a quaternion.

* **Integral Domain:**  $\mathbb{H}$ is *not* an integral domain because it is not commutative.  For example, $ij = k$, but $ji = -k$.

* **Idempotents:**  0 and 1 are always idempotents.  Finding other idempotents requires solving a system of equations, generally.

* **Computations:**
    * $(1+i+j+k)^2 = 1 + i + j + k + i - 1 + k - j + j - k - 1 + i + k - i + j - 1 = -2 + 2i + 2j + 2k$
    * $(1-3i+k)(2+j) = 2 + j - 6i - 3ij + 2k + kj = 2 + j - 6i - 3k + 2k - i = 2 - 7i + j - k$
    * $(2+j)(1-3i+k) = 2 - 6i + 2k + j -3ji + jk = 2 - 6i + 2k + j + 3k + i = 2 - 5i + j + 5k$

* **Inverse of $1+2i-2k$:**  For $q = 1+2i-2k$, we have $a=1, b=2, c=0, d=-2$. Thus $|q|^2 = 1^2 + 2^2 + 0^2 + (-2)^2 = 9$. So the inverse is: $(1-2i+2k)/9 = \frac{1}{9} - \frac{2}{9}i + \frac{2}{9}k$.