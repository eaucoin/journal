
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
Let $a$, $b$ & $c$ be natural numbers such that $a\mid bc$.

Show that $a\mid\gcd(a,b)\gcd(a,c)$.

Note: I want you to do this in two ways:

(1). Use prime factorizations and how the gcd can be written in terms of prime factorization.

Solution:
We write:
$$\begin{align*}
a =& p_1^{a_1}\cdots p_k^{a_k}\\
b =& p_1^{b_1}\cdots p_k^{b_k}\\
c =& p_1^{c_1}\cdots p_k^{c_k}
\end{align*}$$

where $p_1,\cdots,p_k$ are distinct primes and $a_i,\cdots,a_k,b_1,\cdots,b_k,c_1,\cdots,c_k \geq 0$.

Then:
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

(2). Do this using the "same ideas" as we proved that $p\mid bc \Rightarrow p\mid b$ or $p\mid c$ when $p$ is prime.

Solution:
There exists $m,n \in \mathbb{Z}$ such that:
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
Using an appropriate congruence, show that the equation $x^2-6y^2=3$ has no integer solutions.

**Solution.** Suppose $x^2-5y^2=3$ has integer solutions $x,y$.

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

Then:
$$\begin{align*}
\sum_{d\mid n}\Lambda(d) =& \sum_{0\leq\beta_1\leq\alpha_1,\cdots,0\leq\beta_k\leq\alpha_k}\Lambda(p_1^{\beta_1}\cdots p_k^{\beta_k})
\end{align*}$$

By the definition of the Von Mangoldt function:
$$\begin{align*}
\Lambda(p_1^{\beta_1}\cdots p_k^{\beta_k}) = 0
\end{align*}$$
unless $1\leq\beta_i\leq\alpha_i$ for some $1\leq i\leq k$ and $\beta_j=0$ for $j\neq i$. In other words:

$$\begin{align*}
\sum_{d\mid n}\Lambda(d) =& 0 + \sum_{1\leq\beta_1\leq\alpha_1}\Lambda(p_1^{\beta_1}) +\cdots+ \sum_{1\leq\beta_k\leq\alpha_k}\Lambda(p_k^{\beta_k})\\\\
=& \sum_{1\leq\beta_1\leq\alpha_1}\log(p_1) +\cdots+ \sum_{1\leq\beta_k\leq\alpha_k}\log(p_k)\\\\
=& \alpha_1\log(p_1)+\cdots+\alpha_k\log(p_k)\\\\
=& \log(p_1^{\alpha_1}\cdots p_k^{\alpha_k})\\\\
=& \log(n)\text{. }■
\end{align*}$$

(3). Is $\Lambda$ multiplicative? Why or why not?

$$\begin{align*}
\Lambda(6) =& 0\\
\Lambda(2)\Lambda(3) =& (\log 2)(\log 3) \neq 0\\
\text{and }& 6=2\times3\text{ with }\gcd(2,3)=1
\end{align*}$$

Therefore, $\Lambda$ is not multiplicative.

## Problem 7.
Define the Möbius function:
$$\mu(n) := \begin{cases}
1, & n=1\\
(-1)^k, & n\text{ is the product of }k\text{ distinct primes}\\
0, & n\text{ is divisible by a square}>1
\end{cases}$$

(1). Show that if $m,n \geq 1$, $\gcd(m,n)=1$, then $\mu(mn) = \mu(m)\mu(n)$

We consider three Cases:

Case 1:
$$\begin{align*}
\text{a) }m=1:&\\
\text{Then, }&\mu(m)=1\text{ by definition}\\
\mu(mn)=&\mu(1\times n)=\mu(n)=1\times\mu(n)=\mu(m)\mu(n)\\\\
\text{b) }n=1:&\\
&\mu(mn)=\mu(m)\mu(n)\text{ Similarly to (a)}
\end{align*}$$

Case 2:
$$\begin{align*}
\text{a) }m\text{ is divisible}&\text{ by a square, say }k^2m_1\text{, }k^2>1\\
\text{Then, }&\text{by definition, }\mu(m)=0\\
mn=&k^2m_1n\text{ which is also divisible by }k^2\text{, so }\mu(mn)=0\\
\text{Therefore, }&\mu(mn)=\mu(m)\mu(n)
\end{align*}$$

Case 3:
$$\begin{align*}
&m>1, n>1\text{ and }m\text{ and }n\text{ are not divisible by a square,}\\
&\text{that is, they are both a product of distinct primes, say:}\\\\
m=&p_1\cdots p_k\text{, where }p_1,\cdots,p_k\text{ are distinct primes}\\
n=&q_1\cdots q_s\text{, where }q_1,\cdots,q_s\text{ are distinct primes}\\\\
\text{Then, }&mn=p_1\cdots p_kq_1\cdots q_s\\
&\text{Since }\gcd(m,n)=1\text{, the primes }p_1,\cdots,p_k,q_1,\cdots,q_s\text{ are all distinct,}\\
&\text{and thus, by definition:}\\\\
\mu(mn)=&(-1)^{k+s}=(-1)^k(-1)^s=\mu(m)\mu(n)
\end{align*}$$

