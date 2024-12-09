
## Problem 1.
Compute the following gcds without using prime factorization:

(1). 34302 & 5120

$$\begin{align*}
\gcd(5120, 3430) =& \gcd(5120-3430,3430)\\
=& \gcd(3430, 1690)\\
=& \gcd(1690, 3430-2\times1690)\\
=& \gcd(1690, 50)\\
=& \gcd(50, 1690-33\times50)\\
=& \gcd(50, 40)\\
=& \gcd(40, 50-40)\\
=& \gcd(40,10)\\
=& 10
\end{align*}$$

Since $10\mid40$ and $\gcd(a,b)=\gcd(a,r)$ where
$$a = qb+r,\text{ }0\leq r < b$$

(2). 4181, 7315

$$\begin{align*}
\gcd(4181,7315) =& \gcd(7315-4181,4181)\\
=& \gcd(4181, 3134)\\
=& \gcd(3134, 4181-3134)\\
=& \gcd(3134, 927)\\
=& \gcd(927, 3134-3\times927)\\
=& \gcd(927, 413)\\
=& \gcd(413, 927-2\times413)\\
=& \gcd(413, 101)\\
=& \gcd(413, 413-4\times101)\\
=& \gcd(413, 9)\\
=& \gcd(9, 413-45\times9)\\
=& \gcd(9,8)\\
=& 1
\end{align*}$$

(3). 289, 4913

$$\begin{align*}
\gcd(4913, 289) =& \gcd(289, 4913-17\times289)\\
=& \gcd(289,0)\\
=& 289
\end{align*}$$

## Problem 2.
(1). Find the prime factorization of 228:
$$\begin{align*}
228 =& 4\times57\\
=& 4\times3\times19\\
=& 2^2\times3\times19
\end{align*}$$

(2). Find the prime factorization of 195:
$$\begin{align*}
195 =& 5\times39\\
=& 5\times3\times13
\end{align*}$$

Find $\gcd(228,195)$ using prime factorization:
$$\begin{align*}
\gcd(228,195) =& \gcd(4\times3\times19, 5\times3\times13)\\
=& \gcd(2^2\times3\times19, 5\times3\times13)\\
=& 2^{\min(2,0)}\times3^{\min(1,1)}\times5^{\min(0,1)}\times13^{\min(0,1)}\times19^{\min(1,0)}\\
=& 3
\end{align*}$$

Find $m$ & $n \in \mathbb{Z}$ such that $228m + 195n = 3$:

We employ the Euclidean algorithm:
$$\begin{align*}
(a,b) =& (228,195)\\
(b,a-b) =& (195,33)\\
(a-b, b-5(a-b)) =& (33,30)\\
=& (a-b, 6b-5a)\\\\
\therefore a-b-(6b-5a) =& 33-30 = 3\\
\therefore 6a-7b =& 3\\
\therefore m = 6,\text{ }n =& -7
\end{align*}$$

## Problem 3.
Use induction to prove that:

(1). $6^n \equiv 5n+1 \pmod{25}$ for all $n \geq 0$

Base Case: $n=0$
$$\begin{align*}
6^0 =& 1\\
5\times0+1 =& 1\\
6^0 \equiv& 5\times0+1 \pmod{25}
\end{align*}$$

Induction Step: Suppose $6^k \equiv 5k+1 \pmod{25}$ for some $k\geq0$

$$\begin{align*}
6^{k+1} =& 6\times6^k\\
\equiv& 6\times(5k+1)\\
=& 30k+6\\
\equiv& 25k+5k+6\\
\equiv& 5k+6\\
\equiv& 5(k+1)+1 \pmod{25}
\end{align*}$$

By induction, $6^n \equiv 5n+1$ for all $n \geq 0$.

(2). $2^n \mid (2n)!$ for all $n \geq 0$

Base Case: $n=0$
$$\begin{align*}
2^0 =& 1\\
(2\times0)! =& 0! = 1\\
& 1\mid1\text{, we have }2^n\mid(2n)!\text{ for }n=0
\end{align*}$$

Induction Step: Suppose $2^k\mid(2k)!$ for some $k\geq0$

$$\begin{align*}
(2(k+1))! =& (2k+2)(2k+1)(2k)!\\
=& (2k+2)(2k+1)\cdot q\cdot2^k\\
=& q(k+1)(2k+1)\cdot2^{k+1}\\
\Rightarrow& 2^{k+1}\mid(2(k+1))!
\end{align*}$$

By induction, $2^n\mid(2n)!$ for all $n\geq0$.

(3). All natural numbers $\geq23$ can be written as $5m + 7n$, $m,n \geq 0$

Base Cases:
$$\begin{align*}
5\times2+7\times2 =& 24\\
5\times5+7\times0 =& 25\\
5\times1+7\times3 =& 26\\
5\times4+7\times1 =& 27\\
5\times0+7\times4 =& 28
\end{align*}$$

Induction Step:
Suppose that $k = 5m+7n$ for some $m,n\geq0$ & $k\geq24$.

Then:
$$\begin{align*}
k+5 =& 5(m+1)+7n\\
\text{Since }& m+1\geq0, n\geq0\text{, by induction,}\\
\text{we have that all }& k\geq24\text{ can be written as }5m+7n\text{,}\\
\text{where }& m,n\geq0
\end{align*}$$

## Problem 4.
(1). We write:
$$\begin{align*}
a =& p_1^{a_1}\cdots p_k^{a_k}\\
b =& p_1^{b_1}\cdots p_k^{b_k}\\
c =& p_1^{c_1}\cdots p_k^{c_k}
\end{align*}$$

where $p_1,\cdots,p_k$ are distinct primes and $a_i,\cdots,a_k,b_1,\cdots,b_k,c_1,\cdots,c_k \geq 0$.

$$bc = p_1^{b_1+c_1}\cdots p_k^{b_k+c_k}$$

Therefore, $a\mid bc$ implies (is equivalent to, in fact) that:
$$a_i \leq b_i+c_i,\cdots,a_k \leq b_k+c_k \text{ } (1)$$

[Continue with the rest of Problem 4 and Problems 5-8?]