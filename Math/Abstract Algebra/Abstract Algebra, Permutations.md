
### Example 1.

List the elements of $S_3$ in matrix notation.
#### Solution.

$\begin{pmatrix}1 & 2 & 3\\1&2&3\end{pmatrix},\begin{pmatrix}1 & 2 & 3\\1&3&2\end{pmatrix},\begin{pmatrix}1 & 2 & 3\\3&1&2\end{pmatrix},\begin{pmatrix}1 & 2 & 3\\2&1&3\end{pmatrix},\begin{pmatrix}1 & 2 & 3\\3&2&1\end{pmatrix},\begin{pmatrix}1 & 2 & 3\\2&3&1\end{pmatrix}$

## Theorem 1.

$|S_n|=n!$
### Example 2.

If $\sigma=\begin{pmatrix}1&2&3&4\\3&4&1&2\end{pmatrix}$ and $\tau =\begin{pmatrix}1&2&3&4\\2&4&3&1\end{pmatrix}$, then compute $\sigma\tau$.

#### Solution.

$\sigma\tau = \begin{pmatrix}1&2&3&4\\3&4&1&2\end{pmatrix}\begin{pmatrix}1&2&3&4\\2&4&3&1\end{pmatrix}=\begin{pmatrix}1&2&3&4\\4&2&1&3\end{pmatrix}$

### Example 3.

If $\sigma =\begin{pmatrix}1&2&3&4&5&6&7&8\\4&1&8&3&2&5&6&7\end{pmatrix}$, then find $\sigma^{-1}$.
#### Solution.

Switch the rows, then put the columns in order. 

$\begin{align*}\sigma^{-1}& =\begin{pmatrix}1&2&3&4&5&6&7&8\\4&1&8&3&2&5&6&7\end{pmatrix}^{-1}\\&=\begin{pmatrix}4&1&8&3&2&5&6&7\\1&2&3&4&5&6&7&8\end{pmatrix}\\&=\begin{pmatrix}1&2&3&4&5&6&7&8\\2&5&4&1&6&7&8&3\end{pmatrix}\end{align*}$

## Theorem 2.

$\begin{align*}(\forall (\sigma,\tau,\mu)\in S_n^3)(&\sigma\tau\in S_n\\\wedge\;&\sigma\epsilon=\sigma=\epsilon\sigma\\\wedge\;&\sigma(\tau\mu)=(\sigma\tau)\mu\\\wedge\;&\sigma\sigma^{-1}=\epsilon=\sigma^{-1}\sigma)\end{align*}$

### Example 4.

Given $\sigma=\begin{pmatrix}1&2&3&4&5\\4&5&1&2&3\end{pmatrix}$ and $\tau=\begin{pmatrix}1&2&3&4&5\\3&2&1&5&4\end{pmatrix}$, find $\chi\in S_5$ such that $\chi\sigma=\tau$.

#### Solution.

$\begin{align*}\chi\sigma=\tau\iff& \chi\sigma\sigma^{-1}=\tau\sigma^{-1}\\\iff&\chi=\tau\sigma^{-1}\\=&\begin{pmatrix}1&2&3&4&5\\3&2&1&5&4\end{pmatrix}\begin{pmatrix}1&2&3&4&5\\4&5&1&2&3\end{pmatrix}^{-1}\\=&\begin{pmatrix}1&2&3&4&5\\3&2&1&5&4\end{pmatrix}\begin{pmatrix}1&2&3&4&5\\3&4&5&1&2\end{pmatrix}\\\iff&\chi=\begin{pmatrix}1&2&3&4&5\\1&5&4&3&2\end{pmatrix}\end{align*}$

## Definition.

**Background.** 

**(i)** Given $X_n=\{1,2,\dots n\}$, recall that a permutation is an invertible map of every $k$, where $1\leq k\leq n$, to some $\sigma(k)\in X_n$. 
**(ii)** For a given $k\in X_n$ and a permutation $\sigma$, the map $\sigma$ *fixes* $k$ iff $\sigma(k)=k$. Otherwise, if $\sigma(k)\neq k$, then the map $\sigma$ *moves* $k$.

