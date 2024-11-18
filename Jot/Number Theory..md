## Homework for the Week of November 11th.

### Problem 1. The goal of this exercise is to show how Z[√2] sheds light on sum of two squares in other ways than what we've done so far.

Namely, we show the following theorem of Euler: If a,b are integers with gcd(a,b)=1, then any divisor of a²+b² is of the form c²+d² with gcd(c,d)=1.

1. Give an example that shows why the condition gcd(a,b)=1 is necessary.

If $\gcd(a,b) \neq 1$, the theorem doesn't hold.  For example, let $a = 2$ and $b = 4$. Then $\gcd(a, b) = 2$.  We have $a^2 + b^2 = 20$, and $4$ is a divisor of $20$.  However, $4$ can only be expressed as $c^2 + d^2$ if $c=2, d=0$ or $c=0, d=2$.  If we require $\gcd(c, d) = 1$, then $4$ is not expressible in the required form.

2. Let e>1 be an integer divisor of a²+b². Show that e is a product of Gaussian prime divisors q+ir up to units.

We can factor $a^2 + b^2$ in $\mathbb{Z}[i]$ as $(a + bi)(a - bi)$.  Let $e$ be a divisor of $a^2 + b^2$ in $\mathbb{Z}$. Then $e$ is also a divisor of $(a + bi)(a - bi)$ in $\mathbb{Z}[i]$. By unique prime factorization in $\mathbb{Z}[i]$, $e$ can be written as a product of Gaussian primes: $e = \pi_1 \pi_2 \cdots \pi_n$.

[Would you like me to continue with the rest of the problems and solutions in this format?]