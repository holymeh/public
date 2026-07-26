---
publish: true
created: 2026-07-27T00:45:21.540+10:00
modified: 2026-07-27T00:52:36.038+10:00
---

## Primes

A number $p$ is prime if $p \in Z$ and $p \ge 2$ and the only positive integers which divide $p$ are $1$ and $p$.

---

## Prime Factor Theorem

Any integer greater than or equal to $2$ will have a **prime factor**.

Let $x \in Z, x \ge 2$.
$\exists$ a prime $p$ such that $p|x$ ($x=mp, m \in Z$)

Base case — consider $x=2$:
$2=1 \times 2$, where $2=p$.

Assume the theorem is correct for $2 \le x \le k$.

**Examine $k+1$:**

Either $k+1$ is prime $\rightarrow k+1=1 \times (k+1)$, thus $k+1$ has itself as a prime factor.
$OR$
$k+1$ is not a prime $\rightarrow k+1=ab$ where $1 < a,b < k+1$

As $2 \le a \le k$, $a=mp$ $\rightarrow k+1=mpb = (mb)p$ where $mb$ is an integer.
Hence $k+1$ has a prime factor $p$.

---

## Euclid's Theorem (Infinitude of Primes)

Euclid's theorem asserts that there are infinitely many prime numbers.

**Assume for contradiction** that there are only finitely many primes.\
$p_1​,p_2​,p_3​,\ldots,p_n​$.

**Form a new number** by multiplying them all and adding 1:
$N = p_1 \cdot p_2 \cdot p_3​\ldots \cdot p_n​ + 1$.

If $N$ **is prime**, then it is a prime not in the list $\rightarrow$ contradiction: we assumed the list had _all_ primes

If $N$ **is composite**, then it has some prime factor $q$ (as any integer greater than or equal to $2$ will have a prime factor). That prime factor $q$ must be one of the $p_i$, because those are all the primes.

Thus $q$ divides the product $p_1 \cdot p_2 \cdot p_3​\ldots \cdot p_n$ and also divides $N = p_1 \cdot p_2 \cdot p_3​\ldots \cdot p_n​ + 1$.

A number cannot divide two integers that differ by 1, so $q$ cannot divide both the product and $N$. Thus by contradiction there must be infinitely many primes.
