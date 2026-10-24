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
- **Array Transformations:** Sum of odd/even elements, difference of sums, element replacement, large small sum.
- **Strings & Character Operations:** Operation binary string, palindrome checks, anagrams, vowel transformations.
- **Basic Algorithms:** Kadane's algorithm, two sum, rotated sorted array search, inversion count.
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

#### 6. Large Small Sum (Accenture Signature Array Puzzle)
- **College/Drive:** Pan-India Campus 2024 / VIT Vellore
- **Problem Summary:** Given an integer array `arr` of size $n$, find the sum of the second largest element from even positions (0-indexed) and the second smallest element from odd positions. If array length $\le 3$, return 0.
- **Approach:** Separate even and odd indexed elements into two temporary arrays or find 1st/2nd extrema with a single pass, then sum `second_largest_even + second_smallest_odd`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Longest Substring Without Repeating Characters
- **College/Drive:** SRM University / Manipal 2024
- **Problem Summary:** Given a string `s`, find the length of the longest substring without repeating characters.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with hash map storing last seen index of each character.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 8. Inversion Count in an Array
- **College/Drive:** Accenture Advanced Coding 2024
- **Problem Summary:** Given an array of integers, find the number of inversion pairs $(i, j)$ such that $i < j$ and $arr[i] > arr[j]$.
- **Approach:** Enhanced Merge Sort: during the merge step, whenever an element from the right subarray is picked, add $(mid - i + 1)$ to total inversions.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 9. Search in Rotated Sorted Array
- **College/Drive:** Accenture Tech Drive 2024
- **Problem Summary:** Given an integer array `nums` sorted in ascending order and rotated at an unknown pivot, find the index of a given `target`.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking which half is monotonically ordered.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 10. Valid Anagram String Verification
- **College/Drive:** Pan-India 2024
- **Problem Summary:** Given two strings `s` and `t`, return `true` if `t` is an anagram of `s`, and `false` otherwise.
- **LeetCode Equivalent:** [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- **Approach:** 26-length frequency array tracking character counts.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Rat Count House / Food Consumption
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Given $r$ rats and each rat needs $u$ units of food. An array `arr` has food units in each house. Find minimum houses needed to satisfy all rats.
- **Approach:** Running sum prefix loop until sum $\ge r \times u$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Character Carry in Base Addition
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Count total number of carry operations when adding two positive integers.
- **Complexity:** $O(\log_{10} N)$ Time.

#### 13. Maximum Subarray Sum (Kadane's)
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Maximum contiguous subarray sum.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time.

#### 14. Replace Character in String
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Given string $S$ and characters $c_1, c_2$. Replace all $c_1$ with $c_2$ and vice-versa.
- **Complexity:** $O(N)$ Time.

#### 15. Check Palindrome Number without Extra String Space
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Reverse integer with modulo arithmetic and compare.
- **LeetCode Equivalent:** [9. Palindrome Number](https://leetcode.com/problems/palindrome-number/)
- **Complexity:** $O(\log_{10} N)$ Time.

#### 16. Two Sum (Pair Target Sum)
- **College/Drive:** Pan-India Hiring 2023
- **Problem Statement:** Return indices of two numbers that add up to target.
- **LeetCode Equivalent:** [1. Two Sum](https://leetcode.com/problems/two-sum/)
- **Approach:** One-pass Hash Map.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 17. Reverse Singly Linked List In-Place
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Reverse singly linked list in-place and return new head.
- **LeetCode Equivalent:** [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
- **Approach:** Three pointers (`prev`, `curr`, `next`).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 18. Trapping Rain Water (Advanced Track)
- **College/Drive:** Accenture Advanced Coding 2023
- **Problem Statement:** Given $n$ non-negative integers representing elevation map, compute trapped rainwater.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers from left and right inward.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 19. Second Largest Element in Array
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Find second largest element without sorting.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 20. Automorphic Number Verification
- **College/Drive:** Campus Slot 2023
- **Problem Statement:** A number is automorphic if the square of the number ends with the same digits as the number itself (e.g. $5^2 = 25$, $76^2 = 5776$). Determine if $N$ is automorphic.
- **Approach:** Compute $N^2$. Check if $N^2 \pmod{10^k} == N$ where $k$ is number of digits in $N$.
- **Complexity:** $O(\log_{10} N)$ Time, $O(1)$ Space.

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