(2). If $n\geq1$, show that:
$$\sum_{d\mid n}\mu(d) = \begin{cases}
1; & \text{if }n=1\\
0; & \text{if }n>1
\end{cases}$$

Now, suppose $n>1$ and write the prime factorization:
$$n = p_1^{\alpha_1}\cdots p_k^{\alpha_k}\text{, where }p_1,\cdots,p_k\text{ are distinct primes}$$

Let $F(n) = \sum_{d\mid n}\mu(d)$

By part 1, $\mu$ is multiplicative. Then, $F$ is multiplicative. Therefore,

$$\begin{align*}
\sum_{d\mid n}\mu(d) =& F(n) \\=& F(p_1^{\alpha_1})\cdots F(p_k^{\alpha_k})\text{.}\end{align*}$$
Now, 
$$\begin{align*}
F(p^{\alpha}) =& \sum_{0\leq b_i\leq\alpha}\mu(p^{\beta_i})\\\\
=&\mu(1) + \mu(p) + \mu(p^2)+\dots +\mu(p^{\alpha})\text{,}
\end{align*}$$
but


Therefore, $F(n) = 0$. ■

(3). Let:
$$g(n) = \sum_{d\mid mn}F(d)\mu(\frac{n}{d})$$

Using Remark and part 1:
$$\begin{align*}
=& \sum_{d_1\mid m\\d_2\mid n}F(d_1)F(d_2)\mu(\frac{m}{d_1})\mu(\frac{n}{d_2})\\\\
=& [\sum_{d_1\mid m}F(d_1)\mu(\frac{m}{d_1})][\sum_{d_2\mid n}F(d_2)\mu(\frac{n}{d_2})]\\\\
=& g(m)g(n)\text{. }■
\end{align*}$$

(4). If $F(n) := \sum_{d\mid n}f(d)$, using the definition of $\mu$, show that $g(p^\alpha) = f(p^\alpha)$:

$$\begin{align*}
g(p^\alpha) =& \sum_{d\mid p^\alpha}F(d)\mu(\frac{p^\alpha}{d})\\
=& \sum_{0\leq\beta\leq\alpha}F(p^\beta)\mu(p^{\alpha-\beta})
\end{align*}$$

By the definition of the Von Mangoldt function, $\mu(p^{\alpha-\beta})=0$ when $\alpha-\beta\geq2$ by definition, that is, when $\beta\leq\alpha-2$. Therefore:

$$\begin{align*}
g(p^\alpha) =& F(p^{\alpha-1})\mu(p) + F(p^\alpha)\mu(1)\\
=& F(p^\alpha) - F(p^{\alpha-1})\\
=& f(p^\alpha)\text{. }■
\end{align*}$$

(5). Use (4) & (3) to show that (Möbius inversion):
$$\sum_{d\mid n}F(d)\mu(\frac{n}{d}) = f(n)$$

Write:
$$n=p_1^{\alpha_1}\cdots p_k^{\alpha_k}\text{, }p_1,\cdots,p_k\text{ are distinct primes,}$$
$$\alpha_1\geq1,\cdots,\alpha_k\geq1$$

Then:
$$\begin{align*}
\sum_{d\mid n}F(d)\mu(\frac{n}{d}) =& g(n)\\
\stackrel{3.}{=}& g(p_1^{\alpha_1})\cdots g(p_k^{\alpha_k})\\
\stackrel{4.}{=}& f(p_1^{\alpha_1})\cdots f(p_k^{\alpha_k})\\
=& f(n)\text{ by multiplicativity of }f
\end{align*}$$

(6). Show that multiplicativity of $f$ is NOT needed for Möbius inversion:

Let $F(n) := \sum_{e\mid n}f(e)$

Then:
$$\begin{align*}
\sum_{d\mid n}F(d)\mu(\frac{n}{d}) =& \sum_{d\mid n}[\sum_{e\mid d}f(e)]\mu(\frac{n}{d})\\
=& \sum_{n=dd_1}[\sum_{e\mid d}f(e)]\mu(d_1)\\
=& \sum_{d\mid n}[\sum_{e\mid\frac{n}{d_1}}f(e)]\mu(d_1)\\
=& \sum_{e\mid n}f(e)\sum_{d_1\mid\frac{n}{e}}\mu(d_1)\\
=& f(n)\text{. }■
\end{align*}$$

## Problem 8.
Let $p$ be an odd prime and $g$ a primitive root of $p$. Show using the definition that $g^{-1} \pmod{p}$ is also a primitive root.

First:
$$\begin{align*}
(g^{-1})^{p-1} =& g^{(-1)(p-1)}\\
=& (g^{p-1})^{(-1)}\\
\equiv& 1 \pmod{p}
\end{align*}$$

Now, suppose that $(g^{-1})^n \equiv 1 \pmod{p}$ for $1\leq n\leq p-1$

Then:
$$\begin{align*}
1\equiv& g^{-n}\\
\equiv& g^{(p-1)-n}\\
\Rightarrow& g^{(p-1)-n} \equiv 1 \pmod{p}\\
\text{and }& 1\leq(p-1)-n < p-1
\end{align*}$$

contradicting the definition of primitive root of $p$.

By contradiction, $g^{-1}$ is a primitive root of $p$. ■