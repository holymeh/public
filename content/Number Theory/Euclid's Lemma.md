---
publish: true
created: 2026-07-27T00:45:21.539+10:00
modified: 2026-07-27T00:52:28.442+10:00
---

Euclid's lemma states that if a prime number $p$ divides a product $ab$, then $p$ must divide $a$ or $p$ must divide $b$ (or both).

$p \mid ab \quad a,b \in Z$  $\ \rightarrow \quad p \mid a \; \lor \; p \mid b$

---

## Proof

Assume $p \mid ab$

Either $p \mid ab$ or $p \nmid ab$.

If $p \mid ab \rightarrow p \mid a \; \lor \; p \mid b$

If $p \nmid ab$ then $gcd(p, a) = 1$.
This is because the complete list of divisors of $p$, a prime number, is $-p, -1, 1, p$ and since $p \nmid ab$ the only common divisors of $p$ and $a$ are $-1$ and $1$.

Applying [[Number Theory/Bézout's Identity]]:
$\exists \ z_{1}, z_{2} \in Z$ such that $z_{1}p + z_{2}a = 1$

As $p \mid ab$, $ab = mp \quad m \in Z$
Multiply the Bézout equation by $b$:
$z_{1}pb + z_{2}ab = b$
$z_{1}bp + z_{2}mp = b$
$b = (z_{1}b + z_{2}m)p$ where $(z_{1}b + z_{2}m) \in Z$
Hence $p \mid b$ and hence $p \mid a \; \lor \; p \mid b$
