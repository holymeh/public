---
publish: true
created: 2026-07-27T00:45:21.552+10:00
modified: 2026-08-02T19:25:18.614+10:00
---

## Finding LCM using prime factorisation

To find the **LCM (Lowest Common Multiple)** of two numbers using [[Mathematics/Number Theory/Prime Decomposition]], break each number into its prime factors, then combine the _highest power of each prime factor amongst both numbers_.

🔹 **Step 1: Prime factorise each number**
Write each number as a product of its prime factors.
For example:

- $12=2^2 \times 3^1$
- $18=2^1\times3^2$

🔹 **Step 2: Compare the prime factors**
For each prime, take the highest power that appears:

- Prime 2: the highest power is $2^2$ .
- Prime 3: the highest power is $3^2$ .

🔹 **Step 3: Multiply these highest powers**
$LCM=2^2\times3^2=36$

**Explanation**
The LCM is the **smallest number** that **both numbers divide into evenly**.
Each number can only divide into a multiple that contains **at least as many of each prime factor as it has itself**.

So:

- 12 needs at least two 2’s and one 3.
- 18 needs at least one 2 and two 3’s.

A number that both divide into must therefore contain:

- enough 2’s for **both** (so take the higher count, $2^2$), and
- enough 3’s for **both** (so take the higher count, $3^2$).

Taking the **highest power of each prime** ensures the number includes all the factors required by both numbers. Taking only those ensures it’s the _smallest possible_ such number.

---

## Finding LCM using GCD

The [[Mathematics/Number Theory/Greatest Common Divisor]] can be used to find the **lowest common multiple** using the formula $\operatorname{lcm}(a,b) = \frac{|a \cdot b|}{\gcd(a,b)}$. This is often the fastest method for large numbers as the GCD can quickly be computed using the [[Mathematics/Number Theory/Euclidean Algorithm]].

This formula is a rearrangement of the fact that $ab = \operatorname{LCM}(a, b) \times \operatorname{HCF}(a, b)$. Expressing each integer as its prime decomposition $a = p_1^{a_1} p_2^{a_2} \cdots p_k^{a_k},\quad b = p_1^{b_1} p_2^{b_2} \cdots p_k^{b_k}$ allows us to take the minimum power of each prime (which may be zero) for the HCF, and the maximum power of each prime for the LCM. Hence we will have $p_i^{a_1} \times p_i^{b_1}$ for all $p$ when multiplying the HCF and the LCM.

---

## LCM of Fractions

To find the LCM of two (or more) fractions, use the formula:
$\operatorname{LCM}\left(\frac{a}{b},\frac{c}{d}\right) = \frac{\operatorname{LCM}(a,c)}{\operatorname{GCD}(b,d)}$

For a fraction $\frac{x}{y}$​ to be a multiple of both $\frac{a}{b}$ and $\frac{c}{d}$​:
$\frac{x}{y} = k_1 \frac{a}{b} = k_2 \frac{c}{d} \quad \text{for some integers } k_1, k_2$
**Numerator**: Take LCM $\rightarrow$ makes sure fraction is divisible by both numerators.
**Denominator**: Take GCD $\rightarrow$ makes fraction as small as possible while still being a multiple of both original fractions.

$\mathrm{LCM}\left(\frac{3}{4}, \frac{5}{6}\right) = \frac{\operatorname{LCM}(3,5)}{\gcd(4,6)} = \frac{15}{2}$

---

## Examples

1.

$LCM(9, 10)$
$9 = 3^2$
$10 = 2 \times 5$
$LCM = 3^2 \times 2 \times 5 = 90$

As seen above, when **all of the prime factors are unique** (no prime factors are common to both numbers), the **LCM is just the product of the numbers**.

2.

$LCM(105, 120)$
$105 = 3 \times 5 \times 7$
$120 = 2^3 \times 3 \times 5$
$LCM = 2^3 \times 3 \times 5 \times 7 = 840$

The LCM above will be a multiple of $105$ because it contains $3 \times 5 \times 7$, and will be a multiple of $120$ because it contains $2^3 \times 3 \times 5$. It will be the _lowest possible multiple_ as it contains the **fewest possible copies of the shared factors**.

Alternatively,
$\operatorname{lcm}(120,105) = \frac{|120 \cdot 105|}{\gcd(120,105)}$.
$\gcd(120, 105) = \gcd(105, 15) = \gcd(15, 0) = 15$
$\operatorname{lcm}(120,105) = \frac{|120 \cdot 105|}{15} = |8 \cdot 105| = 840$

---

## See Also

[[Mathematics/Number Theory/Prime Decomposition]]
[[Mathematics/Number Theory/Greatest Common Divisor]]
[[Mathematics/Number Theory/Fundamental Theorem of Arithmetic]]
