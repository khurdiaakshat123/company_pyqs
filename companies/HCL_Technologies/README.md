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
- **Basic Math & Number Theory:** Trailing zeroes in factorial, prime factorization, GCD/LCM, armstrong numbers.
- **String Manipulation:** Palindrome checks, anagrams, run-length encoding, vowel/consonant segregation, longest common prefix.
- **Array Operations & Two Pointers:** In-place modifications, duplicate removal, two-sum variations, even-odd separation, Dutch National Flag.
- **Linked Lists & Stacks:** Reverse linked list, cycle detection, valid parentheses.
- **Technical MCQs (OOP & C++):** Pointers, static variables, inheritance types, operator overloading, virtual destructors, SQL constraints.

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

#### 6. Palindrome Number Check Without String Conversion
- **College/Drive:** HCL First Careers Drive 2024
- **Problem Summary:** Determine whether an integer is a palindrome without converting it to a string.
- **LeetCode Equivalent:** [9. Palindrome Number](https://leetcode.com/problems/palindrome-number/)
- **Approach:** Revert second half of integer using `% 10` and `/ 10` until `rev >= x`.
- **Complexity:** $O(\log_{10} N)$ Time, $O(1)$ Space.

#### 7. Two Sum / Pair Target Sum
- **College/Drive:** Pan-India Campus 2024
- **Problem Summary:** Given an array of integers `nums` and target `target`, return indices of two numbers adding to target.
- **LeetCode Equivalent:** [1. Two Sum](https://leetcode.com/problems/two-sum/)
- **Approach:** One-pass Hash Map storing `target - nums[i]`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 8. Longest Common Prefix
- **College/Drive:** KIIT Bhubaneswar 2024
- **Problem Summary:** Find the longest common prefix among an array of strings.
- **LeetCode Equivalent:** [14. Longest Common Prefix](https://leetcode.com/problems/longest-common-prefix/)
- **Approach:** Vertical scanning character by character across all strings.
- **Complexity:** $O(S)$ Time where $S$ is sum of all characters.

#### 9. Move Zeroes to End of Array
- **College/Drive:** Chitkara University 2024
- **Problem Summary:** Move all 0s to end in-place preserving relative order.
- **LeetCode Equivalent:** [283. Move Zeroes](https://leetcode.com/problems/move-zeroes/)
- **Approach:** Two pointers: track index `insert_pos` for non-zero items.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 10. Reverse Singly Linked List In-Place
- **College/Drive:** Lovely Professional University 2024
- **Problem Summary:** Reverse singly linked list in-place and return new head.
- **LeetCode Equivalent:** [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
- **Approach:** Three pointers (`prev`, `curr`, `next`).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Second Largest Element in Array Without Sorting
- **College/Drive:** Campus Placement Slot 1 (2023)
- **Problem Summary:** Find second distinct largest element in an unsorted array in single pass.
- **Approach:** Maintain `first_max` and `second_max` initialized to $-\infty$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Reverse Words in a Given String
- **College/Drive:** Campus Placement Slot 2 (2023)
- **Problem Summary:** Given a string $S$, reverse the order of words without reversing individual characters.
- **LeetCode Equivalent:** [151. Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/)
- **Complexity:** $O(N)$ Time, $O(1)$ Auxiliary Space.

#### 13. Binary Search in Rotated Sorted Array
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Search target element in a sorted rotated array.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 14. Check if Linked List Has a Cycle
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Determine if a linked list contains a cycle.
- **LeetCode Equivalent:** [141. Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/)
- **Approach:** Floyd’s Cycle-Finding Algorithm (slow and fast pointers).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 15. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find the contiguous subarray with the largest sum.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. Find First and Last Position of Element in Sorted Array
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Find starting and ending indices of target element in sorted array.
- **LeetCode Equivalent:** [34. Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
- **Approach:** Two binary searches.
- **Complexity:** $O(\log N)$ Time.

#### 17. Merge Two Sorted Arrays In-Place
- **College/Drive:** Pan-India 2023
- **Problem Summary:** Merge `nums2` into `nums1` in non-decreasing order.
- **LeetCode Equivalent:** [88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)
- **Approach:** Fill backwards from end of `nums1`.
- **Complexity:** $O(M + N)$ Time, $O(1)$ Space.

#### 18. Valid Parentheses Expression
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Check if string containing brackets `'()[]{}'` is valid.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Stack data structure.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 19. Matrix Spiral Traversal
- **College/Drive:** University Drive 2023
- **Problem Summary:** Traverse $M \times N$ matrix in spiral order.
- **LeetCode Equivalent:** [54. Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
- **Approach:** 4-boundary traversal.
- **Complexity:** $O(M \times N)$ Time.

#### 20. Majority Element (Boyer-Moore Voting)
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Return element appearing more than $n / 2$ times.
- **LeetCode Equivalent:** [169. Majority Element](https://leetcode.com/problems/majority-element/)
- **Approach:** Boyer-Moore Voting Algorithm.
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