**Statement.**

**(1)** For a given $X_n$ and a permutation $\sigma\in S_n$, define the $\sigma$-moving set as
$$M(X_n,\;\sigma)=\left\{k\in X_n\;|\;\sigma k\neq k\right\}$$
**(2)** A pair of permutations $(n,\;\sigma,\;\tau)\in\mathbb{N}\times S_n^2$ is called "disjoint" if
$$M(X_n,\;\sigma)\;\cap\;M(X_n,\;\tau)=\varnothing$$

## Lemma 1.

$k\in M(X_n,\;\sigma)\implies \sigma(k)\in M(X_n,\;\sigma)$

## Theorem 3.

$(\forall(n,\;\sigma,\;\tau)\in\mathbb{N}\times S_n^2)(M(X_n,\;\sigma)\;\cap\;M(X_n,\;\tau)=\varnothing\implies \sigma\tau=\tau\sigma)$

## Example 5.

Write the following in cycle notation:
$$\begin{pmatrix}1&2&3&4&5&6&7\\4&7&1&6&5&2&3\end{pmatrix}$$
**Solution.** $(1\;4\;6\;2\;7\;3)$

## Example 6.

Write $S_3$ in cycle notation.

**Solution.** Starting with matrix notation,
$$\begin{align*}S_3 &= \bigg\{\begin{pmatrix}1&2&3\\1&2&3\end{pmatrix},\;\begin{pmatrix}1&2&3\\2&1&3\end{pmatrix},\;\begin{pmatrix}1&2&3\\3&1&2\end{pmatrix},\;\begin{pmatrix}1&2&3\\1&3&2\end{pmatrix},\;\begin{pmatrix}1&2&3\\2&3&1\end{pmatrix},\;\begin{pmatrix}1&2&3\\3&2&1\end{pmatrix}\bigg\}\\&=\{\epsilon,\;(1\;2),\;(1\;3\;2),\;(2\;3),\;(1\;3)\}\end{align*}$$

## Theorem 4.

$\begin{align*}\sigma&=(k_1\;k_2\;\dots\;k_{r-1}\;k_r)\\\iff\sigma^{-1}&=(k_r\;k_{r-1}\;\dots\;k_2\;k_1)\end{align*}$

## Example 8.

Write the following as a product of disjoint cycles:
$$\begin{pmatrix}1&2&3&4&5&6&7&8&9&10&11&12&13\\5&12&2&1&9&11&4&3&7&10&13&8&6\end{pmatrix}$$
**Solution.** $(1\;5\;9\;7\;4)(2\;12\;8\;3)(6\;11\;13)$

## Theorem 5.

If $\sigma\in S_n\setminus\{\epsilon\}$, then $\sigma$ is a product of disjoint $(>2$)-cycles.

### Example 9.

Write $S_4$ as a product of disjoint cycles. 

