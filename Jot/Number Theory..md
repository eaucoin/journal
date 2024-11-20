## Homework for the Week of November 11th.

### Problem 1: Euler's Theorem on Sum of Two Squares in $\mathbb{Z}[i]$

**Theorem (Euler):** If $a,b \in \mathbb{Z}$ with $\gcd(a,b)=1$, then any divisor of $a^2+b^2$ is of the form $c^2+d^2$ where $c,d \in \mathbb{Z}$ with $\gcd(c,d)=1$.

**(1) Necessity of the $\gcd(a,b)=1$ condition:**

Let's examine why this condition is crucial through a counterexample:

Take $a=2$ and $b=4$. Here:
$$\gcd(2,4) = 2 \neq 1$$
$$a^2 + b^2 = 2^2 + 4^2 = 4 + 16 = 20$$

Now, 4 is a divisor of 20. If the theorem were true without the coprime condition, 4 would need to be expressible as $c^2 + d^2$ with $\gcd(c,d)=1$. However:

- The only ways to express 4 as a sum of squares are:
$$4 = 2^2 + 0^2 = 0^2 + 2^2$$
In both cases, $\gcd(c,d) = 2 \neq 1$

**(2) Prime factorization in $\mathbb{Z}[i]$:**

First, observe that in $\mathbb{Z}[i]$:
$$a^2 + b^2 = (a+bi)(a-bi)$$

Let $e$ be a divisor of $a^2+b^2$ where $e > 1$. By the fundamental theorem of arithmetic in $\mathbb{Z}[i]$ (which is a unique factorization domain), we can write:
$$e = u\pi_1\pi_2...\pi_n$$
where:
- $u$ is a unit in $\mathbb{Z}[i]$ (one of $\{1,-1,i,-i\}$)
- Each $\pi_k$ is a Gaussian prime of the form $q_k+ir_k$

**(3) Division properties:**

Let $\pi = q+ir$ be any Gaussian prime dividing $e$. Then:
$$\pi \mid e \text{ and } e \mid (a+bi)(a-bi)$$

By the transitivity of division:
$$\pi \mid (a+bi)(a-bi)$$

Since $\pi$ is prime in $\mathbb{Z}[i]$ and $\mathbb{Z}[i]$ is a unique factorization domain, by the prime property:
$$\text{If } \pi \mid xy \text{ then } \pi \mid x \text{ or } \pi \mid y$$

Therefore:
$$\pi \mid (a+bi) \text{ or } \pi \mid (a-bi)$$

**(4) Showing Gaussian prime factors are not ordinary primes:**

Let's proceed by contradiction. Suppose $\pi = q+ir$ is both a Gaussian prime and an ordinary prime $p$. Then:

$$\pi = p = q+ir$$

Since $\pi$ divides either $a+bi$ or $a-bi$ (from part 3), we have:
$$(a+bi) = \pi(x+yi) \text{ or } (a-bi) = \pi(x+yi)$$
for some $x,y \in \mathbb{Z}$.

Taking the real and imaginary parts:
$$a = px - ry \text{ and } b = rx + py$$
or
$$a = px + ry \text{ and } b = -rx + py$$

In either case, $p$ divides both $a$ and $b$ in $\mathbb{Z}$. Therefore:
$$p \mid \gcd(a,b)$$

But this contradicts our assumption that $\gcd(a,b)=1$.

**(5) Conjugate pairs of Gaussian primes:**

Let $\pi = q+ir$ be a Gaussian prime dividing $e$. Since $e \in \mathbb{Z}$:
$$e = e\cdot 1 = e \cdot (1 \cdot \overline{1}) = e \cdot \frac{\overline{e}}{e} \cdot e = \overline{e}$$

Therefore, if $\pi$ divides $e$, then $\overline{\pi} = q-ir$ must also divide $e$.

To show these factors are distinct, suppose for contradiction that:
$$q+ir = u(q-ir)$$
where $u$ is a unit in $\mathbb{Z}[i]$.

For the four possible units:
$$\text{If } u = 1: \text{ then } r = 0$$
$$\text{If } u = -1: \text{ then } q = 0$$
$$\text{If } u = i: \text{ then } q = r$$
$$\text{If } u = -i: \text{ then } q = -r$$

Each case either makes $\pi$ an ordinary integer (contradicting part 4) or forces it to be an associate of $1+i$, which we can show contradicts $\gcd(a,b)=1$.

**(6) Form of $e$ as sum of squares:**

