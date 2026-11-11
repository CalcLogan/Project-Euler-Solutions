# Project Euler - Problem 1: Multiples of 3 or 5

## Problem Statement
Find the sum of all multiples of 3 or 5 below 1000.

---

## Mathematical Derivation

Instead of a brute-force computational loop, we evaluate the arithmetic progression sums for multiples of 3 and 5 independently, then adjust for overlapping terms.

### 1. Sum of Multiples of 5 below 1000:
The largest multiple of 5 below 1000 is $995$. The number of terms is:
$$p = \frac{995}{5} = 199$$

Using the arithmetic series sum formula $S = \frac{p}{2}(a_1 + a_p)$:
$$S(5) = \frac{199}{2}(5 + 995) = \frac{199}{2}(1000) = 99,500$$

### 2. Sum of Multiples of 3 below 1000:
The largest multiple of 3 below 1000 is $999$. The number of terms is:
$$p = \frac{999}{3} = 333$$

$$S(3) = \frac{333}{2}(3 + 999) = \frac{333}{2}(1002) = 333 \times 501 = 166,833$$

### 3. Correction for Overlaps (Multiples of 15):
Numbers divisible by both 3 and 5 are counted twice. The largest multiple of $15$ below 1000 is $990$. The number of terms is:
$$p = \frac{990}{15} = 66$$

$$S(15) = \frac{66}{2}(15 + 990) = 33 \times 1005 = 33,165$$

---

### Final Calculation (Inclusion-Exclusion Principle):
$$\text{Total} = S(3) + S(5) - S(15)$$
$$\text{Total} = 166,833 + 99,500 - 33,165 = \mathbf{233,168}$$
