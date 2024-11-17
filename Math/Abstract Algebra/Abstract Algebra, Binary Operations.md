
## Definition 1.

A binary operation $\star$ on a set $M$ is a subset of $M\times M$.

## Definition 2.

Let $*$ be a binary operation on $M$. The potential properties that $\star$ may have are:

| Property             | Statement                                                         |
| -------------------- | ----------------------------------------------------------------- |
| Associative          | $(\forall(a,\;b,\;c)\in M^3)(a\star(b\star c)=(a\star b)\star c)$ |
| Commutative          | $(\forall(a,\;b)\in M^2)(a\star b=b\star a)$                      |
| Existence of a Unity | $(\exists u\in M)(\forall a\in M)(a\star u=u\star a=a)$           |

## Theorem 1.

All unity elements are unique. 

## Definition 3.

If a binary operation $(M,\;\star)$ is both associative and has a unity, then $(M,\;\star)$ is called a monoid. If $(M,\;\star)$ is associative, has a unity, and is commutative, then $(M,\;\star)$ is called a commutative monoid.
## Theorem 2.

**Background.** The associativity of monoids.

**Statement.** $(a_1,\;a_2,\;\dots\;a_n)\in M^n$ implies that the product $a_1a_2\dots a_n$ is invariant to parentheses, i.e. ordering of the products.

## Theorem 3.

$\begin{align*}(\forall(a,\;b,\;m,\;n)\in M^2\times(\mathbb{N}\cup\{0\})^2)(&a^na^m=a^{n+m}\\\wedge\;&(a^n)^m=a^{nm}\\\wedge\;&(ab=ba\implies(ab)^n=a^nb^n))\end{align*}$

## Definition 4.

 - For a monoid $(M,\;\star)$, an element $b\in M$ is called the inverse of an element $a\in M$ iff $a\star b=1$. 
- For a monoid $(M,\;\star)$, an element $a\in M$ is called a unit iff there exists an element $b\in M$ such that $a\star b=1$.

So, an inverse is an element that inverts, while a unit is simply an invertible element.
## Theorem 4.

Inverses of a particular element of a monoid are unique.

## Theorem 5.

Let $a,b,a_1,a_2,\dots,a_{n-1},a_n\in M$; then $1$ is a unit, and $1^{-1}=1$. We would also have the following table.

| If:                                   | Then:                              | and in addition:                                                           |
| ------------------------------------- | ---------------------------------- | -------------------------------------------------------------------------- |
| $a$ is a unit                         | $a^{-1}$ is a unit                 |  $(a^{-1})^{-1}=a$                                                         |
| $a$ and $b$ are units                 | $ab$ is a unit                     | $(ab)^{-1}=b^{-1}a^{-1}$                                                   |
| $a_1,a_2,\dots,a_{n-1},a_n$ are units | $a_1a_2\dots a_{n-1}a_n$ is a unit | $(a_1a_2\dots a_{n-1}a_n)^{-1}=a_n^{-1}a_{n-1}^{-1}\dots a_2^{-1}a_1^{-1}$ |
| $a$ is a unit                         | $a^n$ is a unit                    | $(a^n)^{-1}=(a^{-1})^n$                                                    |

## Theorem 6.

$\begin{align*}(\forall(a,\;b,\;m,\;n)\in M^2\times \mathbb{Z}^2)(&a^na^m=a^{n+m}\\\wedge\;&(a^n)^m=a^{nm}\\\wedge\;&(ab=ba\implies (ab)^n=a^nb^n))\end{align*}$

