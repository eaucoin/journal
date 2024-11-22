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

$$\begin{align*}

&(\exists \pi^{-1}\in\mathbb{Z}[\sqrt 2])(\pi\pi^{-1}=1)\\
\implies& \text{norm}(\pi\pi^{-1})=1\\
\implies& \text{norm}(\pi)\text{norm}(\pi^{-1})=1\\
\implies& \text{norm}(\pi)\;|\;1\\
\implies& \text{norm}(\pi)=\pm1
\text{,}
\end{align*}$$
and:
$$\begin{align*}

&\text{norm}(\pi)=\pm1\\
\implies& \pi\bar{\pi}=\pm1\\
\implies& \pi\;|\;1\\
\implies& \pi\text{ is  invertible}

\end{align*}$$

3. Show that for all $n \geq 0$, $(3-2\sqrt{2})^n$ is a unit, using **(1)** and the definition of a unit.

**(1)** shows a base case. The $n$th case is that
$$(\exists\pi\in\mathbb{Z}[\sqrt2])(\pi(3-2\sqrt2)^{n}=1)\text{.}$$
Now, let $\lambda=\pi(3+2\sqrt2)$. We have two facts:
- $\lambda\in\mathbb{Z}[\sqrt2]$
- By **(1)**, $\lambda(3-2\sqrt2)=\lambda$.

From here, our $(n+1)^{\text{th}}$ case presents as
$$\begin{align*}

\lambda(3-2\sqrt2)^{n+1}&=\pi(3-2\sqrt2)^{n}(3-2\sqrt2)(3+2\sqrt2)\\
&=(1)(1)\\
&=1

\end{align*}$$

4. Prove that $norm(\pi_1\pi_2) = norm(\pi_1)norm(\pi_2)$

$$\begin{align*}

\text{norm}(\pi_1\pi_2)&=\text{norm}((a_1+a_2\sqrt2)(b_1+b_2\sqrt2))\\
&=\text{norm}(a_1b_1+2a_2b_2+(a_1b_2+a_2b_1)\sqrt2)\\
&=(a_1b_1+2a_2b_2)^{2}-2(a_1b_2+a_2b_1)^{2}\\
&=a_1^2 b_1^2 - 2 a_2^2 b_1^2 - 2 a_1^2 b_2^2 + 4 a_2^2 b_2^2\text{,}

\end{align*}$$
and:
$$\begin{align*}

\text{norm}(\pi_1)\text{norm}(\pi_2)&=\text{norm}(a_1+a_2\sqrt2)\text{norm}(b_1+b_2\sqrt2)\\
&=(a_1^2-2a_2^2)(b_1^2-2b_2^2)\\
&=a_1^2 b_1^2 - 2 a_2^2 b_1^2 - 2 a_1^2 b_2^2 + 4 a_2^2 b_2^2\text{.}

\end{align*}$$

6. Show that for all $n \geq 0$, $(3-2\sqrt{2})^n$ is a unit using 1., 2. & 4.

   Articulate your justification(s)!

## Problem 3: Factorize the following in $\mathbb{Z}[\sqrt{2}]$ (into product of Gaussian primes)

1. 17

$$\begin{align*}

17=(4+i)(4-i)

\end{align*}$$

3. 53

$$53=(7+2i)(7-2i)$$

5. 39

$$\begin{align*}

39&=3(13)\\
&=3(3+2i)(3-2i)

\end{align*}$$

7. 57

$$\begin{align*}

57&=3(19)\\


\end{align*}$$

## Problem 4 (Primes in $\mathbb{Z}[\sqrt{-3}]$):
Recall that in $\mathbb{Z}[i]$, a prime $\pi|\alpha\beta$ implies that $\pi|\alpha$ or $\pi|\beta$. In $\mathbb{Z}[\sqrt{-3}]$, define a "prime" $\pi$ to be an element that cannot be written as $\pi = \alpha\beta$ with $\alpha$ & $\beta$ nonunits.

1. Define $norm(a+b\sqrt{-3}) = a^2+3b^2$. Prove that 
   $norm(\pi_1\pi_2) = norm(\pi_1)norm(\pi_2)$.

Let $\pi_1 = a_1 + b_1\sqrt{-3}$, $\pi_2 = a_2 + b_2\sqrt{-3}$.

$\pi_1\pi_2 = (a_1a_2-3b_1b_2) + (a_1b_2+a_2b_1)\sqrt{-3}$

$norm(\pi_1\pi_2) = (a_1a_2-3b_1b_2)^2 + 3(a_1b_2+a_2b_1)^2$

$= (a_1a_2)^2 - 6a_1a_2b_1b_2 + 9(b_1b_2)^2$
$+ 3(a_1b_2)^2 + 3(a_2b_1)^2 + 6a_1a_2b_1b_2$

