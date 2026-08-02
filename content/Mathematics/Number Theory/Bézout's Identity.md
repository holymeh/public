---
publish: true
created: 2026-07-27T00:45:21.538+10:00
modified: 2026-08-02T20:44:48.057+10:00
---

Bézout's Identity states that for any integers $m, n \in Z, \exists \ z_{1}, z_{2} \in Z$ such that $z_{1}m + z_{2}n = \gcd(m, n)$.

The numbers $z_{1}, z_{2}$ are called **Bézout coefficients**. They are not unique - there are instead infinitely many pairs.

Bézout's Identity says:

- The **greatest common divisor** of $m$ and $n$ can always be written as a combination of  $m$ and $n$, using integer multipliers.
- This also implies that $\gcd(m, n)$ is the **smallest positive integer** that can be expressed as a linear combination of $m$ and $n$.

---

## Finding Bézout Coefficients

Use the Euclidean algorithm to find $\gcd(36, 20)$:

$$
\begin{array}{c}  \
36 = 1 \times 20 + 16 \\
20 = 1 \times 16 + 4 \\
16 = 4 \times 4 \\\\

\gcd(36, 20) = \gcd(20,16) = \gcd(16,4) = 4
\\\\
16 = 36 + (-1)20
\\\\
4 = 1 \times 20 -1 \times 16
\\ = 1 \times 20 -1 \times (36 -1 \times 20)
\\= -1 \times 36 + 2 \times 20
\\\\
z_{1} = -1, z_{2} = 2
\end{array}
$$

---

## Examples

1. Find the Bézout coefficients for $24$ and $56$.

$56 = 2 \times 24 + 8$

$24 = 3 \times 8$

$\gcd(56, 24) = \gcd(28, 8) = 8$

$8 = 1 \times 56 - 2 \times 24$

$z_{1} = 1, z_{2} = -2$

2. Find the Bézout coefficients for $75$ and $44$.

$75 = 1 \times 44 + 31$

$44 = 1 \times 31 + 13$

$31 = 2 \times 13 + 5$

$13 = 2 \times 5 + 3$

$5 = 1 \times 3 + 2$

$3 = 1 \times 2 + 1$

$2 = 2 \times 1$

$\gcd(75, 44) = \gcd(44, 31) = \gcd(31, 13) = \gcd(13, 5) = \gcd(5, 3) = \gcd(3, 2) = \gcd(2, 1) = 1$

$31 = 1 \times 75 - 1 \times 44$

$13 = 1 \times 44 - 1 \times 31$

$= 1 \times 44 - 1 \times (1 \times 75 - 1 \times 44)$

$= 2 \times 44 - 1 \times 75$

$5 = 1 \times 31 - 2 \times 13$

$= 1 \times (1 \times 75 - 1 \times 44) - 2 \times (2 \times 44 - 1 \times 75)$

\= $3 \times 75 - 5 \times 44$

$3 = 1 \times 13 - 2 \times 5$

$= 1 \times (2 \times 44 - 1 \times 75) - 2 \times (3 \times 75 - 5 \times 44)$

$= -7 \times 75 + 12 \times 44$

$2 = 1 \times 5 - 1 \times 3$

$= 1 \times (3 \times 75 - 5 \times 44) - 1 \times (-7 \times 75 + 12 \times 44)$

$= 10 \times 75 - 17 \times 44$

$1 = 1 \times 3 - 1 \times 2$

$= 1 \times (-7 \times 75 + 12 \times 44) - 1 \times (10 \times 75 - 17 \times 44)$

$= -17 \times 75 + 29 \times 44$

$z_{1} = -17, z_{2} = 29$
