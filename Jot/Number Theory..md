## Homework for the Week of November 11th.

### Problem 1. The goal of this exercise is to show how Z[√2] sheds light on sum of two squares in other ways than what we've done so far.

Namely, we show the following theorem of Euler: If a,b are integers with gcd(a,b)=1, then any divisor of a²+b² is of the form c²+d² with gcd(c,d)=1.

1. Give an example that shows why the condition gcd(a,b)=1 is necessary.

If $\gcd(a,b) \neq 1$, the theorem doesn't hold.  For example, let $a = 2$ and $b = 4$. Then $\gcd(a, b) = 2$.  We have $a^2 + b^2 = 20$, and $4$ is a divisor of $20$.  However, $4$ can only be expressed as $c^2 + d^2$ if $c=2, d=0$ or $c=0, d=2$.  If we require $\gcd(c, d) = 1$, then $4$ is not expressible in the required form.

2. Let e>1 be an integer divisor of a²+b². Show that e is a product of Gaussian prime divisors q+ir up to units.

We can factor $a^2 + b^2$ in $\mathbb{Z}[i]$ as $(a + bi)(a - bi)$.  Let $e$ be a divisor of $a^2 + b^2$ in $\mathbb{Z}$. Then $e$ is also a divisor of $(a + bi)(a - bi)$ in $\mathbb{Z}[i]$. By unique prime factorization in $\mathbb{Z}[i]$, $e$ can be written as a product of Gaussian primes: $e = \pi_1 \pi_2 \cdots \pi_n$.

3. Show that each of the Gaussian primes q+ir divide either a+ib or a-ib.

Since $e | (a+bi)(a-bi)$, each Gaussian prime $\pi_k$ dividing $e$ must also divide $(a+bi)(a-bi)$. Because $\pi_k$ is a Gaussian prime, it must divide either $a+bi$ or $a-bi$.

4. Deduce from 3: that none of the Gaussian primes q+ir is an ordinary (in Z) prime.

Suppose, for contradiction, that a Gaussian prime $\pi = q + ir$ is also an ordinary prime $p$. Since $\pi | a+bi$ or $\pi | a-bi$, we have $p | a+bi$ or $p | a-bi$. This implies $p|a$ and $p|b$ in $\mathbb{Z}$, contradicting $\gcd(a, b) = 1$.  Therefore, $\pi$ cannot be an ordinary prime.

5. Show that if q+ir is a Gaussian prime dividing e, then its conjugate q-ir is also a factor {distinct from q+ir}.

Let $e$ be a divisor of $a^2+b^2$. If a Gaussian prime $\pi = q + ir$ divides $e$, then its conjugate $\overline{\pi} = q - ir$ must also divide $e$. This is because $e$ is a real integer, and the conjugate of any factor of $e$ must also be a factor of $e$.  These factors are distinct. If they were not distinct, then $q + ir = u(q - ir)$ for some unit $u \in \{1, -1, i, -i\}$. This implies either $r=0$ (if $u=1$) or $q=0$ (if $u=-1$), making $\pi$ or its associate equal to an ordinary integer, which we ruled out in step 4. The case where $q + ir$ is an associate of $1+i$ is more subtle. If both $a+bi$ and $a-bi$ are divisible by $1+i$, then both $a$ and $b$ are odd or both are even which contradicts $\gcd(a,b)=1$.  Thus the prime factors of $e$ come in distinct conjugate pairs, or are equal to $1+i$.

6. Deduce from 5: that e is of the form c²+d² where c+di divides a+bi.

Since $e$ is a product of Gaussian primes and their conjugates, we can write $e$ as $(c+di)(c-di) = c^2+d^2$, where $c+di$ is a product of some of the Gaussian primes dividing $e$.

7. Deduce from 6: that gcd(c,d)=1.