Since all prime factors of $e$ come in conjugate pairs $(\pi_k, \overline{\pi_k})$, we can group them:
$$e = \prod_{k=1}^n (\pi_k\overline{\pi_k})$$

Each factor $\pi_k\overline{\pi_k} = (q_k+ir_k)(q_k-ir_k) = q_k^2 + r_k^2$

Therefore:
$$e = (c+di)(c-di) = c^2 + d^2$$
where $c+di$ is the product of some subset of the Gaussian prime factors.

**(7) Proving $\gcd(c,d)=1$:**

Suppose $\gcd(c,d) = g > 1$. Then:
$$g^2 \mid (c^2 + d^2) = e$$
$$g^2 \mid (a^2 + b^2)$$

This implies:
$$g \mid (a+bi) \text{ and } g \mid (a-bi)$$
$$\therefore g \mid 2a \text{ and } g \mid 2b$$
$$\therefore g \mid 2\gcd(a,b) = 2$$

Thus $g=2$. But then $2 \mid e$, and since:
$$2 = (1+i)(1-i) = -i(1+i)^2$$

This means $1+i$ divides both $a+bi$ and $a-bi$, which contradicts $\gcd(a,b)=1$ as shown earlier.

Therefore, $\gcd(c,d) = 1$, completing the proof of Euler's theorem.

I'll rewrite this with detailed mathematical explanations and demonstrations:

### Problem 2: Infinitude of Primes Dividing Polynomial Values

Let's begin with a polynomial $f(x)$ with integer coefficients:
$$f(x) = a_mx^m + a_{m-1}x^{m-1} + ... + a_1x + a_0$$
where $a_0, a_m \neq 0$

We'll prove by contradiction that infinitely many primes divide values of $f(x)$.

**(1) Initial Setup and Degree Analysis:**

Let's assume for contradiction that only finitely many primes $p_1, p_2, ..., p_k$ divide values of $f(x)$ for $x \in \mathbb{Z}$.

Define:
$$g(y) = \frac{1}{a_0}f(p_1p_2...p_ky)$$

To analyze the degree:
$$\begin{align*}
g(y) &= \frac{1}{a_0}[a_m(p_1p_2...p_ky)^m + ... + a_1(p_1p_2...p_ky) + a_0] \\
&= \frac{a_m}{a_0}(p_1p_2...p_k)^my^m + ... + \frac{a_1}{a_0}(p_1p_2...p_k)y + 1
\end{align*}$$

The coefficient of $y^m$ is $\frac{a_m}{a_0}(p_1p_2...p_k)^m \neq 0$, so $g(y)$ has degree $m$.

**(2) Integer Coefficients:**

For each term in $g(y)$:
$$\text{coefficient of }y^j = \frac{a_j}{a_0}(p_1p_2...p_k)^j$$

Since $p_1p_2...p_k$ divides each term except the constant term, and $a_0$ divides $f(p_1p_2...p_k)$, all coefficients are integers.

**(3) Prime Divisor Property:**

Let $p$ be a prime dividing $g(y)$ for some $y \in \mathbb{Z}$. Then:
$$p \mid g(y) = \frac{1}{a_0}f(p_1p_2...p_ky)$$
$$\therefore p \mid f(p_1p_2...p_ky)$$

Let $x = p_1p_2...p_ky$. Then $x \in \mathbb{Z}$ and:
$$p \mid f(x)$$

**(4) Original Primes Don't Divide $g(y)$:**

For any $p_i$ among our original primes:
$$f(p_1p_2...p_ky) \equiv a_0 \pmod{p_i}$$

Since by assumption $\gcd(a_0, p_i) = 1$:
$$\frac{1}{a_0}f(p_1p_2...p_ky) \equiv \frac{1}{a_0}a_0 \equiv 1 \pmod{p_i}$$

Therefore, $p_i \nmid g(y)$ for any $y \in \mathbb{Z}$.

**(5) Value Restriction:**

From (3), any prime dividing $g(y)$ must be among $p_1, ..., p_k$.
From (4), none of $p_1, ..., p_k$ can divide $g(y)$.

Therefore:
$$g(y) \text{ must equal } \pm 1 \text{ for all } y \in \mathbb{Z}$$

**(6) Finite Solutions:**

Consider the equations:
$$g(y) = 1 \text{ and } g(y) = -1$$

By the fundamental theorem of algebra:
- $g(y) = 1$ has at most $m$ complex roots
- $g(y) = -1$ has at most $m$ complex roots

Therefore, these equations have at most $2m$ integer solutions combined.