**Solution.** In matrix notation,
$$\begin{align*}S_4=\bigg\{&\begin{pmatrix}1&2&3&4\\1&2&3&4\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\1&2&4&3\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\1&3&2&4\end{pmatrix},\\&\begin{pmatrix}1&2&3&4\\1&3&4&2\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\1&4&2&3\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\1&4&3&2\end{pmatrix},\\&\begin{pmatrix}1&2&3&4\\2&1&3&4\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\2&1&4&3\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\2&3&1&4\end{pmatrix},\\&\begin{pmatrix}1&2&3&4\\2&3&4&1\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\2&4&1&3\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\2&4&3&1\end{pmatrix},\\&\begin{pmatrix}1&2&3&4\\3&1&2&4\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\3&1&4&2\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\3&2&1&4\end{pmatrix},\\&\begin{pmatrix}1&2&3&4\\3&2&4&1\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\3&4&1&2\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\3&4&2&1\end{pmatrix},\\&\begin{pmatrix}1&2&3&4\\4&1&2&3\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\4&1&3&2\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\4&2&1&3\end{pmatrix},\\&\begin{pmatrix}1&2&3&4\\4&2&3&1\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\4&3&1&2\end{pmatrix},\;\begin{pmatrix}1&2&3&4\\4&3&2&1\end{pmatrix}\bigg\}\end{align*}$$
Writing each as a product of disjoint cycles,
$$\begin{align*}S_4=\{&\epsilon,\;(3\;4),\;(2\;3),\;(2\;3\;4),\;(2\;4\;3),\;(2\;4),\;(1\;2),\\&(1\;2)(3\;4),\;(1\;2\;3),\;(1\;2\;3\;4),\;(1\;2\;4\;3),\\&(1\;2\;4),\;(1\;3\;2),\;(1\;3\;4\;2),\;(1\;3),\;(1\;3\;4),\\&(1\;3)(2\;4),\;(1\;3\;2\;4),\;(1\;4\;3\;2),\;(1\;4\;2),\\&(1\;4\;3),\;(1\;4),\;(1\;4\;2\;3),\;(1\;4)(2\;3)\}\end{align*}$$

## Theorem 6.

Every $r$-cycle is a product of $(r-1)$ cycles of length $2$, taking the form
$$(k_1\;k_2\;\dots\;k_{r-1}\;k_r)=(k_1\;k_2)(k_2\;k_3)\;\dots\;(k_{r-2}\;k_{r-1})(k_{r-1}\;k_r)$$
## Definition.

Two integers $m,n\in\mathbb{Z}$ are said to have the same parity if 
$$m\equiv n\mod 2$$

## Theorem 7.

If:

**(1)** $(m,n)\in\mathbb{Z}_{m\neq n}$ 
**(2)** $\sigma$ is a permutation
**(3)** $\gamma_1,\mu_1,\gamma_2,\mu_2,\dots\gamma_m,\dots\mu_n$ are transpositions 
**(4)** $\sigma=\gamma_1\gamma_2\dots\gamma_m=\mu_1\mu_2\dots\mu_n$

Then $m$ and $n$ have the same parity.

### Example 10.

Determine the parity of $\begin{pmatrix}1&2&3&4&5&6&7&8&9\\5&4&6&1&7&8&2&9&3\end{pmatrix}$.

**Solution.** The permutation $\begin{pmatrix}1&2&3&4&5&6&7&8&9\\5&4&6&1&7&8&2&9&3\end{pmatrix}$ is the product of the disjoint cycles $(1\;5\;7\;2\;4)(3\;6\;8\;9)$; decomposing, we get $(1\;5)(5\;7)(7\;2)(2\;4)(3\;6)(6\;8)(8\;9)$, which has $7$ terms. Since $7\equiv 1\mod 2$, the permutation has odd parity. 

## Theorem 8.

Let $A_n$ be the subset of $S_n$ that is comprised of the permutations in $S_n$ that are of even parity. The following is true of $A_n$:

**(1)** $\epsilon\in A_n$
**(2)** $(\sigma,\;\tau)\in A_n^2\implies (\sigma^{-1},\;\sigma\tau)\in A_n^2$
**(3)** $|A_n|=\frac{1}{2}n!$

## Exercises.

**(1)** Let 
$$\begin{align*}
\sigma&=\begin{pmatrix}1&2&3&4&5\\2&1&4&3&5\end{pmatrix}\text{,}\\
\tau&=\begin{pmatrix}1&2&3&4&5\\3&2&1&5&4\end{pmatrix}\text{,}\\
\mu&=\begin{pmatrix}1&2&3&4&5\\3&4&5&1&2\end{pmatrix}\text{.}\\
\end{align*}$$
Then
$$\begin{align*}

