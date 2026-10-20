# Accenture Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 💼

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **AON (CoCubes)** / **Wheebox** / **Superset**
- **Hiring Process Architecture (Elimination Rounds):**
  1. **Stage 1: Cognitive & Technical Assessment (90 minutes, 90 Questions)** – Strict elimination round.
     - English Ability (17 Questions)
     - Critical Thinking & Problem Solving (18 Questions)
     - Abstract Reasoning (18 Questions)
     - Common Applications & MS Office (12 Questions)
     - Pseudocode & Code Tracing (18 Questions)
     - Networking, Cloud & Security Fundamentals (10 Questions)
  2. **Stage 2: Hands-On Coding Assessment (45 minutes, 2 Questions)** – Unlocks immediately if Stage 1 threshold is passed.
  3. **Stage 3: Communication Assessment (Voice-proctored, ~20 mins)** – Reading, repeating sentences, conversation simulation.
- **Negative Marking:** No negative marking, but strict section-wise cutoffs apply.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Pseudocode Tracing | Easy - Medium | Bitwise operations (`XOR`, `AND`, `OR`), nested while/for loops, recursion tracing |
| **Very High** | Array Transformations | Easy | Sum of odd/even elements, difference of sums, element replacement |
| **High** | Strings & Character Operations | Easy | Palindrome checks, anagrams, vowel transformations, run-length checks |
| **High** | Basic Number Theory | Easy | Binary to decimal conversions, base conversions, primes, GCD |
| **Medium** | MS Office & Cloud Basics | Easy | Excel shortcuts, formulas (`VLOOKUP`), cloud service models (`IaaS`, `PaaS`, `SaaS`) |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Operation Binary String
- **Problem Summary:** You are given a binary string $S$ containing digits '0' and '1' and alphabets 'A' (AND), 'B' (OR), 'C' (XOR). Scan from left to right and evaluate the binary expression.
- **Example:** `"1C0C1C1A0B1"` $\to$ evaluates left-to-right to `1`.
- **Approach:** Linear scan, maintaining running accumulator and applying the operator to the next digit.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 2. Difference of Sums
- **Problem Summary:** Given two integers $n$ and $m$. Return the difference between the sum of integers in the range $[1, m]$ that are NOT divisible by $n$, and the sum of integers that ARE divisible by $n$.
- **LeetCode Equivalent:** [2894. Divisible and Non-divisible Sums Difference](https://leetcode.com/problems/divisible-and-non-divisible-sums-difference/)
- **Approach:** Arithmetic progression formulas or simple loop up to $m$.
- **Complexity:** $O(1)$ Math formula or $O(M)$ loop.

### 3. Password Checker
- **Problem Summary:** Check if a password string is valid: minimum 4 characters, at least 1 digit, at least 1 uppercase letter, no space or slash `'/'`, and first character must not be a number.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 4. Move Zeroes to End of Array
- **Problem Summary:** Given an integer array `nums`, move all `0`s to the end of it while maintaining the relative order of the non-zero elements in-place.
- **LeetCode Equivalent:** [283. Move Zeroes](https://leetcode.com/problems/move-zeroes/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent Pseudocode Snippets in Accenture OA
```text
Integer a, b, c
Set a = 4, b = 6, c = 2
if ((a & b) < (b ^ c))
    a = a + b
else
    b = b + c
End if
Print a + b + c
```
*Tracing:* `4 & 6 = 4`, `6 ^ 2 = 4`. Since `4 < 4` is false, `b = 6 + 2 = 8`. Output is `4 + 8 + 2 = 14`.
