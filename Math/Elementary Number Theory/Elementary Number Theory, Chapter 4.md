
## Mastery

| Section | Exercises Completed |
| ------- | ------------------- |
| 1       | N/A                 |
| 2       | 1-4                 |
| 3       | None                |
| 4       | None                |

## Definition 4.1

$$(\forall (a,b)\in \mathbb{Z}^2)(a\equiv b \mod n)\iff n\;|a-b)$$

### Example 4.1 

Show that $-56\equiv -11\mod 9$ .

#### Solution.

$-56\equiv -11\mod 9$
$\iff 9\;|\;-56+11$
$\iff 9\;|\;-45$
$\iff9\;|\;9(-5)$

## Theorem 4.2

$\forall (a,b,c,d,n)\in \mathbb{Z}^4\times(\mathbb{N}\setminus \{1\})$, all of the following properties hold:

**(1)** $a\equiv a\mod n$
**(2)** $a\equiv b\mod n\implies b\equiv a\mod n$
**(3)** $a\equiv b\mod n\wedge b\equiv c\mod n\implies a\equiv c\mod n$
**(4)** $a\equiv b\mod n\wedge c\equiv d\mod n\implies a+c \equiv b+d\mod n\wedge ac\equiv bd\mod n$
**(5)** $a\equiv b(mod\;n)\implies a+c\equiv b+c(mod\;n)\wedge ac\equiv bc(mod\;n)$
**(6)** $a\equiv b(mod\;n)\implies (\forall k\in\mathbb{Z})(a^k\equiv b^k(mod\;n))$

### Example 4.2

Show that $41$ divides $2^{20} -1$.

#### Solution.

$2^5=32\equiv -9\mod 41$
$\implies 2^{5(4)}\equiv(-9)^4\mod 41$
$\iff 2^{5(4)}\equiv81(81)\mod41\wedge (81=82-1=2(41)-1\equiv -1\mod 41\implies 81^2\equiv 1\mod 41)$
$\implies 2^{20}=2^{5(4)}\equiv 81^2\mod 41\equiv 1 \mod 41$
$\iff 41\;|\;2^{20}-1$

### Example 4.3

Find $x$, where:
$$1! + 2! + \dots99!+100!\equiv x\mod 12$$
#### Solution.

$4!=12=0\mod 12$
$\implies (\forall k\in \mathbb{N}_{>4})(k!\equiv 0\mod 12)$
$\implies 4! + 5! + \dots 99! + 100! \equiv 0 \mod 12$
$\begin{align*}\implies 1! + 2! + \dots 99! + 100! & = 1! + 2! + 3! + (4! + 5! + \dots + 99! + 100!)\\ & \equiv 1! + 2! + 3! + 0 \mod 12 \\ & \equiv 9\mod 12\end{align*}$

#### Matching Problems.

##### 4.2.3

$a\equiv b\mod n$
$\iff n\;|\;a-b$
$\iff (\exists k\in\mathbb{Z})(a=kn+b)$
$\begin{align*}\implies \gcd(a,n)& =min_{(x,y)\in\mathbb{Z}^2}(ax+ny)\\&=min_{(x,y)\in\mathbb{Z}^2}((b+kn)x+ny)\\&=min_{(x,y)\in\mathbb{Z}^2}(bx+n(kx+y))\\&=min_{(x,y)\in\mathbb{Z}^2}(bx+ny)\end{align*}$
$\wedge\; \gcd(b,n)=min_{(z,t)\in\mathbb{Z}^2}(bx+ny)$
$\iff \gcd(a,n)=\gcd(b,n)$

##### 4.2.4(a)

$\begin{align*}2^3\equiv 1\mod 7 &\iff 2^{3\cdot 16}=2^{48}\equiv 1\mod 7\\&\iff4\cdot 2^{48}=2^{50}\equiv 4\mod 7\end{align*}$

$\begin{align*}41\equiv -1\mod 7 &\iff 41^{65}\equiv (-1)^{65}\mod 7\equiv -1\mod 7\end{align*}$

##### 4.2.4(b)

We would like to show that $1^5 + 2^5+\dots +99^5+100^5\equiv 0\mod 4$. Since $4\;|\;100$, it is sufficient to show that $(\forall n\in\mathbb{N})(n^5+(n+1)^5+(n+2)^5+(n+3)^5\equiv 0 \mod 4)$, whence the sum $a_1+a_2+\dots+a_{24}+a_{25}\equiv 0 + 0 +\dots + 0 + 0\equiv 0\mod 4$, where $a_k=k^5+(k+1)^5+(k+2)^5+(k+3)^5$.

First:

$a:= 4n^5+140n^3+360n^2+276=4(n^5+35n^3+90n^2+69)\equiv 0\mod 4$

Then, using the division algorithm:

$\begin{align*}b&:= n(30n^3+490)\\&\iff b=4(5)(2n+1)(12n^3+18n^2+9n+26)\;\vee\;b=4(5n)(24n^3+49)\\&\implies b\equiv 0\mod 4\end{align*}$

So:

$\begin{align*}a+b&=4n^5+30n^4+140n^3+360n^2+490n+276\\&=n^5+(n+1)^5+(n+2)^5+(n+3)^5\\&\equiv 0\mod 4\end{align*}$

##### 4.2.5 



## Theorem 4.3

$ca\equiv cb\mod n\;\wedge\;gcd(c,n)=d\implies a\equiv b\mod \frac{n}{d}$

### Corollary 1

$ca\equiv cb\mod n\;\wedge\;gcd(c,n)=1\implies a\equiv b\mod n$

### Corollary 2

Let $p$ be a prime number.

$ca\equiv cb\mod p\;\wedge\;p\nmid c\implies a\equiv b\mod p$

### Example 4.4

$$\begin{align*}33\equiv 15 \mod 9 & \iff 3(11)\equiv 3(5) \mod 9\;\wedge\;\gcd(3,9)=3\\ & \implies 11\equiv 5\mod \frac{9}{3}\equiv 5\mod 3\end{align*}$$

#### Matching problems