\tau\sigma&=\begin{pmatrix}1&2&3&4&5\\3&2&1&5&4\end{pmatrix}\begin{pmatrix}1&2&3&4&5\\2&1&4&3&5\end{pmatrix}\\
&=\begin{pmatrix}1&2&3&4&5\\4&1&2&5&3\end{pmatrix}\text{,}\\

\sigma\tau&=\begin{pmatrix}1&2&3&4&5\\2&1&4&3&5\end{pmatrix}\begin{pmatrix}1&2&3&4&5\\3&2&1&5&4\end{pmatrix}\\&=\begin{pmatrix}1&2&3&4&5\\2&3&5&1&4\end{pmatrix}\text{,}\\

\tau^{-1}&=\begin{pmatrix}1&2&3&4&5\\3&2&1&5&4\end{pmatrix}^{-1}\\&=\begin{pmatrix}1&2&3&4&5\\3&2&1&5&4\end{pmatrix}\\

\mu^{-1}&=\begin{pmatrix}1&2&3&4&5\\3&4&5&1&2\end{pmatrix}^{-1}\\&=\begin{pmatrix}1&2&3&4&5\\4&5&1&2&3\end{pmatrix}\\

\mu\tau\sigma^{-1}&=
\begin{pmatrix}1&2&3&4&5\\3&4&5&1&2\end{pmatrix}
\begin{pmatrix}1&2&3&4&5\\3&2&1&5&4\end{pmatrix}
\begin{pmatrix}1&2&3&4&5\\2&1&4&3&5\end{pmatrix}^{-1}
\\&=
\begin{pmatrix}1&2&3&4&5\\3&4&5&1&2\end{pmatrix}
\begin{pmatrix}1&2&3&4&5\\3&2&1&5&4\end{pmatrix}
\begin{pmatrix}1&2&3&4&5\\2&1&4&3&5\end{pmatrix}
\\&=
\begin{pmatrix}1&2&3&4&5\\2&5&3&4&1\end{pmatrix}\\

\mu^{-1}\sigma\tau&=\begin{pmatrix}1&2&3&4&5\\4&5&1&2&3\end{pmatrix}\begin{pmatrix}1&2&3&4&5\\2&3&5&1&4\end{pmatrix}
\\&=
\begin{pmatrix}1&2&3&4&5\\1&4&2&3&5\end{pmatrix}

\end{align*}$$

**(2a)** Let
$$\begin{align*}

\sigma&=\begin{pmatrix}1&2&3&4\\4&3&2&1\end{pmatrix}\text{,}\\

\tau&=\begin{pmatrix}1&2&3&4\\2&4&1&3\end{pmatrix}\text{, and}\\

\mu&=\begin{pmatrix}1&2&3&4\\3&1&4&2\end{pmatrix}\text{.}

\end{align*}$$
We will verify that any two of them commute. The set of all possible two-pairs are
$$\{\{\sigma,\tau\},\{\sigma,\mu\},\{\tau,\mu\}\}\text{.}$$
We check each of the pairs:
$$\begin{align*}

\sigma\tau&=\begin{pmatrix}1&2&3&4\\4&3&2&1\end{pmatrix}\begin{pmatrix}1&2&3&4\\2&4&1&3\end{pmatrix}
\\&=
\begin{pmatrix}1&2&3&4\\3&1&4&2\end{pmatrix}\\

\tau\sigma&=\begin{pmatrix}1&2&3&4\\2&4&1&3\end{pmatrix}\begin{pmatrix}1&2&3&4\\4&3&2&1\end{pmatrix}
\\&=
\begin{pmatrix}1&2&3&4\\3&1&4&2\end{pmatrix}\\

\sigma\mu&=\begin{pmatrix}1&2&3&4\\4&3&2&1\end{pmatrix}\begin{pmatrix}1&2&3&4\\3&1&4&2\end{pmatrix}
\\&=
\begin{pmatrix}1&2&3&4\\2&4&1&3\end{pmatrix}\\

