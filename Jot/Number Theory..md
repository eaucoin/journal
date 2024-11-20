## Homework for the Week of November 11th.

### Problem 1: Euler's Theorem on Sum of Two Squares in $\mathbb{Z}[i]$

**Theorem (Euler):** If $a,b \in \mathbb{Z}$ with $\gcd(a,b)=1$, then any divisor of $a^2+b^2$ is of the form $c^2+d^2$ where $c,d \in \mathbb{Z}$ with $\gcd(c,d)=1$.

**(1) To justify the coprime condition:** Show that when $\gcd(a,b)\neq 1$, the theorem can fail by finding specific integers $a,b$ where some divisor of $a^2+b^2$ cannot be written as $c^2+d^2$ with $\gcd(c,d)=1$.**

Let's examine why this condition is crucial through a counterexample:

Take $a=2$ and $b=4$. Here:
$$\gcd(2,4) = 2 \neq 1$$
$$a^2 + b^2 = 2^2 + 4^2 = 4 + 16 = 20$$

Now, 4 is a divisor of 20. If the theorem were true without the coprime condition, 4 would need to be expressible as $c^2 + d^2$ with $\gcd(c,d)=1$. However:

- The only ways to express 4 as a sum of squares are:
$$4 = 2^2 + 0^2 = 0^2 + 2^2$$
In both cases, $\gcd(c,d) = 2 \neq 1$

**(2) To begin factorization:** Show that any divisor $e>1$ of $a^2+b^2$ can be written as $e = u\pi_1\pi_2...\pi_n$ where $u$ is a unit in $\mathbb{Z}[i]$ and each $\pi_k$ is a Gaussian prime, by using the factorization $a^2+b^2=(a+bi)(a-bi)$ in $\mathbb{Z}[i]$.**

First, observe that in $\mathbb{Z}[i]$:
$$a^2 + b^2 = (a+bi)(a-bi)$$

Let $e$ be a divisor of $a^2+b^2$ where $e > 1$. By the fundamental theorem of arithmetic in $\mathbb{Z}[i]$ (which is a unique factorization domain), we can write:
$$e = u\pi_1\pi_2...\pi_n$$
where:
- $u$ is a unit in $\mathbb{Z}[i]$ (one of $\{1,-1,i,-i\}$)
- Each $\pi_k$ is a Gaussian prime of the form $q_k+ir_k$

**(3) To establish key division property:** Prove that for any Gaussian prime $\pi$ dividing $e$, either $\pi \mid (a+bi)$ or $\pi \mid (a-bi)$ but not both (as this would contradict $\gcd(a,b)=1$).

Let $\pi = q+ir$ be any Gaussian prime dividing $e$. Then:
$$\pi \mid e \text{ and } e \mid (a+bi)(a-bi)$$

By the transitivity of division:
$$\pi \mid (a+bi)(a-bi)$$

Since $\pi$ is prime in $\mathbb{Z}[i]$ and $\mathbb{Z}[i]$ is a unique factorization domain, by the prime property:
$$\text{If } \pi \mid xy \text{ then } \pi \mid x \text{ or } \pi \mid y$$

Therefore:
$$\pi \mid (a+bi) \text{ or } \pi \mid (a-bi)$$

**(4) To restrict prime factors:** Prove that no Gaussian prime $\pi=q+ir$ dividing $e$ can be an ordinary prime $p$ in $\mathbb{Z}$, as this would force $p \mid \gcd(a,b)=1$.

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

**(5) To pair prime factors:** Show that if $\pi=q+ir$ divides $e$, then its conjugate $\overline{\pi}=q-ir$ also divides $e$, and prove these factors must be distinct when $\gcd(a,b)=1$.

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

**(6) To obtain desired form:** Use the conjugate pairing of prime factors to prove $e=(c+di)(c-di)=c^2+d^2$ for some $c,d \in \mathbb{Z}$.

Since all prime factors of $e$ come in conjugate pairs $(\pi_k, \overline{\pi_k})$, we can group them:
$$e = \prod_{k=1}^n (\pi_k\overline{\pi_k})$$

Each factor $\pi_k\overline{\pi_k} = (q_k+ir_k)(q_k-ir_k) = q_k^2 + r_k^2$

Therefore:
$$e = (c+di)(c-di) = c^2 + d^2$$
where $c+di$ is the product of some subset of the Gaussian prime factors.

**(7) To complete the theorem:** Prove that the integers $c,d$ in the representation $e=c^2+d^2$ must satisfy $\gcd(c,d)=1$ by showing any common factor would force a contradiction with $\gcd(a,b)=1$.

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

### Problem 2: Infinitude of Primes Dividing Polynomial Values

**Main Theorem:** For any polynomial $f(x) = a_mx^m + ... + a_1x + a_0$ with integer coefficients where $a_0, a_m \neq 0$, infinitely many primes divide values of $f(x)$.

