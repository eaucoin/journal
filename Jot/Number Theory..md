## Homework for the Week of November 11th.

### Problem 1. The goal of this exercise is to show how $\mathbb{Z}[i]$ sheds light on sum of two squares in other ways than what we've done so far.

Namely, we show the following theorem of Euler: If $a,b$ are integers with $\gcd(a,b)=1$, then any divisor of $a^2+b^2$ is of the form $c^2+d^2$ with $\gcd(c,d)=1$.

**(1)** Give an example that shows why the condition $\gcd(a,b)=1$ is necessary.

If $\gcd(a,b) \neq 1$, the theorem doesn't hold. For example, let $a = 2$ and $b = 4$. Then $\gcd(a, b) = 2$. We have $a^2 + b^2 = 20$, and $4$ is a divisor of $20$. However, $4$ can only be expressed as $c^2 + d^2$ if $c=2, d=0$ or $c=0, d=2$. If we require $\gcd(c, d) = 1$, then $4$ is not expressible in the required form.

**(2)** Let $e>1$ be an integer divisor of $a^2+b^2$. Show that $e$ is a product of Gaussian prime divisors $q+ir$ up to units.

We can factor $a^2 + b^2$ in $\mathbb{Z}[i]$ as $(a + bi)(a - bi)$. Let $e$ be a divisor of $a^2 + b^2$ in $\mathbb{Z}$. Then $e$ is also a divisor of $(a + bi)(a - bi)$ in $\mathbb{Z}[i]$. By unique prime factorization in $\mathbb{Z}[i]$, $e$ can be written as a product of Gaussian primes: $e = \pi_1 \pi_2 \cdots \pi_n$.

**(3)** Show that each of the Gaussian primes $q+ir$ divide either $a+ib$ or $a-ib$.

Since $e | (a+bi)(a-bi)$, each Gaussian prime $\pi_k$ dividing $e$ must also divide $(a+bi)(a-bi)$. Because $\pi_k$ is a Gaussian prime, it must divide either $a+bi$ or $a-bi$.

**(4)** Deduce from **(3)**: that none of the Gaussian primes $q+ir$ is an ordinary (in $\mathbb{Z}$) prime.

Suppose, for contradiction, that a Gaussian prime $\pi = q + ir$ is also an ordinary prime $p$. Since $\pi | a+bi$ or $\pi | a-bi$, we have $p | a+bi$ or $p | a-bi$. This implies $p|a$ and $p|b$ in $\mathbb{Z}$, contradicting $\gcd(a, b) = 1$. Therefore, $\pi$ cannot be an ordinary prime.

**(5)** Show that if $q+ir$ is a Gaussian prime dividing $e$, then its conjugate $q-ir$ is also a factor {distinct from $q+ir$}.

Let $e$ be a divisor of $a^2+b^2$. If a Gaussian prime $\pi = q + ir$ divides $e$, then its conjugate $\overline{\pi} = q - ir$ must also divide $e$. This is because $e$ is a real integer, and the conjugate of any factor of $e$ must also be a factor of $e$. These factors are distinct. If they were not distinct, then $q + ir = u(q - ir)$ for some unit $u \in \{1, -1, i, -i\}$. This implies either $r=0$ (if $u=1$) or $q=0$ (if $u=-1$), making $\pi$ or its associate equal to an ordinary integer, which we ruled out in step 4. The case where $q + ir$ is an associate of $1+i$ is more subtle. If both $a+bi$ and $a-bi$ are divisible by $1+i$, then both $a$ and $b$ are odd or both are even which contradicts $\gcd(a,b)=1$. Thus the prime factors of $e$ come in distinct conjugate pairs, or are equal to $1+i$.

**(6)** Deduce from **(5)**: that $e$ is of the form $c^2+d^2$ where $c+di$ divides $a+bi$.

Since $e$ is a product of Gaussian primes and their conjugates, we can write $e$ as $(c+di)(c-di) = c^2+d^2$, where $c+di$ is a product of some of the Gaussian primes dividing $e$.

**(7)** Deduce from **(6)**: that $\gcd(c,d)=1$.

Suppose $\gcd(c, d) = g > 1$. Then $g^2 | c^2 + d^2 = e$, so $g | a+bi$ and $g | a-bi$. This implies $g|2a$ and $g|2b$, so $g | 2\gcd(a, b) = 2$. Therefore, $g=2$. This implies $2 | e$, and since $2=(1+i)(1-i)=-i(1+i)^2$, the prime $1+i$ divides $a+ib$ and $a-ib$ which again contradicts $\gcd(a,b)=1$ as shown above. Therefore, $\gcd(c, d) = 1$.

### Problem 2. Recall that to show there are infinitely many primes $p \equiv 1 \pmod{4}$, we showed there are infinitely many primes $p$ that divide a value of the form $x^2+1$. We now generalize this.

- Let $f(x) = a_mx^m + ... + a_1x + a_0$, $a_0,...,a_m \in \mathbb{Z}$, $a_0\neq0$, $a_m\neq0$.
- We will show that there are infinitely many prime dividing values of $f(x)$ by contradiction. 
- To this end, suppose that there are finitely many primes $p_1,p_2,\dots p_k$ that divide $f()x$

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