\mu\sigma&=\begin{pmatrix}1&2&3&4\\3&1&4&2\end{pmatrix}\begin{pmatrix}1&2&3&4\\4&3&2&1\end{pmatrix}
\\&=
\begin{pmatrix}1&2&3&4\\2&4&1&3\end{pmatrix}\\

\tau\mu&=\begin{pmatrix}1&2&3&4\\2&4&1&3\end{pmatrix}\begin{pmatrix}1&2&3&4\\3&1&4&2\end{pmatrix}
\\&=
\begin{pmatrix}1&2&3&4\\1&2&3&4\end{pmatrix}\\

\mu\tau&=\begin{pmatrix}1&2&3&4\\3&1&4&2\end{pmatrix}\begin{pmatrix}1&2&3&4\\2&4&1&3\end{pmatrix}
\\&=
\begin{pmatrix}1&2&3&4\\1&2&3&4\end{pmatrix}

\end{align*}$$
**(2b)** We can start by verifying that 
$$\sigma=\begin{pmatrix}1&2&3&4\\4&3&2&1\end{pmatrix}\text{,}$$
and 
$$\begin{align*}\tau^2&=\begin{pmatrix}1&2&3&4\\2&4&1&3\end{pmatrix}\begin{pmatrix}1&2&3&4\\2&4&1&3\end{pmatrix}\\&=\begin{pmatrix}1&2&3&4\\4&3&2&1\end{pmatrix}\\&=\sigma\text{.}\end{align*}$$
Then, we can show that 
$$\mu=\begin{pmatrix}1&2&3&4\\3&1&4&2\end{pmatrix}\text{,}$$
and 
$$
\begin{align*}

\tau^3&=
\begin{pmatrix}1&2&3&4\\2&4&1&3\end{pmatrix}
\begin{pmatrix}1&2&3&4\\2&4&1&3\end{pmatrix}
\begin{pmatrix}1&2&3&4\\2&4&1&3\end{pmatrix}
\\&=
\begin{pmatrix}1&2&3&4\\3&1&4&2\end{pmatrix}
\\&=\mu\text{,}
\end{align*}
$$
which completes our initial verification. Now, recall that the pair sets whose commutativity we need to prove are
$$\{\{\sigma,\tau\},\{\sigma,\mu\},\{\tau,\mu\}\}\text{,}$$
using $\sigma=\tau^2$ and $\mu=\tau^3$.

**(i)**

$$\begin{align*}

&\sigma\tau=\tau\sigma
\\\iff&
\tau^2\tau=\tau\tau^2
\\\iff&
\tau^3=\tau^3

\end{align*}$$

**(ii)**

$$\begin{align*}

&
\sigma\mu=\mu\sigma
\\\iff&
\sigma\tau^3=\tau^3\sigma
\\\iff&
\tau^2\tau^3=\tau^3\tau^2
\\\iff&
\tau^5=\tau^5

\end{align*}$$

**(iii)**

$$\begin{align*}

&
\tau\mu=\mu\tau
\\\iff&
\tau\tau^3=\tau^3\tau
\\\iff&
\tau^4=\tau^4

\end{align*}$$

Note: All completed exercises done above may be inaccurate; these were done at a time when I think I was computing the permutations in a different direction. 

**(3)** Let 
$$\begin{align*}

\sigma=\begin{pmatrix}1&2&4&3\end{pmatrix}\text{, and }\tau=\begin{pmatrix}1&3\end{pmatrix}\begin{pmatrix}2&4\end{pmatrix}\text{.}

\end{align*}$$
In **(a-f)**, we solve for $\chi$.

**(a)**. 

$$\begin{align*}