**(1) To analyze the key auxiliary polynomial:** For $g(y) = \frac{1}{a_0}f(a_0p_1p_2...p_ky)$, prove it has the same degree $m$ as $f(x)$ by showing its leading coefficient is nonzero.

Let's assume for contradiction that only finitely many primes $p_1, p_2, ..., p_k$ divide values of $f(x)$ for $x \in \mathbb{Z}$.

Expanding $g(y)$:
$$\begin{align*}
g(y) &= \frac{1}{a_0}[a_m(a_0p_1p_2...p_ky)^m + ... + a_1(a_0p_1p_2...p_ky) + a_0] \\
&= a_m(p_1p_2...p_k)^m(a_0)^{m-1}y^m + ... + a_1p_1p_2...p_ky + 1
\end{align*}$$

The coefficient of $y^m$ is $a_m(p_1p_2...p_k)^m(a_0)^{m-1} \neq 0$, so $g(y)$ has degree $m$.

**(2) To establish well-definedness:** Prove that $g(y)$ has integer coefficients by showing each coefficient is an integer.

For any term $y^j$ in $g(y)$, its coefficient is:
$$a_j(p_1p_2...p_k)^j(a_0)^{j-1}$$

Since $j \geq 1$ for all terms except the constant term (which is 1), all coefficients are integers.

**(3) To connect prime factors:** Prove that if a prime $p$ divides $g(y)$ for some $y \in \mathbb{Z}$, then $p$ must divide $f(x)$ for some $x \in \mathbb{Z}$, by explicitly constructing such an $x$.

Let $p$ be a prime dividing $g(y)$ for some $y \in \mathbb{Z}$. Then:
$$p \mid g(y) = \frac{1}{a_0}f(a_0p_1p_2...p_ky)$$
$$\therefore p \mid f(a_0p_1p_2...p_ky)$$

Let $x = a_0p_1p_2...p_ky$. Then $x \in \mathbb{Z}$ and:
$$p \mid f(x)$$

**(4) To exclude original primes:** Show that none of the original primes $p_1,...,p_k$ can divide any value of $g(y)$ by proving $g(y) \equiv 1 \pmod{p_i}$ for all $y$ and all $i$.

For any $p_i$ among our original primes:
$$f(a_0p_1p_2...p_ky) \equiv a_0 \pmod{p_i}$$
since every term except the constant term contains $p_i$ as a factor.

Therefore:
$$g(y) = \frac{1}{a_0}f(a_0p_1p_2...p_ky) \equiv \frac{1}{a_0}a_0 \equiv 1 \pmod{p_i}$$

Thus, $p_i \nmid g(y)$ for any $y \in \mathbb{Z}$.

**(5) To restrict possible values:** Use results from (3) and (4) to prove that $g(y)$ can only take values $\pm 1$ for all $y \in \mathbb{Z}$.

From (3), if any prime $p$ divides $g(y)$, then $p$ must divide some value of $f(x)$, making $p$ one of the original primes $p_1,...,p_k$.

However, from (4), none of $p_1,...,p_k$ can divide any value of $g(y)$.

Therefore, no prime can divide $g(y)$, meaning:
$$g(y) = \pm 1 \text{ for all } y \in \mathbb{Z}$$

**(6) To bound solutions:** Show that the equations $g(y)=1$ and $g(y)=-1$ have at most $2m$ integer solutions combined, using the fact that $g$ has degree $m$.

The polynomial $g(y)$ has degree $m$, so by the fundamental theorem of algebra:
- The equation $g(y) = 1$ has at most $m$ complex roots
- The equation $g(y) = -1$ has at most $m$ complex roots

Therefore, the equations $g(y) = \pm 1$ have at most $2m$ integer solutions combined.

**(7) To reach contradiction:** Show that the statements "$g(y)=\pm 1$ for all $y \in \mathbb{Z}$" and "$g(y)=\pm 1$ has at most $2m$ solutions" are mutually contradictory.

We have proven:
1. $g(y) = \pm 1$ for all $y \in \mathbb{Z}$ (from step 5)
2. The equations $g(y) = \pm 1$ have at most $2m$ integer solutions combined (from step 6)

Since $\mathbb{Z}$ is infinite and $2m$ is finite, these statements contradict each other.

**(8) To complete the proof:** Conclude that the original assumption must be false, proving there are infinitely many primes dividing values of $f(x)$.

The contradiction in (7) proves our initial assumption (that only finitely many primes divide values of $f(x)$) must be false.

Therefore:
$$\text{There are infinitely many primes } p \text{ that divide values of } f(x)$$

This generalizes our earlier proof about primes $p \equiv 1 \pmod{4}$, where we used $f(x) = x^2 + 1$.

### Problem 3: Representation of Primes as $x^2 - 2y^2$

**Theorem:** A prime $p$ can be written as $p = x^2 - 2y^2$ if and only if $p \equiv \pm1 \pmod{8}$.

First, let's establish our working environment:

In $\mathbb{Z}[\sqrt{2}]$:
- Elements are of the form $a + b\sqrt{2}$ where $a,b \in \mathbb{Z}$
- The norm is defined as: $\text{norm}(a+b\sqrt{2}) = a^2-2b^2$
- For $\pi = a+b\sqrt{2}$, its conjugate is $\overline{\pi} = a-b\sqrt{2}$
- The norm is multiplicative: $\text{norm}(\pi_1\pi_2) = \text{norm}(\pi_1)\text{norm}(\pi_2)$

**(1) To restrict possible prime values:** Prove that if a prime $p$ is of the form $x^2-2y^2$, then $p \equiv \pm1 \pmod{8}$ by:
1. Analyzing all possible values of $x^2 \pmod{8}$
2. Analyzing all possible values of $2y^2 \pmod{8}$
3. Showing that for primes $p \equiv 3,5 \pmod{8}$, $p$ must be prime in $\mathbb{Z}[\sqrt{2}]$

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

**(2) To exclude $p=2$ case:** Prove that 2 cannot be represented as $x^2-2y^2$ by showing any such representation leads to a contradiction modulo 2.**

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

**(3) To begin reverse implication:** For primes $p \equiv \pm1 \pmod{8}$, prove that 2 is a quadratic residue modulo $p$ using quadratic reciprocity, yielding an integer $m$ where $m^2 \equiv 2 \pmod{p}$.

For primes $p \equiv \pm1 \pmod{8}$, quadratic reciprocity tells us:
$$(\frac{2}{p}) = 1$$

This means:
$$\exists m \in \mathbb{Z}: m^2 \equiv 2 \pmod{p}$$

Key observation:
$$p \equiv \pm1 \pmod{8} \implies 2 \text{ is a quadratic residue modulo } p$$

**(4) To show factorization in $\mathbb{Z}[\sqrt{2}]$:** Use the quadratic residue from (3) to prove that $p$ cannot be prime in $\mathbb{Z}[\sqrt{2}]$ by showing it would lead to $p=2$, contradicting $p \equiv \pm1 \pmod{8}$.

From $m^2 \equiv 2 \pmod{p}$:
$$m^2 - 2 \equiv 0 \pmod{p}$$
$$(m - \sqrt{2})(m + \sqrt{2}) \equiv 0 \pmod{p}$$

If $p$ were prime in $\mathbb{Z}[\sqrt{2}]$:
- $p$ would divide either $(m - \sqrt{2})$ or $(m + \sqrt{2})$
- This implies $p \mid 2\sqrt{2}$
- Therefore $p^2 \mid 8$
- But this means $p = 2$, contradicting $p \equiv \pm1 \pmod{8}$

Therefore, $p$ is not prime in $\mathbb{Z}[\sqrt{2}]$.

**(5) To establish division algorithm:** Prove that $\mathbb{Z}[\sqrt{2}]$ has the division property by explicitly constructing remainders with norm less than the divisor's norm.**

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

**(6) To complete representation:** Use the non-primality from (4) to factor $p$ in $\mathbb{Z}[\sqrt{2}]$ and prove this factorization yields a representation $p=x^2-2y^2$, completing the proof that $p \equiv \pm1 \pmod{8}$ implies $p=x^2-2y^2$.

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

**(1) To characterize squares modulo q:** Prove that with a primitive root $a \bmod q$, the squares modulo $q$ are exactly $\{1, a^2, a^4, ..., a^{q-3}\}$ by:
1. Using that every nonzero residue is some power of $a$
2. Showing $x$ is a square if and only if its exponent as a power of $a$ is even

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

**(2) To count distinct squares:** Prove there are exactly $\frac{q-1}{2}$ squares modulo $q$ by:
1. Showing the exponents of squares form arithmetic sequence $\{0,2,4,...,q-3\}$
2. Computing the number of terms in this sequence

The exponents in the squares are:
$$\{0, 2, 4, ..., q-3\}$$

This is an arithmetic sequence with:
- First term: 0
- Last term: $q-3$
- Common difference: 2

Number of terms = $\frac{q-1}{2}$ squares modulo $q$

**(3) To evaluate powers of squares:** For any square $P \equiv a^{2k} \pmod{q}$, prove that $P^{\frac{q-1}{2}} \equiv 1 \pmod{q}$ by:
1. Computing $(a^{2k})^{\frac{q-1}{2}}$
2. Using Fermat's Little Theorem to simplify

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

**(4) To evaluate powers of non-squares:** For any non-square $P \equiv a^{2k+1} \pmod{q}$, prove that $P^{\frac{q-1}{2}} \equiv -1 \pmod{q}$ by:
1. Computing $(a^{2k+1})^{\frac{q-1}{2}}$
2. Showing $a^{\frac{q-1}{2}} \equiv -1 \pmod{q}$ using that $a$ is a primitive root
3. Concluding that this establishes Euler's criterion $(\frac{p}{q}) \equiv p^{\frac{q-1}{2}} \pmod{q}$

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