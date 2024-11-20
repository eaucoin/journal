You're on the right track! Using properties of the ring $\mathbb{Z}[\sqrt{2}]$ is the most elegant way to solve this.

**Proof using $\mathbb{Z}[\sqrt{2}]$**

1. **The Ring $\mathbb{Z}[\sqrt{2}]$:** This ring consists of numbers of the form $x + y\sqrt{2}$, where $x$ and $y$ are integers.
    
2. **The Norm:** We define the norm function $N: \mathbb{Z}[\sqrt{2}] \to \mathbb{Z}$ as $N(x + y\sqrt{2}) = (x + y\sqrt{2})(x - y\sqrt{2}) = x^2 - 2y^2$. The crucial property of the norm is that it's multiplicative: $N(\alpha \beta) = N(\alpha)N(\beta)$ for any $\alpha, \beta \in \mathbb{Z}[\sqrt{2}]$.
    
3. **The Equation in $\mathbb{Z}[\sqrt{2}]$:** Our equation $a^2 - 2b^2 = 2$ can be rewritten as $N(a + b\sqrt{2}) = 2$.
    
4. **Units in $\mathbb{Z}[\sqrt{2}]$:** The units in $\mathbb{Z}[\sqrt{2}]$ are elements with norm $\pm 1$. It's known that all units are of the form $\pm(1 + \sqrt{2})^n$ for some integer $n$. (This can be proven using continued fractions or other methods.)
    
5. **Proof by Contradiction:** Suppose there is a solution $a + b\sqrt{2}$ with norm 2. Then, if we could find an element with norm 2, we could multiply it by a unit to get infinitely many solutions with norm 2.
    
    - Consider the smallest positive integer solution for a. Let's call this solution $a_0 + b_0\sqrt{2}$.
        
    - Now consider the element $(a_0 + b_0\sqrt{2})(1 - \sqrt{2}) = (a_0 - 2b_0) + (b_0 - a_0)\sqrt{2}$.
        
    - Calculate its norm: $N((a_0 - 2b_0) + (b_0 - a_0)\sqrt{2}) = (a_0 - 2b_0)^2 - 2(b_0 - a_0)^2 = a_0^2 - 4a_0b_0 + 4b_0^2 - 2b_0^2 + 4a_0b_0 - 2a_0^2 = -a_0^2 + 2b_0^2$.
        
    - Since $a_0^2 - 2b_0^2 = 2$, we have $-a_0^2 + 2b_0^2 = -2$, or $(a_0 - 2b_0)^2 - 2(a_0-b_0)^2 = -2$.
        

If $a_0$ and $b_0$ are positive, and $a_0^2 - 2b_0^2 = 2$, then $a_0 > \sqrt{2}b_0$. Let $a_1 = |a_0 - 2b_0|$ and $b_1 = |b_0-a_0|$. Then we have $a_1^2 - 2b_1^2 = 2$, and we also have $a_1 = |a_0 - 2b_0| < a_0$. This contradicts the minimality of $a_0$, proving that no solution exists.

Therefore, there are no integer solutions to $a^2 - 2b^2 = 2$.