&\sigma\chi=\tau\\
\iff & \chi=\sigma^{-1}\tau\\\\
\iff & \chi=\begin{pmatrix}1&2&4&3\end{pmatrix}^{-1}\begin{pmatrix}1&3\end{pmatrix}\begin{pmatrix}2&4\end{pmatrix}\\\\
\iff &\chi=\begin{pmatrix}3&4&2&1\end{pmatrix}\begin{pmatrix}1&3\end{pmatrix}\begin{pmatrix}2&4\end{pmatrix}\\\\
\iff &\chi=\begin{pmatrix}1&4\end{pmatrix}

\end{align*}$$

**(b)**. 

$$\begin{align*}

&\chi\tau=\sigma\\
\iff & \chi=\sigma\tau^{-1}\\\\
\iff &\chi=\begin{pmatrix}1&2&4&3\end{pmatrix}\big[\begin{pmatrix}1&3\end{pmatrix}\begin{pmatrix}2&4\end{pmatrix}\big]^{-1}\\\\
\iff &\chi=\begin{pmatrix}1&2&4&3\end{pmatrix}\begin{pmatrix}3&1\end{pmatrix}\begin{pmatrix}2&4\end{pmatrix}\\\\
\iff &\chi=\begin{pmatrix}2&3\end{pmatrix}

\end{align*}$$

**(c)**.

$$\begin{align*}

&\sigma^{-1}\chi=\tau\\
\iff & \chi=\sigma\tau\\
\iff & \chi=\begin{pmatrix}1&2&4&3\end{pmatrix}\begin{pmatrix}1&3\end{pmatrix}\begin{pmatrix}2&4\end{pmatrix}\\
\iff &\chi=\begin{pmatrix}2&3\end{pmatrix}

\end{align*}$$

**(d)**.

$$\begin{align*}

&\chi\tau\sigma=\epsilon\\
\iff & \chi=\sigma^{-1}\tau^{-1}\\
\iff & \chi=\sigma^{-1}\tau\text{ (tau is composed of disjoint transpositions)}\\
\iff & \chi=\begin{pmatrix}1&4\end{pmatrix}


\end{align*}$$

**(e)**.

$$\begin{align*}

&\tau\chi\sigma=\epsilon\\
\iff & \chi=\tau^{-1}\sigma^{-1}\\
\iff & \chi=\begin{pmatrix}1&3\end{pmatrix}\begin{pmatrix}2&4\end{pmatrix}\begin{pmatrix}3&4&2&1\end{pmatrix}\\
\iff & \chi= \begin{pmatrix}2&3\end{pmatrix}\begin{pmatrix}3&2\end{pmatrix}\\
\iff & \chi=\begin{pmatrix}2&3\end{pmatrix}

\end{align*}$$

**(f)**.

$$\begin{align*}

&\tau\chi\sigma^{-1}=\sigma\\
\iff & \chi=\tau^{-1}\sigma^{2}\\
\iff & \chi=\begin{pmatrix}1&3\end{pmatrix}\begin{pmatrix}2&4\end{pmatrix}\begin{pmatrix}1&2&4&3\end{pmatrix}\begin{pmatrix}1&2&4&3\end{pmatrix}\\
\iff &\chi=\begin{pmatrix}1&2\end{pmatrix}\begin{pmatrix}3&4\end{pmatrix}

\end{align*}$$

**(4)**. If $\tau\sigma=\begin{pmatrix}1&5&2&3\end{pmatrix}$, $\sigma\tau=\begin{pmatrix}1&2&4&5\end{pmatrix}$, and $\sigma(1)=2$, then find $\sigma$ and $\tau$.

**Solution**. The extractable facts from the assumptions are given in a table:

| The expression... | Is equal to... |
| ----------------- | -------------- |
| $\tau(\sigma(1))$ | $5$            |
| $\tau(\sigma(2))$ | $3$            |
| $\tau(\sigma(3))$ | $1$            |
| $\tau(\sigma(5))$ | $2$            |
| $\sigma(\tau(1))$ | $2$            |
| $\sigma(\tau(2))$ | $4$            |
| $\sigma(\tau(4))$ | $5$            |
| $\sigma(\tau(5))$ | $1$            |