**(7) Contradiction:**

We have shown:
1. $g(y) = \pm 1$ for all $y \in \mathbb{Z}$ (from step 5)
2. $g(y) = \pm 1$ has at most $2m$ integer solutions (from step 6)

Since $\mathbb{Z}$ is infinite and $2m$ is finite, this is a contradiction.

**(8) Conclusion:**

Our initial assumption must be false. Therefore:
$$\text{There are infinitely many primes } p \text{ that divide values of } f(x)$$

This generalizes our earlier proof about primes $p \equiv 1 \pmod{4}$, where we used $f(x) = x^2 + 1$.

### Problem 3. The goal of this exercise is to show that any prime $p$ can be written as $p = x^2 - 2y^2$ if and only if $p \equiv \pm1 \pmod{8}$.

To this end, define:
- $\mathbb{Z}[\sqrt{2}] := \{a+b\sqrt{2}; a,b\in\mathbb{Z}\}$
- $\text{norm}(a+b\sqrt{2}) = a^2-2b^2$
- $\pi$ is a prime in $\mathbb{Z}[\sqrt{2}]$ if $\pi\neq\alpha\beta$ for $\alpha,\beta\in\mathbb{Z}[\sqrt{2}]$ with $|\text{norm}(\alpha)|>1$, $|\text{norm}(\beta)|>1$
- If $\pi = a+b\sqrt{2}$, define the conjugate $\overline{\pi} = a-b\sqrt{2}$
- $\text{norm}(\pi_1\pi_2) = \text{norm}(\pi_1)\text{norm}(\pi_2)$

**(1)** The squares modulo 8 are 0, 1, and 4. Thus, $x^2$ can be congruent to 0, 1, or 4 modulo 8, and $2y^2$ can be congruent to 0 or 2 modulo 8. Therefore, $x^2 - 2y^2$ can be congruent to 0, 1, 2, 4, 6, or 7 modulo 8. If $p$ is an odd prime, then $p$ cannot be congruent to 0, 2, 4, or 6 modulo 8. Also, if $p \equiv 3, 5 \pmod{8}$, then $(\frac{2}{p})=-1$, so $p$ does not divide $x^2-2$, and hence $p$ is prime in $\mathbb{Z}[\sqrt{2}]$, thus $p$ is not of the form $x^2 - 2y^2$. Therefore if $p = x^2 - 2y^2$ for some integers $x$ and $y$, and $p$ is prime, $p$ must be congruent to $\pm 1 \pmod{8}$.

**(2)** If $2=x^2-2y^2$, then $x^2 \equiv 2 \pmod{2}$, which means $x^2$ is even, so $x$ is even. Let $x=2k$. Then $2 = 4k^2 - 2y^2$ implying $1 = 2k^2 - y^2$, so $y^2 \equiv -1 \equiv 1 \pmod{2}$, and $y$ is also even. Then let $y=2j$, which gives 
$$\begin{align*}
1&=2k^2-4j^2\\
&=2(k^2-2j^2)\text{,}
\end{align*}$$
which is a contradiction because the right-hand side is even. Thus, $p$ cannot be 2.

**(3)** Since $p \equiv \pm 1 \pmod{8}$, we have $(\frac{2}{p}) = 1$ by quadratic reciprocity. This means that $2$ is a quadratic residue modulo $p$, so there exists an integer $m$ such that $m^2 \equiv 2 \pmod{p}$.

**(4)** We can write $m^2 \equiv 2 \pmod{p}$ as $m^2 - 2 \equiv 0 \pmod{p}$. This means $p | (m - \sqrt{2})(m + \sqrt{2})$ in $\mathbb{Z}[\sqrt{2}]$. If $p$ were prime in $\mathbb{Z}[\sqrt{2}]$, then it would divide either $m - \sqrt{2}$ or $m + \sqrt{2}$. This would imply that $p$ divides $2\sqrt{2}$ and hence $p^2 | 8$, so $p=2$, but this contradicts the initial condition that $p \equiv \pm 1 \pmod{8}$. Therefore $p$ is not a prime in $\mathbb{Z}[\sqrt{2}]$.