$norm(\pi_1)norm(\pi_2) = (a_1^2+3b_1^2)(a_2^2+3b_2^2)$

$= (a_1a_2)^2 + 3(a_1b_2)^2 + 3(a_2b_1)^2 + 9(b_1b_2)^2$

Therefore, $norm(\pi_1\pi_2) = norm(\pi_1)norm(\pi_2)$.

2. Prove that $\pi \in \mathbb{Z}[\sqrt{-3}]$ is a unit if and only if $norm(\pi) = 1$.

If $\pi$ is a unit, there exists $\pi'$, $\pi\pi' = 1$. Taking norms on both sides,

$norm(\pi\pi') = norm(1) = 1$.

By 1., $norm(\pi)norm(\pi') = 1$. Since $norm(\pi) \geq 0$ and is an integer (similarly for $norm(\pi')$), then $norm(\pi) = 1$.

Now, assume $\pi = a+b\sqrt{-3}$ and $norm(\pi) = 1$. Then,
$(a^2+3b^2) = 1 \Rightarrow (a+b\sqrt{-3})(a-b\sqrt{-3}) = 1$. Since
$a-b\sqrt{-3} \in \mathbb{Z}[\sqrt{-3}]$, $\pi$ is a unit by definition.

3. Prove that if $norm(\pi)$ is a prime in $\mathbb{N}$, then $\pi$ is "prime" in $\mathbb{Z}[\sqrt{-3}]$.

Let $\pi \in \mathbb{Z}[\sqrt{-3}]$ such that $norm(\pi)$ is prime in $\mathbb{N}$.
Assume $\pi$ is not a "prime" in $\mathbb{Z}[\sqrt{-3}]$.

Then, $\pi = \alpha\beta$, with $\alpha$ & $\beta$ nonunits.

Since $\alpha$ & $\beta$ are nonunits, by part 2.,
$norm(\alpha) > 1$, $norm(\beta) > 1$. Then,

$norm(\pi) = norm(\alpha)norm(\beta)$, $norm(\alpha) > 1$, $norm(\beta) > 1$.

This is impossible since $norm(\pi)$ is prime in $\mathbb{N}$.
By contradiction, $\pi$ is "prime" in $\mathbb{Z}[\sqrt{-3}]$.

4. Prove that 2 is "prime" in $\mathbb{Z}[\sqrt{-3}]$.

Suppose not. Then, $2 = \alpha\beta$ with $norm(\alpha) > 1$, $norm(\beta) > 1$.

Therefore, taking norms, $4 = norm(\alpha)norm(\beta)$ with
$norm(\alpha) > 1$, $norm(\beta) > 1$.

Therefore, $norm(\alpha) = norm(\beta) = 2$.

Let $\alpha = a+b\sqrt{-3}$, $a^2+3b^2 = 2$.

Taking both sides (mod 4), $a^2+3b^2 \equiv 2$ (mod 4).
But $a^2 \equiv 0,1$ (mod 4), $3b^2 \equiv 0,3$ (mod 4), and therefore,
this is impossible. By contradiction, 2 is "prime" in $\mathbb{Z}[\sqrt{-3}]$.

5. Show that $2|(1+\sqrt{-3})(1-\sqrt{-3})$.

$(1+\sqrt{-3})(1-\sqrt{-3}) = 1+3 = 4 = 2 \cdot 2$.
Therefore, $2|(1+\sqrt{-3})(1-\sqrt{-3})$.

6. Conclude that $\mathbb{Z}[\sqrt{-3}]$ does not have the property that for "primes", $\pi|\alpha\beta \Rightarrow \pi|\alpha$ or $\pi|\beta$.

Note that 2 is "prime" in $\mathbb{Z}[\sqrt{-3}]$.
$2|(1+\sqrt{-3})(1-\sqrt{-3})$ but $2 \nmid 1+\sqrt{-3}$,
$2 \nmid 1-\sqrt{-3}$.

Remark: The reason I put "prime" in quotes is because when this property doesn't hold, we stop calling $\pi$ a prime, and we call it irreducible. This is just for your own benefit if you end up learning ring theory or algebraic number theory.

## Problem 5:
1. Write the law of quadratic reciprocity

If $p$ & $q$ are distinct odd primes, then,
$$\left(\frac{p}{q}\right)\left(\frac{q}{p}\right) = (-1)^{\frac{p-1}{2}\frac{q-1}{2}}$$

2. Write the "strong multiplicativity" symbol

If $q$ is an odd prime, $P_1 \not\equiv 0$ (mod $q$), $P = P_1P_2$, then
$$\left(\frac{P}{q}\right) = \left(\frac{P_1}{q}\right)\left(\frac{P_2}{q}\right)$$