With the assumption that $\sigma(1)=2$, we can simplify the table:

| The expression... | Is equal to... |
| ----------------- | -------------- |
| $\tau(2)$         | $5$            |
| $\tau(\sigma(2))$ | $3$            |
| $\tau(\sigma(3))$ | $1$            |
| $\tau(\sigma(5))$ | $2$            |
| $\sigma(\tau(1))$ | $2$            |
| $\sigma(\tau(2))$ | $4$            |
| $\sigma(\tau(4))$ | $5$            |
| $\sigma(\tau(5))$ | $1$            |

And then we now have a new piece of information that allows us to fill in more of the table. Repeating this process, we end up with the table:

| The expression... | Is equal to... |
| ----------------- | -------------- |
| $\tau(2)$         | $5$            |
| $\tau(5)$         | $3$            |
| $\tau(1)$         | $1$            |
| $\tau(4)$         | $2$            |
| $\sigma(1)$       | $2$            |
| $\sigma(5)$       | $4$            |
| $\sigma(2)$       | $5$            |
| $\sigma(3)$       | $1$            |

And now, only possible row remains for both of the mappings in the full table:

| The expression... | Is equal to... |
| ----------------- | -------------- |
| $\tau(1)$         | $1$            |
| $\tau(2)$         | $5$            |
| $\tau(3)$         | $4$            |
| $\tau(4)$         | $2$            |
| $\tau(5)$         | $3$            |
| $\sigma(1)$       | $2$            |
| $\sigma(2)$       | $5$            |
| $\sigma(3)$       | $1$            |
| $\sigma(4)$       | $3$            |
| $\sigma(5)$       | $4$            |

The permutations $\tau$ and $\sigma$ can therefore be written in cycle notation as $\tau=\begin{pmatrix}2&5&3&4\end{pmatrix}$ and $\sigma=\begin{pmatrix}1&2&5&4&3\end{pmatrix}$, in which obviously
- $\sigma\tau=\begin{pmatrix}1&2&5&4&3\end{pmatrix}\begin{pmatrix}2&5&3&4\end{pmatrix}=\begin{pmatrix}1&2&4&5\end{pmatrix}$,
- $\tau\sigma=\begin{pmatrix}2&5&3&4\end{pmatrix}\begin{pmatrix}1&2&5&4&3\end{pmatrix}=\begin{pmatrix}1&5&2&3\end{pmatrix}$, 
- $\sigma(1)=2$,
as required by the original problem.

**(5)**. We need to show that $\tau\sigma=\begin{pmatrix}1&2&3&4\end{pmatrix}$ and $\sigma\tau=\begin{pmatrix}1&2\end{pmatrix}\begin{pmatrix}3&4\end{pmatrix}$ is impossible for $\sigma,\;\tau\in S_4$. The table of extractable information would be

| The expression... | Is equal to... |
| ----------------- | -------------- |
| $\tau(\sigma(1))$ | $2$            |
| $\tau(\sigma(2))$ | $3$            |
| $\tau(\sigma(3))$ | $4$            |
| $\tau(\sigma(4))$ | $1$            |
| $\sigma(\tau(1))$ | $2$            |
| $\sigma(\tau(2))$ | $1$            |
| $\sigma(\tau(3))$ | $4$            |
| $\sigma(\tau(4))$ | $3$            |

We can safely assume that $\tau(1)\in\{1,2,3,4\}$. Consider those four cases, starting with $\tau(1)=1$. We construct this first table, stopping at the apparent impossibility:

| The expression... | Is equal to... |
| ----------------- | -------------- |
| $\tau(2)$         | $2$            |
| $\tau(1)$         | $3$            |
| $\tau(\sigma(3))$ | $4$            |
| $\tau(\sigma(4))$ | $1$            |
| $\sigma(1)$       | $2$            |
| $\sigma(2)$       | $1$            |
| $\sigma(\tau(3))$ | $4$            |
| $\sigma(\tau(4))$ | $3$            |