Suppose $\gcd(c, d) = g > 1$. Then $g^2 | c^2 + d^2 = e$, so $g | a+bi$ and $g | a-bi$.  This implies $g|2a$ and $g|2b$, so $g | 2\gcd(a, b) = 2$. Therefore, $g=2$. This implies $2 | e$, and since $2=(1+i)(1-i)=-i(1+i)^2$, the prime $1+i$ divides $a+ib$ and $a-ib$ which again contradicts $\gcd(a,b)=1$ as shown above.  Therefore, $\gcd(c, d) = 1$.

### Problem 2. Recall that to show there are infinitely many primes p ≡ 1 (mod 4), we showed there are infinitely many primes p that divide a value of the form x²+1. We now generalize this.

Let $f(x) = a_mx^m + ... + a_1x + a_0$, $a_0,...,a_m \in \mathbb{Z}$, $a_0\neq0$, $a_m\neq0$.

1. Show that g is of degree m.

Assume, for the sake of contradiction, that only finitely many primes $p_1, \dots, p_k$ divide values of $f(x)$ for $x \in \mathbb{Z}$. We can also assume that no prime dividing $a_m$ divides $f(x)$ for any integer $x$ (if this were the case, we could divide $f(x)$ by $a_m$ to obtain a new polynomial with the same set of prime divisors and a constant leading coefficient). Also, if $a_0 = 0$ then $f(p_1 \dots p_k)$ is composite, divisible by $p_1 \dots p_k$. Then $f(2p_1 \dots p_k)$ will be divisible by a prime not among $p_1, \dots, p_k$, contradicting the assumption. So we can assume $a_0 \neq 0$ and that $\gcd(a_0, a_m, p_1, \dots, p_k) = 1$.

2. Show that g(y) has integer coefficients.

Define $g(y) = \frac{1}{a_m}f(a_m p_1 \dots p_k y)$.  Since $f(x)$ has integer coefficients, the constant term of $f(a_m p_1 \dots p_k y)$ is $a_0$, and all other terms are divisible by $a_m$. Therefore, $g(y)$ has integer coefficients. Furthermore, $g(y)$ has the same degree $m$ as $f(x)$.

3. Show that if p|g(y) for some y∈Z, then p|f(x) for some x∈Z.

If a prime $p$ divides $g(y)$ for some $y \in \mathbb{Z}$, then $p | f(a_m p_1 \dots p_k y)$.  Letting $x = a_m p_1 \dots p_k y$, we see that $p | f(x)$ for some $x \in \mathbb{Z}$.

4. Show that none of p₁,...,pk divide g(y) when y∈Z.

Consider $f(a_m p_1 \dots p_k y) \pmod{p_i}$. We have
$$f(a_m p_1 \dots p_k y) \equiv a_0 \pmod{p_i}\text{.}$$
Since $\gcd(a_0, p_i) = 1$, $p_i$ does not divide $f(a_m p_1 \dots p_k y)$. As $p_i$ does not divide $a_m$ either, it follows that $p_i$ does not divide $g(y) = \frac{1}{a_m}f(a_m p_1 \dots p_k y)$.

5. Conclude from 3&4: that g(y)=±1.

From step 3, any prime dividing $g(y)$ must also divide a value of $f(x)$. From step 4, none of the primes $p_1, \dots, p_k$ divide $g(y)$. Thus, $g(y)$ must equal $\pm 1$ for all $y \in \mathbb{Z}$.

6. Show that g(y)=1 & g(y)=-1 have only finitely many solutions.

Since $g(y)$ is a non-constant polynomial of degree $m$ with integer coefficients, the equations $g(y) = 1$ and $g(y) = -1$ each have at most $m$ integer solutions.

7. Show that 6. contradicts 5.

Step 5 asserts that $g(y) = \pm 1$ for all integers $y$, while step 6 states that these equations have at most $m$ integer solutions each. Since there are infinitely many integers $y$, this is a contradiction.

8. Conclude.

The contradiction arises from assuming that only finitely many primes divide values of $f(x)$. Therefore, infinitely many primes must divide values of $f(x)$.