**(5)** $\mathbb{Z}[\sqrt{2}]$ has the division property. To see why, let $\alpha=a+b\sqrt{2}$ and $\beta = c+d\sqrt{2}$ be elements of $\mathbb{Z}[\sqrt{2}]$ where $\beta \neq 0$. Consider the quotient 
$$\begin{align*}
\frac{\alpha}{\beta} &= \frac{a+b\sqrt{2}}{c+d\sqrt{2}} \\
&= \frac{(a+b\sqrt{2})(c-d\sqrt{2})}{c^2-2d^2} \\
&= \frac{ac-2bd}{c^2-2d^2} + \frac{bc-ad}{c^2-2d^2}\sqrt{2} \\
&= r_1+r_2\sqrt{2}\text{.}
\end{align*}$$

Let $m_1$ and $m_2$ be integers such that $|r_1-m_1| \leq \frac{1}{2}$ and $|r_2-m_2| \leq \frac{1}{2}$, and let $\gamma = m_1 + m_2\sqrt{2}$. Then 
$$\begin{align*}
|\text{norm}(\frac{\alpha}{\beta}-\gamma)| &= |(r_1-m_1)^2-2(r_2-m_2)^2| \\
&\leq |(\frac{1}{2})^2 + 2(\frac{1}{2})^2| \\
&= \frac{3}{4} \\
&< 1\text{.}
\end{align*}$$

Then letting $\rho = \alpha-\gamma\beta$, we have  
$$\begin{align*}
|\text{norm}(\rho)| &= |\text{norm}(\beta)| |\text{norm}(\frac{\alpha}{\beta}-\gamma)| \\
&< |\text{norm}(\beta)|\text{.}
\end{align*}$$

**(6)** Since $p$ is not prime in $\mathbb{Z}[\sqrt{2}]$, it must be expressible as $p = x^2 - 2y^2$ for some integers $x$ and $y$. This is because if $p$ factors nontrivially as $(x+y\sqrt{2})(u+v\sqrt{2})$ then multiplying by the conjugate gives $p^2=(x^2-2y^2)(u^2-2v^2)$, and unique prime factorization in integers forces both factors to equal $p$.

### Problem 4. The goal of this exercise is to give an alternative proof of $(\frac{p}{q}) = p^{\frac{q-1}{2}} \pmod{q}$.

**(1)** If $a$ is a primitive root of $q$, then we know $1,a,...,a^{q-2}$ are distinct nonzero elements mod $q$.
Show that the squares mod $q$ are $1,a^2,...,a^{q-3}$.

Let $g$ be a primitive root modulo $q$. This means that the powers $g^1, g^2, \dots, g^{q-1} \equiv 1 \pmod{q}$ are all distinct modulo $q$ and represent the $q-1$ non-zero residues modulo $q$.

**(2)** The squares modulo $q$ are precisely the even powers of $g$: $1, g^2, g^4, \dots, g^{q-3}$ (since $q-1$ is even, $q-3$ will be the largest even exponent less than $q-1$). There are $\frac{q-1}{2}$ such squares.

**(3)** If $P$ is a square modulo $q$, then $P \equiv g^{2k} \pmod{q}$ for some integer $k$. Then
$$\begin{align*}
P^{\frac{q-1}{2}} &\equiv (g^{2k})^{\frac{q-1}{2}} \\
&\equiv g^{k(q-1)} \\
&\equiv (g^{q-1})^k \\
&\equiv 1^k \\
&\equiv 1 \pmod{q}\text{,}
\end{align*}$$
by Fermat's Little Theorem.

**(4)** If $P$ is not a square modulo $q$, it must be congruent to an odd power of $g$: $P \equiv g^{2k+1} \pmod{q}$ for some integer $k$. Then
$$\begin{align*}
P^{\frac{q-1}{2}} &\equiv (g^{2k+1})^{\frac{q-1}{2}} \\
&\equiv g^{k(q-1)+\frac{q-1}{2}} \\
&\equiv (g^{q-1})^k g^{\frac{q-1}{2}} \\
&\equiv g^{\frac{q-1}{2}} \pmod{q}\text{.}
\end{align*}$$

Since $g$ is a primitive root, $g^{\frac{q-1}{2}} \not\equiv 1 \pmod{q}$. However, we know that $(g^{\frac{q-1}{2}})^2 \equiv g^{q-1} \equiv 1 \pmod{q}$. Because $q$ is prime, the congruence $x^2 \equiv 1 \pmod{q}$ has only two solutions: $x \equiv \pm 1 \pmod{q}$. Since $g^{\frac{q-1}{2}} \not\equiv 1 \pmod{q}$, we must have $g^{\frac{q-1}{2}} \equiv -1 \pmod{q}$. Thus, if $P$ is not a square modulo $q$, $P^{\frac{q-1}{2}} \equiv -1 \pmod{q}$.