**(1) To characterize squares modulo q:** Prove that with a primitive root $a \bmod q$, the squares modulo $q$ are exactly $\{1, a^2, a^4, ..., a^{q-3}\}$ by:
1. Using that every nonzero residue is some power of $a$
2. Showing $x$ is a square if and only if its exponent as a power of $a$ is even

**(2) To count distinct squares:** Prove there are exactly $\frac{q-1}{2}$ squares modulo $q$ by:
1. Showing the exponents of squares form arithmetic sequence $\{0,2,4,...,q-3\}$
2. Computing the number of terms in this sequence

**(3) To evaluate powers of squares:** For any square $P \equiv a^{2k} \pmod{q}$, prove that $P^{\frac{q-1}{2}} \equiv 1 \pmod{q}$ by:
1. Computing $(a^{2k})^{\frac{q-1}{2}}$
2. Using Fermat's Little Theorem to simplify

**(4) To evaluate powers of non-squares:** For any non-square $P \equiv a^{2k+1} \pmod{q}$, prove that $P^{\frac{q-1}{2}} \equiv -1 \pmod{q}$ by:
1. Computing $(a^{2k+1})^{\frac{q-1}{2}}$
2. Showing $a^{\frac{q-1}{2}} \equiv -1 \pmod{q}$ using that $a$ is a primitive root
3. Concluding that this establishes Euler's criterion $(\frac{p}{q}) \equiv p^{\frac{q-1}{2}} \pmod{q}$