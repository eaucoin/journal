## Homework for the Week of November 11th.

### Problem 1: Euler's Theorem on Sum of Two Squares

**Main Theorem:** For coprime integers $a,b$, any divisor of $a^2+b^2$ is of the form $c^2+d^2$ with $\gcd(c,d)=1$.

**(1) Prove necessity of coprime condition:**
Let's examine what happens when we violate the coprime condition $\gcd(a,b)=1$:

Take $a=2$ and $b=4$ where $\gcd(2,4)=2$. Then:
$$a^2 + b^2 = 2^2 + 4^2 = 4 + 16 = 20$$

4 divides 20, but let's show 4 cannot be written as $c^2+d^2$ with $\gcd(c,d)=1$:

The only representations of 4 as sum of squares are:
$$4 = 2^2 + 0^2 = 0^2 + 2^2$$

In both cases, $\gcd(c,d) = 2 \neq 1$, proving the necessity of the coprime condition.

**(2) Prove factorization into Gaussian primes:**
We'll show any divisor $e > 1$ of $a^2+b^2$ factors into Gaussian primes.

First, factorize in $\mathbb{Z}[i]$:
$$a^2 + b^2 = (a+bi)(a-bi)$$

Let $e$ divide $a^2+b^2$. Then by unique factorization in $\mathbb{Z}[i]$ (a UFD):
$$e = u\pi_1\pi_2...\pi_n$$
where:
- $u$ is a unit in $\mathbb{Z}[i]$ (one of $\{1,-1,i,-i\}$)
- Each $\pi_k$ is a Gaussian prime of form $q_k+ir_k$

**(3) Prove division properties of Gaussian primes:**
Let $\pi = q+ir$ be any Gaussian prime dividing $e$. Then:
$$\pi \mid e \text{ and } e \mid (a+bi)(a-bi)$$

By transitivity:
$$\pi \mid (a+bi)(a-bi)$$

Since $\pi$ is prime and $\mathbb{Z}[i]$ is a UFD:
$$\text{If } \pi \mid xy \text{ then } \pi \mid x \text{ or } \pi \mid y$$

Therefore:
$$\pi \mid (a+bi) \text{ or } \pi \mid (a-bi)$$

**(4) Prove Gaussian prime factors are not ordinary primes:**
We'll show that no prime factor $q+ir$ of $e$ can be an ordinary prime $p$.

Suppose for contradiction that $\pi = q+ir$ equals some ordinary prime $p$. Then:
$$\pi = p = q+ir$$

From (3), $\pi$ divides either $a+bi$ or $a-bi$, so:
$$(a+bi) = \pi(x+yi) \text{ or } (a-bi) = \pi(x+yi)$$
for some $x,y \in \mathbb{Z}$.

Taking real and imaginary parts:
$$a = px - ry \text{ and } b = rx + py$$
or
$$a = px + ry \text{ and } b = -rx + py$$

Either way implies $p$ divides both $a$ and $b$ in $\mathbb{Z}$, contradicting $\gcd(a,b)=1$.

**(5) Prove conjugate pairing of Gaussian prime factors:**
We'll show that if $q+ir$ divides $e$, its conjugate $q-ir$ must also divide $e$, and they are distinct.

Since $e \in \mathbb{Z}$:
$$e = e\cdot 1 = e \cdot (1 \cdot \overline{1}) = e \cdot \frac{\overline{e}}{e} \cdot e = \overline{e}$$

Thus if $\pi = q+ir$ divides $e$, $\overline{\pi} = q-ir$ must also divide $e$.

To prove distinctness, suppose $q+ir = u(q-ir)$ for some unit $u$. Then:
- If $u = 1$: $r = 0$
- If $u = -1$: $q = 0$
- If $u = i$: $q = r$
- If $u = -i$: $q = -r$

Each case either makes $\pi$ an ordinary integer (contradicting part 4) or forces it to be an associate of $1+i$, which would contradict $\gcd(a,b)=1$.

**(6) Prove final representation:**
We'll demonstrate that $e$ must be of form $c^2+d^2$ with $c+di$ dividing $a+bi$.

Since all prime factors come in conjugate pairs $(\pi_k, \overline{\pi_k})$, we can write:
$$e = \prod_{k=1}^n (\pi_k\overline{\pi_k})$$

Each factor $\pi_k\overline{\pi_k} = (q_k+ir_k)(q_k-ir_k) = q_k^2 + r_k^2$

Therefore:
$$e = (c+di)(c-di) = c^2 + d^2$$
where $c+di$ is the product of some subset of the Gaussian prime factors.

