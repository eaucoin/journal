
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

Now, note that:
$$\begin{align*}
\gcd(a,b) =& p_1^{\min(a_1,b_1)}\cdots p_k^{\min(a_k,b_k)}\\
\gcd(a,c) =& p_1^{\min(a_1,c_1)}\cdots p_k^{\min(a_k,c_k)}
\end{align*}$$

and therefore:
$$\gcd(a,b)\gcd(a,c) = p_1^{\min(a_1,b_1)+\min(a_1,c_1)}\cdots p_k^{\min(a_k,b_k)+\min(a_k,c_k)}$$

Therefore, to show that $a\mid\gcd(a,b)\gcd(a,c)$, we need to show that:
$$\begin{align*}
a_i \leq& \min(a_i,b_i)+\min(a_i,c_i)\\
\vdots&\\
a_k \leq& \min(a_k,b_k)+\min(a_k,c_k)
\end{align*}$$

Let $1\leq i\leq k$, and we consider two cases:

Case 1: $\min(a_i,b_i) = a_i$ OR $\min(a_i,c_i) = a_i$
$$\begin{align*}
\text{In this case, }&\min(a_i,b_i)+\min(a_i,c_i) = a_i+x\text{, }x\geq0\\
\Rightarrow& a_i \leq \min(a_i,b_i)+\min(a_i,c_i)
\end{align*}$$

Case 2: $\min(a_i,b_i) = b_i$ and $\min(a_i,c_i) = c_i$
$$\begin{align*}
\text{In this case, }&\min(a_i,b_i)+\min(a_i,c_i) = b_i+c_i \geq a_i\\
&\text{by equation (1)}
\end{align*}$$

Therefore, $a\mid\gcd(a,b)\gcd(a,c)$. ■

(2). There exists $m,n \in \mathbb{Z}$ such that:
$$\begin{align*}
\gcd(a,b) =& ma+nb\\
\text{and }r,s \in \mathbb{Z}\text{ such that}\\
\gcd(a,c) =& ra+sc
\end{align*}$$

Therefore:
$$\begin{align*}
\gcd(a,b)\gcd(a,c) =& (ma+nb)(ra+sc)\\
=& mra^2 + msac + nrab + nsbc
\end{align*}$$

Since $a\mid mra^2$, $msac$ & $nrab$ obviously, and since we assume that $a\mid bc$,
we have $a\mid\gcd(a,b)\gcd(a,c)$. ■

## Problem 5.
Suppose $x^2-5y^2=3$ has integer solutions $x,y$.

Taking the equation modulo 5:
$$x^2 \equiv 3 \pmod{5}$$

Method 1: By trying out all possible $x \pmod{5}$, we see that this is impossible.

Method 2:
$$\begin{align*}
x^2 \equiv 3 \pmod{5}\text{ implies that}&\text{ (is equivalent to, in fact) }(\frac{3}{5})=1\\\\
\text{However, }(\frac{3}{5}) =& (\frac{5}{3}) = (\frac{2}{3}) = -1\\
&\text{since }3 \equiv 3 \pmod{8}
\end{align*}$$

By contradiction, $x^2-5y^2=3$ has no integer solutions.

## Problem 6.
Define the Von Mangoldt function:
$$\Lambda(n) := \begin{cases}
\log p & \text{if }n=p^k\text{ for some prime }p, k\geq 1\\
0 & \text{otherwise}
\end{cases}$$

(1). Compute the first 7 values of $\Lambda$:
$$\begin{align*}
\Lambda(1) =& 0\\
\Lambda(2) = \Lambda(2^1) =& \log 2\\
\Lambda(3) = \Lambda(3^1) =& \log 3\\
\Lambda(4) = \Lambda(2^2) =& \log 2\\
\Lambda(5) = \Lambda(5^1) =& \log 5\\
\Lambda(6) = \Lambda(2\times3) =& 0\\
\Lambda(7) = \Lambda(7^1) =& \log 7
\end{align*}$$

(2). Show that $\log(n) = \sum_{d\mid n} \Lambda(d)$ for all $n \geq 1$

Write the prime factorization of $n$ as:
$$n = p_1^{\alpha_1}\cdots p_k^{\alpha_k}$$
where $p_1,\cdots,p_k$ are distinct primes & $\alpha_1\geq1,\cdots,\alpha_k\geq1$.

Now, note that all divisors $d\mid n$ correspond to:
$$d = p_1^{\beta_1}\cdots p_k^{\beta_k}$$ 
with $0\leq\beta_1\leq\alpha_1,\cdots,0\leq\beta_k\leq\alpha_k$.

[Should I continue with the rest of this problem and Problems 7-8?]