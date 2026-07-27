---
publish: true
created: 2026-07-27T00:45:21.550+10:00
modified: 2026-07-27T00:53:00.393+10:00
---

Every integer greater than 1 can be written as a product of prime numbers, and this factorisation is unique (except for the order of the factors).

This is one of the most fundamental facts in number theory. It gives the integers structure, like atoms making molecules - each integer is a unique product of primes. It's used in finding the [[Number Theory/Greatest Common Divisor|HCF]] and [[Number Theory/Lowest Common Multiple|LCM]], solving Diophantine equations, proving properties about divisibility, and cryptography.

---

## Implications of the Fundamental Theorem of Arithmetic:

1. **Every number has a prime factorisation**

Any whole number bigger than 1 can be [[Number Theory/Prime Decomposition|broken down into primes]]. Examples:

- $20=2 \times 2 \times 5$
- $91 = 7 \times 13$
- $144 = 2 \times 2 \times 2 \times 2 \times 3 \times 3$

2. **Each number's prime factorisation is unique**

If you factor a number properly into primes, there is **only one correct way**, excepting order. Example:

- $60 = 2 \times 2 \times 3 \times 5$

You could reorder: $3 \times 5 \times 2 \times 2$ - but it's still the **same primes**. You will never find a different set of primes that multiply to 60 .

---

## Existence Proof

For all $n \geq 2$, we can write $n = p_{1} \cdot p_{2} \ldots \cdot p_{k}$ where $p_{i}= prime$.

Proof by way of contradiction: suppose that there is a natural number without such a representation (as a product of primes). Let $m$ be the **smallest** such number.

Observe that $m$ must be _composite_, as if $m$ were prime then $n=m$, which is already in the form of a product of primes.

Hence $m=ab$, where $2\leq a, b<m$.

Since $a, b<m$, and $m$ is the **smallest** such number that is not representable as a product of primes, both $a$ and $b$ can be represented as a product of primes. Thus $ab$ can also be represented as a product of primes, and thus so can $m$.

---

## Uniqueness Proof

Suppose, for contradiction, that some number $n>1$ has **two different prime factorisations**: $n=p_{1} \cdot p_{2} \ldots \cdot p_{k}=q_{1} \cdot q_{2} \ldots \cdot q_{k}$
Where $p_{i}$ and $q_{j}$ are primes, and the two lists are not the same.

Divide both sides by $p_{1}$. $LHS \rightarrow p_{2} \ldots \cdot p_{k}$ which is an integer.
$R H S$ must equal $L H S$ and thus also be an integer. So $\frac{q_{1} \cdot q_{2} \ldots \cdot q_{k}}{p_{1}}$ is an integer.

**[[Number Theory/Euclid's Lemma]]**

- If a prime divides the product of two integers, it must divide **at least one of those integers**.
- So $p_{1}$ divides some $q_{j}$. But $q_{j}$ is prime $\rightarrow$ the only way $p_{1}$ divides $q_{j}$ is if $p_{1}=q_{j}$.

Cancel $p_{1}$ and $q_{j}$ from both sides.
$p_{2} \ldots \cdot p_{k}=q_{2} \ldots \cdot q_{k}$

Repeat this process for the remaining primes. If the two prime factorisations have an _equal number of primes_, then eventually, all primes on both sides must match. Hence the two prime factorisations must actually be identical.

Suppose that the two prime factorisations have a _different number of primes_, i.e. $n=p_{1} \cdot p_{2} \ldots \cdot p_{k}=q_{1} \cdot q_{2} \ldots \cdot q_{l}$ where $k<l$.

Repeatedly divide both sides by each prime until $LHS=1$ and $R H S=q_{k+1} \ldots \cdot q_{l}$.
The product of remaining primes cannot be equal to 1, hence by way of contradiction the two prime factorisations cannot have a differing number of primes.

---

## See Also

[[Number Theory/Prime Decomposition]]
[[Number Theory/Lowest Common Multiple]]
[[Number Theory/Greatest Common Divisor]]
