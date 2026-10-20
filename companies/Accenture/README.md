# Accenture Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💼

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

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Pseudocode Tracing:** Bitwise operations (`XOR`, `AND`, `OR`), nested while/for loops, recursion tracing.
- **Array Transformations:** Sum of odd/even elements, difference of sums, element replacement.
- **Strings & Character Operations:** Palindrome checks, anagrams, vowel transformations, run-length checks.
- **Basic Number Theory:** Binary to decimal conversions, base conversions, primes, GCD.
- **MS Office & Cloud Basics:** Excel shortcuts, formulas (`VLOOKUP`), cloud service models (`IaaS`, `PaaS`, `SaaS`).

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Operation Binary String (Accenture Signature)
- **College/Drive:** Pan-India On-Campus 2024
- **Problem Summary:** You are given a binary string $S$ containing digits '0' and '1' and alphabets 'A' (AND), 'B' (OR), 'C' (XOR). Scan from left to right and evaluate the binary expression.
- **Example:** `"1C0C1C1A0B1"` $\to$ evaluates left-to-right to `1`.
- **Approach:** Linear scan, maintaining running accumulator and applying the operator to the next digit.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Difference of Sums
- **College/Drive:** National Level NLA 2024
- **Problem Summary:** Given two integers $n$ and $m$. Return the difference between the sum of integers in the range $[1, m]$ that are NOT divisible by $n$, and the sum of integers that ARE divisible by $n$.
- **LeetCode Equivalent:** [2894. Divisible and Non-divisible Sums Difference](https://leetcode.com/problems/divisible-and-non-divisible-sums-difference/)
- **Approach:** Arithmetic progression formulas or simple loop up to $m$.
- **Complexity:** $O(1)$ Math formula or $O(M)$ loop.

#### 3. Password Checker & Validation
- **College/Drive:** Pool Campus Drive 2024
- **Problem Summary:** Check if a password string is valid: minimum 4 characters, at least 1 digit, at least 1 uppercase letter, no space or slash `'/'`, and first character must not be a number.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Move Zeroes to End of Array
- **College/Drive:** Campus Slot 1 (2024)
- **Problem Summary:** Given an integer array `nums`, move all `0`s to the end of it while maintaining the relative order of the non-zero elements in-place.
- **LeetCode Equivalent:** [283. Move Zeroes](https://leetcode.com/problems/move-zeroes/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Superior Elements in Array (Leaders Variant)
- **College/Drive:** Campus Slot 2 (2024)
- **Problem Summary:** An element is called superior if it is strictly greater than all elements to its right. Return count of superior elements.
- **Approach:** Reverse linear scan maintaining `max_from_right`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Rat Count House / Food Consumption
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Given $r$ rats and each rat needs $u$ units of food. An array `arr` has food units in each house. Find minimum houses needed to satisfy all rats.
- **Approach:** Running sum prefix loop until sum $\ge r \times u$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Character Carry in Base Addition
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Count total number of carry operations when adding two positive integers.
- **Complexity:** $O(\log_{10} N)$ Time.

#### 8. Maximum Subarray Sum (Kadane's)
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Maximum contiguous subarray sum.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time.

#### 9. Replace Character in String
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Given string $S$ and characters $c_1, c_2$. Replace all $c_1$ with $c_2$ and vice-versa.
- **Complexity:** $O(N)$ Time.

#### 10. Check Palindrome Number without Extra String Space
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Reverse integer with modulo arithmetic and compare.
- **Complexity:** $O(\log_{10} N)$ Time.

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