3. Write $(\frac{1}{q})$ & $(\frac{2}{q})$. (Evaluate and recall their values)

$$\left(\frac{-1}{q}\right) = \begin{cases} 
1; & q \equiv 1 \pmod{4} \\
-1; & q \equiv 3 \pmod{4}
\end{cases}$$

4. Compute $(\frac{55}{89})$, $(\frac{56}{89})$, $(\frac{23}{59})$

$$\left(\frac{55}{89}\right) = \left(\frac{5}{89}\right)\cdot\left(\frac{11}{89}\right)$$
$$= \left(\frac{89}{5}\right)\cdot\left(\frac{89}{11}\right)$$
$$= \left(\frac{4}{5}\right)\cdot\left(\frac{1}{11}\right) = \left(\frac{2}{5}\right)^2\cdot\left(\frac{1}{11}\right) = 1\cdot1 = 1$$

$$\left(\frac{56}{89}\right) = \left(\frac{2^3\cdot7}{89}\right)$$
$$= \left(\frac{2}{89}\right)^3\cdot\left(\frac{7}{89}\right)$$
$$= 1\cdot1\cdot\left(\frac{89}{7}\right) = \left(\frac{5}{7}\right) = \left(\frac{7}{5}\right) = \left(\frac{2}{5}\right) = -1$$

$$\left(\frac{23}{59}\right)$$
$$= -\left(\frac{59}{23}\right) = -\left(\frac{13}{23}\right)$$
$$= -\left(\frac{23}{13}\right) = -\left(\frac{10}{13}\right) = -\left(\frac{2}{13}\right)\left(\frac{5}{13}\right)$$
$$= -(-1)\left(\frac{5}{13}\right) = \left(\frac{13}{5}\right) = \left(\frac{3}{5}\right) = \left(\frac{2}{3}\right)^2 = -1$$

## Problem 6:
Using quadratic reciprocity & the Chinese remainder theorem, show that
$$\left(\frac{3}{q}\right) = \begin{cases} 
1; & q \equiv 1,11 \pmod{12} \\
-1; & q \equiv 5,7 \pmod{12}
\end{cases}$$

Using quadratic reciprocity,

$$\left(\frac{3}{q}\right) = \begin{cases} 
\left(\frac{3}{q}\right); & q \equiv 1 \pmod{4} \\
-\left(\frac{3}{q}\right); & q \equiv 3 \pmod{4}
\end{cases}$$

Now, notice that the squares (mod 3) are 0,1, and 2 is a nonsquare (mod 3).

Therefore, $$\left(\frac{q}{3}\right) = \begin{cases}
1; & q \equiv 1 \pmod{3} \\
-1; & q \equiv 2 \pmod{3}
\end{cases}$$

Putting these together, we have

$$\left(\frac{3}{q}\right) = \begin{cases}
\left(\frac{q}{3}\right); & q \equiv 1 \pmod{4} \\
-\left(\frac{q}{3}\right); & q \equiv 3 \pmod{4}
\end{cases}$$

$$= \begin{cases} 1; & q \equiv 1 \pmod{4} \text{ and } q \equiv 1 \pmod{3} \ -1; & q \equiv 1 \pmod{4} \text{ and } q \equiv 2 \pmod{3} \ -1; & q \equiv 3 \pmod{4} \text{ and } q \equiv 1 \pmod{3} \ 1; & q \equiv 3 \pmod{4} \text{ and } q \equiv 2 \pmod{3} \end{cases}$$

Now, notice that odd primes (mod 12) are
1, 5, 7, 11.

$$1 \bmod 12 \leftrightarrow (1 \bmod 3, 1 \bmod 4)$$
$$5 \bmod 12 \leftrightarrow (2 \bmod 3, 1 \bmod 4)$$
$$7 \bmod 12 \leftrightarrow (1 \bmod 3, 3 \bmod 4)$$
$$11 \bmod 12 \leftrightarrow (2 \bmod 3, 3 \bmod 4)$$
 
By the Chinese Remainder Theorem

Therefore,
$$\left(\frac{3}{q}\right) = \begin{cases}
1; & q \equiv 1,11 \pmod{12} \\
-1; & q \equiv 5,7 \pmod{12}
\end{cases}$$

[Continue with Problem 7?]
## Problem 7: Alternative Proof to $(p-1)! \equiv -1 \pmod{p}$

Let $p$ be an odd prime, $g$ is a primitive root of $p$.

1. Show that $(p-1)! \equiv g^{\frac{p(p-1)}{2}} \pmod{p}$
2. Show that $g^p \equiv g \pmod{p}$
3. Show that $g^{\frac{p-1}{2}} \equiv -1 \pmod{p}$
4. Conclude that $(p-1)! \equiv -1 \pmod{p}$