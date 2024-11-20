Let me work this through:

If $2 = x^2-2y^2$, then working mod 2:
1. $0 \equiv x^2-0 \pmod{2}$ (since $2y^2 \equiv 0 \pmod{2}$)
2. $0 \equiv x^2 \pmod{2}$
3. So $x \equiv 0 \pmod{2}$, meaning $x$ is even
4. Let $x = 2k$
5. Then $2 = 4k^2-2y^2$
6. So $1 = 2k^2-y^2$
7. Therefore $y^2 = 2k^2-1$

Ah! Here's the key:
- The RHS is always odd (even - 1)
- But any value of $y^2$ is ≥ 0
- So $2k^2$ must be > 1
- Therefore $2k^2 \geq 2$
- So $y^2 \geq 1$
- Then the original equation would give us:
  $2 = 4k^2-2y^2 \leq 4k^2-2 = 2(2k^2-1)$
- But this says 2 is at least twice something positive...

I feel like I'm getting closer but still not quite seeing the clear contradiction using divisibility. Can you help me see what I'm missing?