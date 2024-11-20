## Homework for the Week of November 11th.

I'll rewrite this with more detailed mathematical demonstrations, making it more suitable for students learning the material. I'll break it down step by step with clear explanations and mathematical notation.

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

[Continued in next post due to length...]

### Problem 2. Recall that to show there are infinitely many primes $p \equiv 1 \pmod{4}$, we showed there are infinitely many primes $p$ that divide a value of the form $x^2+1$. We now generalize this.

- Let $f(x) = a_mx^m + ... + a_1x + a_0$, $a_0,...,a_m \in \mathbb{Z}$, $a_0\neq0$, $a_m\neq0$.
- We will show that there are infinitely many prime dividing values of $f(x)$ by contradiction. 
- To this end, suppose that there are finitely many primes $p_1,p_2,\dots p_k$ that divide $f(x)$, and let $g(y)$ be defined by $\frac{1}{a_0}f(p_1p_2\dots p_ky)$.

**(1)** Show that $g$ is of degree $m$.

Assume, for the sake of contradiction, that only finitely many primes $p_1, \dots, p_k$ divide values of $f(x)$ for $x \in \mathbb{Z}$. We can also assume that no prime dividing $a_m$ divides $f(x)$ for any integer $x$ (if this were the case, we could divide $f(x)$ by $a_m$ to obtain a new polynomial with the same set of prime divisors and a constant leading coefficient). Also, if $a_0 = 0$ then $f(p_1 \dots p_k)$ is composite, divisible by $p_1 \dots p_k$. Then $f(2p_1 \dots p_k)$ will be divisible by a prime not among $p_1, \dots, p_k$, contradicting the assumption. So we can assume $a_0 \neq 0$ and that $\gcd(a_0, a_m, p_1, \dots, p_k) = 1$.

**(2)** Show that $g(y)$ has integer coefficients.

Define $g(y) = \frac{1}{a_m}f(a_m p_1 \dots p_k y)$. Since $f(x)$ has integer coefficients, the constant term of $f(a_m p_1 \dots p_k y)$ is $a_0$, and all other terms are divisible by $a_m$. Therefore, $g(y)$ has integer coefficients. Furthermore, $g(y)$ has the same degree $m$ as $f(x)$.

**(3)** Show that if $p|g(y)$ for some $y\in\mathbb{Z}$, then $p|f(x)$ for some $x\in\mathbb{Z}$.

If a prime $p$ divides $g(y)$ for some $y \in \mathbb{Z}$, then $p | f(a_m p_1 \dots p_k y)$. Letting $x = a_m p_1 \dots p_k y$, we see that $p | f(x)$ for some $x \in \mathbb{Z}$.

**(4)** Show that none of $p_1,...,p_k$ divide $g(y)$ when $y\in\mathbb{Z}$.

Consider $f(a_m p_1 \dots p_k y) \pmod{p_i}$. We have
$$f(a_m p_1 \dots p_k y) \equiv a_0 \pmod{p_i}\text{.}$$
Since $\gcd(a_0, p_i) = 1$, $p_i$ does not divide $f(a_m p_1 \dots p_k y)$. As $p_i$ does not divide $a_m$ either, it follows that $p_i$ does not divide $g(y) = \frac{1}{a_m}f(a_m p_1 \dots p_k y)$.

**(5)** Conclude from **(3)** & **(4)**: that $g(y)=\pm1$.

From step 3, any prime dividing $g(y)$ must also divide a value of $f(x)$. From step 4, none of the primes $p_1, \dots, p_k$ divide $g(y)$. Thus, $g(y)$ must equal $\pm 1$ for all $y \in \mathbb{Z}$.

**(6)** Show that $g(y)=1$ & $g(y)=-1$ have only finitely many solutions.

Since $g(y)$ is a non-constant polynomial of degree $m$ with integer coefficients, the equations $g(y) = 1$ and $g(y) = -1$ each have at most $m$ integer solutions.

**(7)** Show that **(6)** contradicts **(5)**.

Step 5 asserts that $g(y) = \pm 1$ for all integers $y$, while step 6 states that these equations have at most $m$ integer solutions each. Since there are infinitely many integers $y$, this is a contradiction.

**(8)** Conclude.

The contradiction arises from assuming that only finitely many primes divide values of $f(x)$. Therefore, infinitely many primes must divide values of $f(x)$.

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