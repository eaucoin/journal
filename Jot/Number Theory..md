## Problem 1 (Practice Long Division):

To compute the long division of $\alpha$ by $\beta$, where:

1. $\alpha = 5+i$, $\beta = 3-i$

**Solution.** 

$$\begin{align*}
\frac{5+i}{3-i}&=\frac{(5+i)(3+i)}{(3-i)(3+i)}\\
&=\frac{14+8i}{10}\\
&=\frac{7}{5}+\frac{4}{5}i\\
&\implies \mu=1+i\\
&\implies \mu\beta=(1+i)(3-i)=4+2i\\
&\implies \mu\beta + \rho=(1+i)(3-i)+(1-i)
\end{align*}$$

3. $\alpha = 2+14i$, $\beta = 3+5i$

**Solution.**

$$\begin{align*}
\frac{2+14i}{3+5i}&=\frac{(2+14i)(3-5i)}{(3+5i)(3-5i)}\\
&=\frac{32i+76}{34}\\
&=\frac{16}{17}+\frac{38}{17}i\\
&\implies \mu=1+2i\\
&\implies \mu\beta=(1+2i)(3+5i)=11i-7\\
&\implies \mu\beta + \rho=(1+2i)(2+14i)+(9-3i)
\end{align*}$$

## Problem 2 (Units in $\mathbb{Z}[\sqrt{2}]$):

Recall that $\mathbb{Z}[\sqrt{2}] := \{a+b\sqrt{2} ; a,b\in \mathbb{Z}\}$ with the usual addition and multiplication.

1. We define $\pi \in \mathbb{Z}[\sqrt{2}]$ to be a unit if there exists $\pi_2 \in \mathbb{Z}[\sqrt{2}]$ such that $\pi_1\pi_2 = 1$.

   Show that $3-2\sqrt{2}$ is a unit.

**Solution.**

$$\begin{align*}

(3-2\sqrt2)(a+b\sqrt2)&=
3a+3b\sqrt2 -2a\sqrt2-4b\\
&=(3a-4b)+(3b-2a)\sqrt 2\\
&=1\\
&\iff3a-4b=1\\
&\wedge\;\;\;\;\;\;3b-2a=0\\
&\iff 6a-8b=2\\
&\wedge\;\;\;\;\;\;9b=6a\\
&\iff b=2\\
&\wedge\;\;\;\;\;\;a=3\\

\end{align*}$$

2. Define $norm(a+b\sqrt{2}) = a^2-2b^2$.
   
   Prove that $a+b\sqrt{2}$ is a unit if and only if $norm(a+b\sqrt{2}) = \pm 1$.

**Solution.**

$$$$

3. Show that for all $n \geq 0$, $(3-2\sqrt{2})^n$ is a unit:
   
   (i) using 1, 2 the definition of a unit
   
   (ii)

4. Prove that $norm(\pi_1\pi_2) = norm(\pi_1)norm(\pi_2)$

5. Show that for all $n \geq 0$, $(3-2\sqrt{2})^n$ is a unit using 1., 2. & 4.

   Articulate your justification(s)!

## Problem 3: Factorize the following in $\mathbb{Z}[\sqrt{2}]$ (into product of Gaussian primes)

1. 17
2. 53
3. 39
4. 57

## Problem 4 (Primes in $\mathbb{Z}[\sqrt{-3}]$):

Recall that in $\mathbb{Z}[i]$, a prime $\pi|\alpha\beta$ implies that $\pi|\alpha$ or $\pi|\beta$. In $\mathbb{Z}[\sqrt{-3}]$, define a "prime" $\pi$ to be an element that cannot be written as $\pi = \alpha\beta$ with $\alpha$ & $\beta$ nonunits.

1. Define $norm(a+b\sqrt{-3}) = a^2+3b^2$. Prove that 
   $norm(\pi_1\pi_2) = norm(\pi_1)norm(\pi_2)$.

2. Prove that $\pi \in \mathbb{Z}[\sqrt{-3}]$ is a unit if and only if $norm(\pi) = 1$.

3. Prove that if $norm(\pi)$ is a prime in $\mathbb{N}$, then $\pi$ is "prime" in $\mathbb{Z}[\sqrt{-3}]$.

4. Prove that 2 is "prime" in $\mathbb{Z}[\sqrt{-3}]$.

5. Show that $2|(1+\sqrt{-3})(1-\sqrt{-3})$.

6. Conclude that $\mathbb{Z}[\sqrt{-3}]$ does not have the property that for "primes", $\pi|\alpha\beta \Rightarrow \pi|\alpha$ or $\pi|\beta$.

Remark: The reason I put "prime" in quotes is because when this property doesn't hold, we stop calling $\pi$ a prime, and we call it irreducible. This is just for your own benefit if you end up learning ring theory or algebraic number theory.

## Problem 5:

1. Write the law of quadratic reciprocity
2. Write the "strong multiplicativity" symbol
3. Write $(\frac{1}{q})$ & $(\frac{2}{q})$. (Evaluate and recall their values)
4. Compute $(\frac{55}{89})$, $(\frac{56}{89})$, $(\frac{23}{59})$

## Problem 6:

Using quadratic reciprocity & the Chinese remainder theorem, show that

$$\left(\frac{3}{q}\right) = \begin{cases} 
1; & q \equiv 1,11 \pmod{12} \\
-1; & q \equiv 5,7 \pmod{12}
\end{cases}$$

## Problem 7: Alternative Proof to $(p-1)! \equiv -1 \pmod{p}$

Let $p$ be an odd prime, $g$ is a primitive root of $p$.

1. Show that $(p-1)! \equiv g^{\frac{p(p-1)}{2}} \pmod{p}$
2. Show that $g^p \equiv g \pmod{p}$
3. Show that $g^{\frac{p-1}{2}} \equiv -1 \pmod{p}$
4. Conclude that $(p-1)! \equiv -1 \pmod{p}$