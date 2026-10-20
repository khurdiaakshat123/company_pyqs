# HCL Technologies Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) 🏢

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **CoCubes (Aon)** / **Firstnaukri** / **Mettl**
- **Test Duration:** 90 to 120 minutes
- **Structure Breakdown:**
  1. **Cognitive Aptitude Section (45 mins):** Quantitative Ability (16 Q), Analytical / Logical Reasoning (16 Q), Verbal English (16 Q).
  2. **Technical MCQs Section (30 mins):** 20 to 25 MCQs covering C/C++, Java, OOPs concepts, Database Management (SQL), and Operating Systems.
  3. **Coding Section (30–45 mins, 2 Questions):** Focuses on array manipulations, string parsing, sorting, and number theory.
- **Negative Marking:** None. High accuracy across cognitive aptitude is strictly prioritized for entry-level hiring (Score $\ge 70\%$ recommended).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Basic Math & Number Theory:** Fibonacci series, prime factorization, factorial trailing zeroes, GCD/LCM, armstrong numbers.
- **String Manipulation:** Palindrome checks, anagrams, run-length encoding, vowel/consonant segregation.
- **Array Operations & Two Pointers:** In-place modifications, duplicate removal, two-sum variations, even-odd separation.
- **Technical MCQs (OOP & C++):** Pointers, static variables, inheritance types, operator overloading, SQL aggregate queries (`COUNT`, `GROUP BY`, joins).

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Count Trailing Zeroes in Factorial
- **College/Drive:** HCL First Careers Drive 2024 / SRM University
- **Problem Summary:** Given an integer $N$, return the number of trailing zeroes in $N!$.
- **LeetCode Equivalent:** [172. Factorial Trailing Zeroes](https://leetcode.com/problems/factorial-trailing-zeroes/)
- **Approach:** Count factors of 5 by iteratively adding $\lfloor N / 5^k \rfloor$ for $5^k \le N$.
- **Complexity:** $O(\log_5 N)$ Time, $O(1)$ Space.

#### 2. Segregate Positive and Negative Numbers In-Place
- **College/Drive:** Amity University / KIIT 2024
- **Problem Summary:** Given an unsorted array of integers, modify it in-place such that all negative integers appear before all positive integers.
- **LeetCode Equivalent:** [Dutch National Flag variant](https://leetcode.com/problems/sort-colors/)
- **Approach:** Two pointers: one starting from left scanning for positive numbers, another swapping with negative numbers found.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. Valid Anagram String Verification
- **College/Drive:** Chandigarh University 2024
- **Problem Summary:** Given two strings $S$ and $T$, return `true` if $T$ is an anagram of $S$, and `false` otherwise.
- **LeetCode Equivalent:** [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- **Approach:** 26-element integer frequency array or hash map; verify all frequencies cancel out.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Remove Duplicates from Sorted Array
- **College/Drive:** HCL TechBee / Campus Slot 2024
- **Problem Summary:** Given an integer array sorted in non-decreasing order, remove duplicates in-place such that each unique element appears once.
- **LeetCode Equivalent:** [26. Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)
- **Approach:** Two pointer index tracking: `k = 1`; if `nums[i] != nums[k-1]`, assign `nums[k++] = nums[i]`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Find the Missing Number in Range [0, n]
- **College/Drive:** LPU / Chitkara University 2024
- **Problem Summary:** Given an array containing $n$ distinct numbers in the range $[0, n]$, return the only number in the range that is missing.
- **LeetCode Equivalent:** [268. Missing Number](https://leetcode.com/problems/missing-number/)
- **Approach:** XOR sum or Gauss formula: $\frac{n(n+1)}{2} - \sum \text{nums}$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Second Largest Element in Array Without Sorting
- **College/Drive:** Campus Placement Slot 1 (2023)
- **Problem Summary:** Find second distinct largest element in an unsorted array in single pass.
- **Approach:** Maintain `first_max` and `second_max` initialized to $-\infty$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Reverse Words in a Given String
- **College/Drive:** Campus Placement Slot 2 (2023)
- **Problem Summary:** Given a string $S$, reverse the order of words without reversing individual characters.
- **LeetCode Equivalent:** [151. Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/)
- **Complexity:** $O(N)$ Time, $O(1)$ Auxiliary Space.

#### 8. Binary Search in Rotated Sorted Array
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Search target element in a sorted rotated array.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 9. Check if Linked List Has a Cycle
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Determine if a linked list contains a cycle.
- **LeetCode Equivalent:** [141. Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/)
- **Approach:** Floyd’s Cycle-Finding Algorithm (slow and fast pointers).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 10. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find the contiguous subarray with the largest sum.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent Technical & OOP MCQs Asked in HCL OA
1. **Virtual Functions in C++:**
   - Why do we need virtual destructors in base classes?
   - *Answer:* To ensure that the derived class destructor is invoked when deleting an object through a base class pointer, preventing memory leaks.
2. **Static Variables in Functions:**
   - What is the lifetime and scope of a `static` variable declared inside a C function?
   - *Answer:* Lifetime is the entire program execution (stored in data segment), but its scope is limited to the function in which it is defined.
3. **Primary Key vs Unique Key in SQL:**
   - Can a table have multiple Unique keys and multiple Primary keys?
   - *Answer:* A table can have multiple `UNIQUE` constraints, but only one `PRIMARY KEY`. Primary keys cannot accept `NULL` values.
