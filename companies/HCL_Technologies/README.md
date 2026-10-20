# HCL Technologies Online Assessment Guide & PYQs (2023 - 2025/2026) 🏢

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **CoCubes (Aon)** / **Firstnaukri** / **Mettl**
- **Test Duration:** 90 to 120 minutes
- **Structure Breakdown:**
  1. **Cognitive Aptitude Section (45 mins):** Quantitative Ability (16 Q), Analytical / Logical Reasoning (16 Q), Verbal English (16 Q).
  2. **Technical MCQs Section (30 mins):** 20 to 25 MCQs covering C/C++, Java, OOPs concepts, Database Management (SQL), and Operating Systems.
  3. **Coding Section (30–45 mins, 1 to 2 Questions):** Focuses on basic to intermediate array, string, and number theory implementations.
- **Negative Marking:** None. High accuracy across cognitive aptitude is strictly prioritized for entry-level hiring.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Basic Math & Number Theory | Easy | Fibonacci series, Prime factorization, Factorial trailing zeroes, GCD/LCM |
| **Very High** | String Manipulation | Easy | Palindrome checks, string reversal without library, count vowels and consonants |
| **High** | Array Traversal & Operations | Easy | Even-odd separation, element frequency, matrix diagonal sum |
| **High** | Technical MCQs (OOP & C++) | Easy - Medium | Pointers, static variables, inheritance types, SQL aggregate queries |
| **Medium** | Searching & Sorting | Easy | Binary search, selection sort simulation |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Count Trailing Zeroes in Factorial
- **Problem Summary:** Given an integer $n$, return the number of trailing zeroes in $n!$.
- **LeetCode Equivalent:** [172. Factorial Trailing Zeroes](https://leetcode.com/problems/factorial-trailing-zeroes/)
- **Approach:** Count factors of 5: $\sum_{k=1}^{\infty} \lfloor \frac{n}{5^k} \rfloor$.
- **Complexity:** $O(\log_5 n)$ Time, $O(1)$ Space.

### 2. Move Negative Numbers to Beginning
- **Problem Summary:** Given an unsorted array of numbers, move all negative numbers to the beginning and positive numbers to the end in-place.
- **Approach:** Two pointers (Dutch national flag partition style).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 3. Check for Anagram Strings
- **Problem Summary:** Given two strings $s$ and $t$, return true if $t$ is an anagram of $s$, and false otherwise.
- **LeetCode Equivalent:** [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- **Approach:** 26-element character frequency array.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 4. Remove Duplicates from Sorted Array
- **Problem Summary:** Given an integer array `nums` sorted in non-decreasing order, remove duplicates in-place such that each unique element appears only once.
- **LeetCode Equivalent:** [26. Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.
