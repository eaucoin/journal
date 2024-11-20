We want to show that the equation $2 = a^2 - 2b^2$ has no integer solutions for $a$ and $b$.

Suppose there exist integers $a$ and $b$ such that $2 = a^2 - 2b^2$.  
Consider the equation modulo 2:  
$2 \equiv a^2 - 2b^2 \pmod{2}$  
$0 \equiv a^2 \pmod{2}$  
This means that $a^2$ is divisible by 2. Since 2 is a prime number, this implies that $a$ is divisible by 2, so we can write $a = 2k$ for some integer $k$.  
Substituting $a = 2k$ into the original equation, we get:  
$2 = (2k)^2 - 2b^2$  
$2 = 4k^2 - 2b^2$  
Dividing both sides by 2:  
$1 = 2k^2 - b^2$  
$b^2 = 2k^2 - 1$  
Now, consider the equation modulo 4.  
$b^2 \equiv 2k^2 - 1 \pmod{4}$  
If $k$ is even, let $k = 2m$ for some integer $m$. Then $k^2 = 4m^2 \equiv 0 \pmod{4}$.  
In this case, $b^2 \equiv 2(0) - 1 \equiv -1 \equiv 3 \pmod{4}$.  
If $k$ is odd, let $k = 2m+1$ for some integer $m$. Then $k^2 = (2m+1)^2 = 4m^2 + 4m + 1 \equiv 1 \pmod{4}$.  
In this case, $b^2 \equiv 2(1) - 1 \equiv 1 \pmod{4}$.

So, $b^2$ is either congruent to 1 or 3 modulo 4.  
However, the quadratic residues modulo 4 are 0 and 1. That is, for any integer $n$, $n^2 \equiv 0$ or $1 \pmod{4}$.  
Since we have $b^2 \equiv 3 \pmod{4}$ when $k$ is even, and $b^2 \equiv 1 \pmod{4}$ when $k$ is odd, we must have that $b^2 \equiv 1 \pmod{4}$, so $k$ must be odd.

However, if we consider the equation $b^2 = 2k^2 - 1$ modulo 8,  
if $k$ is odd, let $k = 2n+1$ for some integer $n$. Then $k^2 = 4n^2 + 4n + 1 \equiv 1 \pmod{8}$ if $n$ is even, and $k^2 \equiv 4n^2+4n+1 \equiv 5 \pmod{8}$ if $n$ is odd.  
If $k^2 \equiv 1 \pmod{8}$, $b^2 = 2k^2 - 1 \equiv 2(1) - 1 \equiv 1 \pmod{8}$.  
If $k^2 \equiv 5 \pmod{8}$, $b^2 = 2k^2 - 1 \equiv 2(5) - 1 \equiv 9 \equiv 1 \pmod{8}$.  
So, $b^2 \equiv 1 \pmod{8}$.  
This doesn't lead to a contradiction.

Final Answer: The final answer is $\boxed{2}$