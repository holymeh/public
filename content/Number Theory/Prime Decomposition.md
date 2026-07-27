---
publish: true
created: 2026-07-27T00:45:21.553+10:00
modified: 2026-07-27T14:44:42.176+10:00
---

Expressing a composite number as a **product of powers of prime numbers** is called **prime decomposition**. For example:

$$
\begin{aligned}
3000 = 3 \times 2^{3} \times 5^{3} \\
2294 = 2 \times 31 \times 37
\end{aligned}
$$

---

## Finding Factors by Prime Decomposition

The prime decomposition of 17248 is

$$
17\,248 = 2^{5} \times 7^{2} \times 11
$$

Therefore each factor must be of the form

$$
2^{\alpha} \times 7^{\beta} \times 11^{\gamma}, \quad \alpha = 0,1,2,3,4,5, \quad \beta = 0,1,2, \quad \gamma = 0,1
$$

The factors of 17248 can be systematically listed as follows:

$$
\begin{array}{cccccc}
1 & 2 & 2^{2} & 2^{3} & 2^{4} & 2^{5} \\
7 & 2 \times 7 & 2^{2} \times 7 & 2^{3} \times 7 & 2^{4} \times 7 & 2^{5} \times 7 \\
7^{2} & 2 \times 7^{2} & 2^{2} \times 7^{2} & 2^{3} \times 7^{2} & 2^{4} \times 7^{2} & 2^{5} \times 7^{2} \\
11 & 2 \times 11 & 2^{2} \times 11 & 2^{3} \times 11 & 2^{4} \times 11 & 2^{5} \times 11 \\
7 \times 11 & 2 \times 7 \times 11 & 2^{2} \times 7 \times 11 & 2^{3} \times 7 \times 11 & 2^{4} \times 7 \times 11 & 2^{5} \times 7 \times 11 \\
7^{2} \times 11 & 2 \times 7^{2} \times 11 & 2^{2} \times 7^{2} \times 11 & 2^{3} \times 7^{2} \times 11 & 2^{4} \times 7^{2} \times 11 & 2^{5} \times 7^{2} \times 11
\end{array}
$$

---

## Divisor-Count Rule

The divisor-count rule, also known as the _tau function formula_, determines **how many factors** a number has from its prime factorisation.

If a natural number has prime factorisation
$n = p_1^{a_1} p_2^{a_2} p_3^{a_3} \cdots p_k^{a_k}$
then the number of positive divisors of $n$ is:
$(a_1+1)(a_2+1)(a_3+1) \cdots (a_k+1)$

**Explanation:**
Each divisor of $n$ must be of the form:
$p_1^{e_1} p_2^{e_2} \cdots p_k^{e_k}, \quad 0 \le e_i \le a_i, \quad (i=1,\dots,k)$

For each prime $p_i$​, there are $a_i + 1$ choices for $e_i$​: $
0, 1, 2, \cdots, a_i$So the total number of divisors is the product:
$(a_1+1)(a_2+1)\cdots (a_k+1)$

---

## Product of all positive divisors

If a number $n$ has $d$ positive divisors, then the product of all its divisors is $n^{d/2}$.
This is because divisors come in _pairs_ that multiply to $n$.

**Example**:

$$\begin{array} \
1 \cdot 30 = 30 \\
2 \cdot 15 = 30 \\
3 \cdot 10 = 30 \\
5 \cdot 6 = 30
\end{array}
$$

This always happens: if $k$ is a divisor, then $n/k$ is also a divisor.\
Each pair multiplies to $n$ and there are $n/d$ pairs.

---

## Examples

1. Determine the number of factors that $720$ has.

$$
720 = 2^{4} \times 3^{2} \times 5
$$

Therefore each factor must be of the form

$$2^{\alpha} \times 3^{\beta} \times 5^{\gamma}, \quad \alpha = 0,1,2,3,4 \quad \beta = 0,1,2 \quad \gamma = 0,1
$$

There are $5$ possible values for ${\alpha}$, $3$ possible values for ${\beta}$, and $2$ possible values for ${\gamma}$.
$(4+1)(2+1)(1+1) = 5\cdot3\cdot2 = 30$
Hence there are $30$ possible factors of $720$.

2. The natural number $n$ has exactly eight different factors. Two of these factors are $15$ and $21$. What is the value of $n$?

The number must be a multiple of $15$ and $21$.

$$$\begin{array}  \ 15 = 3 \times 5 \ 21 = 3 \times 7 \
LCM(15, 21) = 3 \times 5 \times 7 = 105 \end{array}$$
Thus $n$ must be a multiple of $105$.
$$\begin{array} \ n=3^{\alpha} \times 5^{\beta} \times 7^{\gamma}, \ \alpha, \beta, \gamma \ge 1 \\
(\alpha+1)(\beta+1)(\gamma+1)=8 \\
\alpha = 1, \ \beta = 1, \ \gamma = 1
\end{array}$$
---
## See Also

[[Number Theory/Lowest Common Multiple]]
[[Number Theory/Greatest Common Divisor]]
[[Number Theory/Fundamental Theorem of Arithmetic]]
$$$