Here, we've stopped at the point of implication where $\tau(1)=3$. We'll continue with the other cases of $\tau(1)=2$, $\tau(1)=3$, and $\tau(1)=4$:

| The expression... | Is equal to... |
| ----------------- | -------------- |
| $\tau(\sigma(1))$ | $2$            |
| $\tau(2)$         | $3$            |
| $\tau(1)$         | $4$            |
| $\tau(\sigma(4))$ | $1$            |
| $\sigma(2)$       | $2$            |
| $\sigma(3)$       | $1$            |
| $\sigma(\tau(3))$ | $4$            |
| $\sigma(\tau(4))$ | $3$            |

| The expression... | Is equal to... |
| ----------------- | -------------- |
| $\tau(\sigma(1))$ | $2$            |
| $\tau(\sigma(2))$ | $3$            |
| $\tau(2)$         | $4$            |
| $\tau(1)$         | $1$            |
| $\sigma(3)$       | $2$            |
| $\sigma(4)$       | $1$            |
| $\sigma(\tau(3))$ | $4$            |
| $\sigma(\tau(4))$ | $3$            |

| The expression... | Is equal to... |
| ----------------- | -------------- |
| $\tau(1)$         | $2$            |
| $\tau(\sigma(2))$ | $3$            |
| $\tau(\sigma(3))$ | $4$            |
| $\tau(2)$         | $1$            |
| $\sigma(4)$       | $2$            |
| $\sigma(1)$       | $1$            |
| $\sigma(\tau(3))$ | $4$            |
| $\sigma(\tau(4))$ | $3$            |

So, no matter the choice of $\tau(1)$, this situation is an impossibility, always implying that $\tau(1)$ is not equal to our choice. Therefore, this situation is impossible.

**(6)**. The permutations $\sigma$ and $\tau$ fix $k$ iff $\sigma(k)=\tau(k)=k$. Then 
- $(\sigma\circ\tau)(k)=\sigma(\tau(k))=\sigma(k)=k$, so $\sigma\tau$ indeed fixes $k$, and
- $\sigma(k)=k$ and $\sigma$ by definition being invertible implies that $\sigma^{-1}(k)=k$, so $\sigma^{-1}$ fixes $k$.

**(7)**. Permutations in $S_5$ that fix $1$ are simply of the form $\begin{pmatrix}1&2&3&4&5\\1&a&b&c&d\end{pmatrix}$. Since there are $4$ different unknowns and they can be in any order, we have $4!$ possible choices for such a permutation, and therefore $4!$ permutations in $S_5$ that fix $1$.

Likewise for those that fix $1$ *and* $2$: there exists $(5-2)!=3!$ of such permutations in $S_5$.

**(8)**.

**(a)**. For $\sigma,\;\tau\in X_n$, the permutation $\sigma\tau$ is equal to $\epsilon$ iff $(\forall k\in X_n)(\sigma(\tau(k))=k)$. Since $\sigma$ is by definition invertible, this is the case iff $(\forall k\in X_n)(\tau(k)=\sigma^{-1}(k))$, which is the case iff $(\forall k\in X_n)(\tau^{-1}(k)=\sigma(k))$, which is the case iff $\sigma=\tau^{-1}$.

**(b)**. For $\sigma\in S_n$, the permutation $\sigma^2$ is equal to $\epsilon$ iff $(\forall k\in X_n)(\sigma(\sigma(k))=k)$. Since $\sigma$ is by definition invertible, this is the case iff $(\forall k\in X_n)(\sigma(k)=\sigma^{-1}(k))$, which is the case iff $\sigma=\epsilon$.

**(9)**. For $\sigma,\;\tau\in X_n$, the permutation $\sigma$ is equal to $\tau$ iff s