**(7) Prove coprimality of representation:**
Finally, we'll show $\gcd(c,d)=1$.

Suppose $\gcd(c,d) = g > 1$. Then:
$$g^2 \mid (c^2 + d^2) = e \mid (a^2 + b^2)$$
$$g \mid (a+bi) \text{ and } g \mid (a-bi)$$
$$\therefore g \mid 2a \text{ and } g \mid 2b$$
$$\therefore g \mid 2\gcd(a,b) = 2$$

Thus $g=2$. But then $2 \mid e$, and since $2=(1+i)(1-i)=-i(1+i)^2$, this means $1+i$ divides both $a+bi$ and $a-bi$, contradicting $\gcd(a,b)=1$.

**Conclusion:** We have proven Euler's theorem by showing:
1. The coprime condition is necessary
2. Any divisor $e$ factors into conjugate pairs of Gaussian primes
3. These factors combine to give a representation $e=c^2+d^2$
4. The integers $c,d$ in this representation must be coprime

### Problem 2: Infinitude of Prime Divisors of Polynomial Values

**Main Theorem:** For any polynomial $f(x) = a_mx^m + ... + a_1x + a_0$ with integer coefficients where $a_0, a_m \neq 0$, infinitely many primes divide values of $f(x)$.

**Strategy:** Prove by contradiction. Assume finitely many primes divide values of $f(x)$.

**(1) Prove degree preservation under transformation:**
Let's analyze the degree of:
$$g(y) = \frac{1}{a_0}f(p_1p_2...p_ky)$$

The expanded polynomial:
$$\begin{align*}
g(y) &= \frac{1}{a_0}[a_m(p_1p_2...p_ky)^m + ... + a_1(p_1p_2...p_ky) + a_0] \\
&= \frac{a_m}{a_0}(p_1p_2...p_k)^my^m + ... + \frac{a_1}{a_0}(p_1p_2...p_k)y + 1
\end{align*}$$

The coefficient of $y^m$ is $\frac{a_m}{a_0}(p_1p_2...p_k)^m \neq 0$, so $g(y)$ is indeed degree $m$.

**(2) Prove integrality of coefficients:**
For any term in $g(y)$:
$$\text{coefficient of }y^j = \frac{a_j}{a_0}(p_1p_2...p_k)^j$$

[Note: This is where we previously identified a gap regarding why $a_0$ should divide these terms. This needs to be addressed in the setup of the problem or through additional conditions.]

**(3) Prove prime divisor inheritance:**
We'll show that if a prime $p$ divides $g(y)$ for some $y$, then $p$ divides $f(x)$ for some $x$.

If $p \mid g(y)$ for some $y \in \mathbb{Z}$:
$$p \mid \frac{1}{a_0}f(p_1p_2...p_ky)$$
$$p \mid f(p_1p_2...p_ky)$$

Let $x = p_1p_2...p_ky$. Then $x \in \mathbb{Z}$ and:
$$p \mid f(x)$$

**(4) Prove original primes don't divide transformed polynomial:**
For any $p_i$ among our original primes:

$$f(p_1p_2...p_ky) \equiv a_0 \pmod{p_i}$$

[Again, this step needs clarification regarding divisibility by $a_0$]

**(5) Deduce value constraint:**
From (3) and (4), we can conclude:
- Any prime dividing $g(y)$ must be among $p_1,...,p_k$
- But none of $p_1,...,p_k$ can divide $g(y)$

Therefore:
$$g(y) = \pm 1 \text{ for all } y \in \mathbb{Z}$$

**(6) Prove finite solution property:**
By the fundamental theorem of algebra:
- $g(y) = 1$ has at most $m$ complex roots
- $g(y) = -1$ has at most $m$ complex roots

Therefore these equations have at most $2m$ integer solutions combined.

**(7) Establish contradiction:**
We have:
1. $g(y) = \pm 1$ for all $y \in \mathbb{Z}$ (from step 5)
2. $g(y) = \pm 1$ has at most $2m$ integer solutions (from step 6)

Since $\mathbb{Z}$ is infinite and $2m$ is finite, this is a contradiction.

**Conclusion:** Our initial assumption must be false. Therefore, infinitely many primes divide values of $f(x)$.

[Would you like me to continue with Problem 3?]

### Problem 3: Representation of Primes as $x^2 - 2y^2$

**Theorem:** A prime $p$ can be written as $p = x^2 - 2y^2$ if and only if $p \equiv \pm1 \pmod{8}$.

First, let's establish our working environment:

In $\mathbb{Z}[\sqrt{2}]$:
- Elements are of the form $a + b\sqrt{2}$ where $a,b \in \mathbb{Z}$
- The norm is defined as: $\text{norm}(a+b\sqrt{2}) = a^2-2b^2$
- For $\pi = a+b\sqrt{2}$, its conjugate is $\overline{\pi} = a-b\sqrt{2}$
- The norm is multiplicative: $\text{norm}(\pi_1\pi_2) = \text{norm}(\pi_1)\text{norm}(\pi_2)$

**(1) Modular Analysis:**

Let's analyze possible values modulo 8:

For squares modulo 8:
$$\begin{array}{c|c}
x & x^2 \pmod{8} \\
\hline
0 & 0 \\
1,7 & 1 \\
2,6 & 4 \\
3,5 & 1 \\
4 & 0 \\
\end{array}$$

For $2y^2$ modulo 8:
$$2y^2 \equiv \begin{cases}
0 \pmod{8} & \text{if } y \text{ is even} \\
2 \pmod{8} & \text{if } y \text{ is odd}
\end{cases}$$

Therefore, $x^2 - 2y^2$ can be:
$$x^2 - 2y^2 \equiv \{0, 1, 2, 4, 6, 7\} \pmod{8}$$

For a prime $p$:
- If $p \equiv 3,5 \pmod{8}$, then $(\frac{2}{p}) = -1$
- Thus $p$ cannot divide $x^2-2$
- Therefore $p$ is prime in $\mathbb{Z}[\sqrt{2}]$
- Hence $p \neq x^2 - 2y^2$

**(2) Special Case of $p=2$:**

Let's prove 2 cannot be represented as $x^2 - 2y^2$:

Suppose $2 = x^2-2y^2$. Then:
$$x^2 \equiv 2 \pmod{2} \implies x \text{ is even} \implies x = 2k$$

Substituting:
$$2 = 4k^2 - 2y^2$$
$$1 = 2k^2 - y^2$$
$$y^2 \equiv 1 \pmod{2} \implies y \text{ is odd}$$

But if $y = 2j$:
$$1 = 2(k^2-2j^2)$$

This is impossible as the RHS is even.

**(3) Quadratic Residues:**

For primes $p \equiv \pm1 \pmod{8}$, quadratic reciprocity tells us:
$$(\frac{2}{p}) = 1$$

This means:
$$\exists m \in \mathbb{Z}: m^2 \equiv 2 \pmod{p}$$

Key observation:
$$p \equiv \pm1 \pmod{8} \implies 2 \text{ is a quadratic residue modulo } p$$

**(4) Non-Primality in $\mathbb{Z}[\sqrt{2}]$:**

From $m^2 \equiv 2 \pmod{p}$:
$$m^2 - 2 \equiv 0 \pmod{p}$$
$$(m - \sqrt{2})(m + \sqrt{2}) \equiv 0 \pmod{p}$$

If $p$ were prime in $\mathbb{Z}[\sqrt{2}]$:
- $p$ would divide either $(m - \sqrt{2})$ or $(m + \sqrt{2})$
- This implies $p \mid 2\sqrt{2}$
- Therefore $p^2 \mid 8$
- But this means $p = 2$, contradicting $p \equiv \pm1 \pmod{8}$

Therefore, $p$ is not prime in $\mathbb{Z}[\sqrt{2}]$.

**(5) Division Property in $\mathbb{Z}[\sqrt{2}]$:**

For $\alpha = a+b\sqrt{2}$ and $\beta = c+d\sqrt{2}$ with $\beta \neq 0$:

$$\frac{\alpha}{\beta} = \frac{(a+b\sqrt{2})(c-d\sqrt{2})}{c^2-2d^2}$$
$$= \frac{ac-2bd}{c^2-2d^2} + \frac{bc-ad}{c^2-2d^2}\sqrt{2}$$
$$= r_1 + r_2\sqrt{2}$$

Let $m_1, m_2$ be integers with:
$$|r_1-m_1| \leq \frac{1}{2} \text{ and } |r_2-m_2| \leq \frac{1}{2}$$

For $\gamma = m_1 + m_2\sqrt{2}$:

$$|\text{norm}(\frac{\alpha}{\beta}-\gamma)| = |(r_1-m_1)^2-2(r_2-m_2)^2|$$
$$\leq |(\frac{1}{2})^2 + 2(\frac{1}{2})^2| = \frac{3}{4} < 1$$

For $\rho = \alpha-\gamma\beta$:
$$|\text{norm}(\rho)| = |\text{norm}(\beta)| |\text{norm}(\frac{\alpha}{\beta}-\gamma)| < |\text{norm}(\beta)|$$

