---
publish: true
created: 2026-07-27T00:45:21.548+10:00
modified: 2026-07-27T15:06:58.523+10:00
---

## Greatest Common Divisor

The **greatest common divisor (GCD)** is the largest positive integer that divides two or more integers _without leaving a remainder_. It is also known as the **greatest common factor (GCF)**.

Consider integers $20$ and $36$ and their divisors:
$20: -20, -10, -5, -4, -2, -1, 1, 2, 4, 5, 10, 20$.
$36: -36, -18, -12, -9, -6, -4, -3, -2, -1, 1, 2, 3, 4, 6, 9, 12, 18, 36$.

The **common divisors** are those shared by both integers: $-4, -2, -1, 1, 2, 4$.
The $\gcd(36, 20)$ is the largest (most positive) shared divisor: $4$.

The divisors, common divisors, and GCD of $20$ and $36$, $-20$ and $36$, $20$ and $-36$, and $-20$ and $-36$ are all identical.

---

## The Euclidian Algorithm

The Euclidian algorithm is an efficient method for computing the **greatest common divisor (GCD)** of two integers. It is based on the principle that the GCD of two numbers does not change if the larger number is replaced by its difference with the smaller number.

To use the Euclidean Algorithm to more efficiently find the GCD, take the integer with the **greater modulus** and write it as a Euclidean division, that is, in the form:$a=bq+r, \quad a, b, q, r \in Z, \quad b\ne 0$where $a$ is a **dividend**, $b$ is its **divisor**, $q$ is the **quotient** and $r$ is the **remainder**. Additionally, $0 \le r < \left|b\right|$.

The GCD of two integers $a$ and $b$ is equal to the GCD of $b$ and the remainder $r$ when $a$ is divided by $b$. Thus repeated divisions provide increasingly smaller pairs of integers that share $\gcd(a, b)$. These divisions will eventually terminate in a division with no remainder, enabling easy identification of the GCD.

**For example**, let $a = 36$ and $b = 20$:

$36 = 1 \times 20 + 16$
$\gcd(36, 20) = \gcd(20,16)$
$20 = 1 \times 16 + 4$
$\gcd(20, 16) = \gcd(16,4)$
$16 = 4 \times 4$
$\gcd(16,4) = 4$

Thus $\gcd(36, 20) = 4$

---

## Proof

For $m, n \in Z$:

If $\left| m \right| = \left| n \right|$
then $\gcd(m, n) =$ the larger of $m, n$

If $\left| m \right| > \left| n \right|$
$m = qn + r, \quad r = 0$
then $\gcd(m, n) =$ $\left| n \right|$

If $\left| m \right| > \left| n \right|$
$m = qn + r \quad 0 < r < \left| m \right|$

$\gcd(m, n) = \gcd(n, r)$
This is true because $d|m \ d|n \leftrightarrow d|n \ d|r$.

$d|m \rightarrow d|r$ because:
$m = qn + r$
$r = m - qn$
$m = z_{1}d \quad n = z_{2}d$ (because $d$ divides $m$ and $n$)
$r = z_{1}d + (-q)z_{2}d = (z_{1} -qz_{2})d$
$(z_{1} -qz_{2}) \in Z \implies d|r$

$d|r \rightarrow d|m$ because:
$m = qn + r$
$n = z_{2}d \quad r = z_{3}d$ (because $d$ divides $n$ and $r$)
$m = qz_{2}d + z_{3}d = (qz_{2} + z_{3})d$
$(qz_{2} + z_{3}) \in Z \implies d|m$

Thus the list of all the common divisors of $m$ and $n$ will be the same as the list of all the common divisors of $n$ and $r$.

$\gcd(m,n) \le \gcd(n,r)$, because $\gcd(n,r)$ is the **greatest** common divisor of $n$ and $r$.
$\gcd(n,r) \le \gcd(m,n)$, because $\gcd(m,n)$ is the **greatest** common divisor of $m$ and $n$.

Thus $\gcd(m,n) = \gcd(n,r)$

---

## Examples

1. Find the greatest common divisor of $270$ and $192$.

$$
\begin{array} \
\gcd(270, 192) \\
270 = 1 \times 192 + 78 \\
192 = 2 \times 78 + 36 \\
78 = 2 \times 36 + 6 \\
36 = 6 \times 6 \\
\gcd(270, 192) = \gcd(6, 0) = 6
\end{array}
$$

2. Find the greatest common divisor of $-120$ and $-36$.

$$
\begin{array} \
\gcd(-120, -36) \\
-120 = 4 \times -36 + 24 \\
-36 = -2 \times 24 + 12 \\
24 = 2 \times 12 \\
\gcd(-120, -36) = \gcd(12, 0) = 12
\end{array}
$$

_Note: it would be easier to find $\gcd(120, 36)$ as this will equal $\gcd(-120, -36)$._
