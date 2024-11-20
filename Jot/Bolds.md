Let me break this down:

1. First, we need to understand what $(\frac{2}{p}) = -1$ means:
   - It means 2 is not a quadratic residue modulo $p$
   - In other words, there is no solution to $x^2 \equiv 2 \pmod{p}$

2. If $p$ divides $x^2-2$, then:
   - $x^2 \equiv 2 \pmod{p}$
   - But we just said this is impossible when $(\frac{2}{p}) = -1$
   - Therefore $p$ cannot divide $x^2-2$

3. Next key fact: if $p$ is not prime in $\mathbb{Z}[\sqrt{2}]$, then $p$ must divide $x^2-2$ for some $x$
   - Because being not prime means $p$ factors non-trivially in $\mathbb{Z}[\sqrt{2}]$
   - Any such factorization would give $p = x^2-2y^2$ for some $x,y$
   - This means $p$ divides $x^2-2y^2$
   - Which means $p$ divides $x^2-2$ for some $x$

4. Therefore:
   - Since $p$ cannot divide $x^2-2$ (from step 2)
   - $p$ must be prime in $\mathbb{Z}[\sqrt{2}]$ (from step 3)
   - And thus $p$ cannot be written as $x^2-2y^2$

Would you like me to clarify any of these steps further?