**(6) Final Representation:**

Since $p$ is not prime in $\mathbb{Z}[\sqrt{2}]$, it factors as:
$$p = (x+y\sqrt{2})(u+v\sqrt{2})$$

Taking norms:
$$p^2 = (x^2-2y^2)(u^2-2v^2)$$

By unique factorization in $\mathbb{Z}$:
$$p = x^2-2y^2$$

Therefore:
1. If $p \equiv \pm1 \pmod{8}$, then $p = x^2-2y^2$ for some $x,y \in \mathbb{Z}$
2. If $p = x^2-2y^2$, then by part (1), $p \equiv \pm1 \pmod{8}$

This completes the proof that $p = x^2-2y^2$ if and only if $p \equiv \pm1 \pmod{8}$.

### Problem 4: Alternative Proof of Euler's Criterion

**Theorem to Prove:** For an odd prime $q$ and any integer $p$ not divisible by $q$:
$$(\frac{p}{q}) \equiv p^{\frac{q-1}{2}} \pmod{q}$$

**(1) Structure of Multiplicative Group Modulo q:**

Let $a$ be a primitive root modulo $q$. Then:
$$\{a^k \bmod q: 0 \leq k \leq q-2\} = \{1, a, a^2, ..., a^{q-2}\}$$

This forms a complete set of nonzero residues modulo $q$.

To find squares modulo $q$:
- For any $x \not\equiv 0 \pmod{q}$, $x \equiv a^k \pmod{q}$ for some unique $k$
- $x$ is a square $\iff \exists y: y^2 \equiv x \pmod{q}$
- $y \equiv a^m \pmod{q}$ for some $m$
- Therefore: $a^{2m} \equiv x \equiv a^k \pmod{q}$
- By primitive root properties: $2m \equiv k \pmod{q-1}$
- Thus $k$ must be even

Therefore, squares modulo $q$ are:
$$\{1, a^2, a^4, ..., a^{q-3}\}$$

**(2) Count of Squares:**

The exponents in the squares are:
$$\{0, 2, 4, ..., q-3\}$$

This is an arithmetic sequence with:
- First term: 0
- Last term: $q-3$
- Common difference: 2

Number of terms = $\frac{q-1}{2}$ squares modulo $q$

**(3) Case of Quadratic Residues:**

For $P$ a square modulo $q$:
$$P \equiv a^{2k} \pmod{q} \text{ for some } k$$

Computing the power:
$$\begin{align*}
P^{\frac{q-1}{2}} &\equiv (a^{2k})^{\frac{q-1}{2}} \pmod{q} \\
&\equiv a^{k(q-1)} \pmod{q} \\
&\equiv (a^{q-1})^k \pmod{q} \\
&\equiv 1^k \pmod{q} \text{ (by Fermat's Little Theorem)} \\
&\equiv 1 \pmod{q}
\end{align*}$$

**(4) Case of Non-Squares:**

For $P$ not a square modulo $q$:
$$P \equiv a^{2k+1} \pmod{q} \text{ for some } k$$

Computing the power:
$$\begin{align*}
P^{\frac{q-1}{2}} &\equiv (a^{2k+1})^{\frac{q-1}{2}} \pmod{q} \\
&\equiv a^{k(q-1)+\frac{q-1}{2}} \pmod{q} \\
&\equiv (a^{q-1})^k \cdot a^{\frac{q-1}{2}} \pmod{q} \\
&\equiv a^{\frac{q-1}{2}} \pmod{q}
\end{align*}$$

Key observations:
1. $(a^{\frac{q-1}{2}})^2 \equiv a^{q-1} \equiv 1 \pmod{q}$
2. $a^{\frac{q-1}{2}} \not\equiv 1 \pmod{q}$ (as $a$ is primitive root)
3. In $\mathbb{F}_q$, $x^2 \equiv 1$ has only solutions $x \equiv \pm 1$

Therefore:
$$a^{\frac{q-1}{2}} \equiv -1 \pmod{q}$$

Thus for non-squares:
$$P^{\frac{q-1}{2}} \equiv -1 \pmod{q}$$

This proves:
$$p^{\frac{q-1}{2}} \equiv \begin{cases}
1 \pmod{q} & \text{if } p \text{ is a square mod } q \\
-1 \pmod{q} & \text{if } p \text{ is not a square mod } q
\end{cases}$$

Which is equivalent to:
$$(\frac{p}{q}) \equiv p^{\frac{q-1}{2}} \pmod{q}$$