
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
