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

Let me clarify:

The statement should be about congruences modulo 8, not modulo p. Specifically:

If $p$ is a prime and $p \equiv 3 \text{ or } 5 \pmod{8}$, then $(\frac{2}{p}) = -1$

This comes from the quadratic reciprocity formula for $(\frac{2}{p})$, which states:
$$(\frac{2}{p}) = (-1)^{\frac{p^2-1}{8}}$$

When you plug in:
- If $p \equiv 3 \pmod{8}$, then $\frac{p^2-1}{8} = \frac{9-1}{8} = 1$ (odd)
- If $p \equiv 5 \pmod{8}$, then $\frac{p^2-1}{8} = \frac{25-1}{8} = 3$ (odd)

So in both cases, $(\frac{2}{p}) = -1$

This is crucial because we're trying to characterize which primes can be written as $x^2-2y^2$. The fact that primes congruent to 3 or 5 modulo 8 make 2 a non-quadratic residue tells us these primes cannot be represented in this form.

Is this clearer? Would you like me to elaborate on any part?