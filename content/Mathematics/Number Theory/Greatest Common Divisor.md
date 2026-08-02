---
publish: true
created: 2026-07-27T00:45:21.551+10:00
modified: 2026-08-02T19:25:18.591+10:00
---

## Greatest Common Divisor

The **greatest common divisor (GCD)** is the largest positive integer that divides two or more integers _without leaving a remainder_. It is also known as the **greatest common factor (GCF)**.

Consider integers $20$ and $36$ and their divisors:
$20: -20, -10, -5, -4, -2, -1, 1, 2, 4, 5, 10, 20$.
$36: -36, -18, -12, -9, -6, -4, -3, -2, -1, 1, 2, 3, 4, 6, 9, 12, 18, 36$.

The **common divisors** are those shared by both integers: $-4, -2, -1, 1, 2, 4$.
The $\gcd(36, 20)$ is the largest (most positive) shared divisor: $4$.

The divisors, common divisors, and GCD of $20$ and $36$, $-20$ and $36$, $20$ and $-36$, and $-20$ and $-36$ are all identical.

The GCD can be found using [[Mathematics/Number Theory/Prime Decomposition]] or the [[Mathematics/Number Theory/Euclidean Algorithm]].

---

## Using Prime Decomposition

Consider the integers $112$ and $60$.

Express each number as a product of primes:
$120 = 2^3 \times 3 \times 5$
$36 = 2^2 \times 3^2$

Take the prime powers that both numbers share:
$gcd(120, 36) = 2^2 \times 3 = 12$
