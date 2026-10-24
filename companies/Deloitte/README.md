# Deloitte (USI) Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) 🏢

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **RippleNfinity** / **AMCAT** / **Mercer Mettl**
- **Hiring Tiers:**
  - **Consulting / Technology Analyst (USI):** 7.6 to 11.5 LPA
  - **Associate Analyst (Off-Campus / Mass Campus):** 4.0 to 6.0 LPA
- **Test Duration:** 90 to 105 minutes
- **Structure Breakdown:**
  1. **Quantitative Ability (25 mins, 20 Q):** Time-speed-distance, percentages, profit & loss, mixtures, permutations & probability.
  2. **Logical Reasoning (25 mins, 20 Q):** Syllogisms, coding-decoding, blood relations, seating arrangements, data sufficiency.
  3. **Verbal Ability (20 mins, 20 Q):** Reading comprehension, sentence correction, synonyms/antonyms, contextual vocabulary.
  4. **Computer Fundamentals & Coding (30 mins):**
     - 10 MCQs on OOPs, DBMS/SQL, and Operating Systems.
     - 1 to 2 Hands-on Coding Problems (Easy to Medium).
- **Negative Marking:** None. High overall accuracy across cognitive sections is mandatory.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Aptitude Formulas:** Time & work LCM, speed ratio, compound interest, mixtures.
- **Array Manipulations & Basics:** Second largest element, move zeroes, pair sum target, Kadane's maximum subarray.
- **Strings & Linked Lists:** Valid palindrome, reverse linked list, valid parentheses, longest common prefix.
- **Number Theory & Binary Search:** Prime range queries, Armstrong numbers, rotated array search.
- **SQL Queries:** Department aggregations, manager self-joins, window functions.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Second Largest Element in Array without Full Sorting
- **College/Drive:** Pan-India Campus Drive 2024
- **Problem Statement:** Given an array of integers, find the second largest distinct element without using pre-built sorting functions. If no second largest exists, return -1.
- **Approach:** Single linear traversal maintaining two variables: `max1` and `max2`. Update `max2 = max1` and `max1 = x` when $x > max1$; update `max2 = x` when $x > max2$ and $x \ne max1$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Prime Numbers in a Given Range [L, R]
- **College/Drive:** National Level NLA 2024
- **Problem Statement:** Given two positive integers $L$ and $R$, count the total number of prime numbers lying in the inclusive range $[L, R]$.
- **Approach:** Sieve of Eratosthenes up to $R$, count primes where `isPrime[i] == true`.
- **Complexity:** $O(R \log \log R)$ Time.

#### 3. Real SQL Question: Department Highest Average Salary
- **College/Drive:** Deloitte USI Campus Drive 2024
- **Problem Statement:** Write a query to find the department name that has the highest average employee salary, along with the average salary rounded to 2 decimal places.
- **SQL Implementation:**
  ```sql
  SELECT d.dept_name, ROUND(AVG(e.salary), 2) as avg_salary
  FROM Department d
  JOIN Employee e ON d.dept_id = e.dept_id
  GROUP BY d.dept_name
  ORDER BY avg_salary DESC
  LIMIT 1;
  ```

#### 4. Valid Palindrome String after Stripping Punctuation
- **College/Drive:** Off-Campus Drive 2024
- **Problem Statement:** Check whether a given sentence is a palindrome, considering only alphanumeric characters and ignoring cases.
- **LeetCode Equivalent:** [125. Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)
- **Approach:** Two Pointers from both ends skipping non-alphanumeric characters.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Trapping Rain Water (Consulting / Technology Track)
- **College/Drive:** Deloitte USI Tech Hiring 2024 / VIT Vellore
- **Problem Statement:** Given $n$ non-negative integers representing an elevation map where the width of each bar is 1, compute how much water it can trap after raining.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers inward from boundaries maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 6. Longest Substring Without Repeating Characters
- **College/Drive:** SRM / Manipal 2024
- **Problem Statement:** Given a string `s`, find the length of the longest substring without duplicate characters.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with hash map storing last seen index of each character.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 7. Merge Two Sorted Linked Lists
- **College/Drive:** Thapar University 2024
- **Problem Statement:** Merge two sorted singly linked lists into one sorted list and return its head.
- **LeetCode Equivalent:** [21. Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
- **Approach:** Iterative pointer comparison using dummy head node.
- **Complexity:** $O(N + M)$ Time, $O(1)$ Space.

#### 8. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Pan-India Drive 2024
- **Problem Statement:** Find contiguous subarray with maximum sum in integer array.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Approach:** `curr_sum = max(num, curr_sum + num)`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Real SQL: Employees Earning More Than Their Managers
- **College/Drive:** Deloitte USI 2024
- **Problem Statement:** Write a query to find employees who earn more than their direct managers.
- **SQL Implementation:**
  ```sql
  SELECT e.name AS Employee
  FROM Employee e
  JOIN Employee m ON e.manager_id = m.id
  WHERE e.salary > m.salary;
  ```

#### 10. Search in Rotated Sorted Array
- **College/Drive:** Deloitte Tech Placement 2024
- **Problem Statement:** Given integer array `nums` sorted in ascending order and rotated at unknown pivot, find index of target.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Modified binary search checking if left half or right half is strictly sorted.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Move All Zeroes to End of Array
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Move all 0's to the end of array in-place maintaining relative order of non-zero elements.
- **LeetCode Equivalent:** [283. Move Zeroes](https://leetcode.com/problems/move-zeroes/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Missing Number in Sequence 1 to N
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Find missing number from an array of size $N-1$ containing distinct numbers from 1 to $N$.
- **LeetCode Equivalent:** [268. Missing Number](https://leetcode.com/problems/missing-number/)
- **Approach:** Sum formula: $\frac{N(N+1)}{2} - \sum A[i]$ or XOR accumulator.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 13. Check for Anagram Strings
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Verify if two strings are valid anagrams.
- **LeetCode Equivalent:** [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- **Complexity:** $O(N)$ Time.

#### 14. Matrix Diagonal Difference
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Calculate absolute difference between the sums of matrix primary and secondary diagonals.
- **LeetCode Equivalent:** [1572. Matrix Diagonal Sum](https://leetcode.com/problems/matrix-diagonal-sum/)
- **Complexity:** $O(N)$ Time.

#### 15. Reverse Singly Linked List In-Place
- **College/Drive:** Pan-India Campus 2023
- **Problem Statement:** Reverse singly linked list in-place and return new head.
- **LeetCode Equivalent:** [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
- **Approach:** Three pointers: `prev`, `curr`, `next`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. Valid Parentheses Expression
- **College/Drive:** Campus Slot 2023
- **Problem Statement:** Determine if brackets `'()[]{}'` are closed in correct order.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Stack data structure.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 17. Longest Common Prefix
- **College/Drive:** Deloitte Hiring 2023
- **Problem Statement:** Find longest common prefix string among array of strings.
- **LeetCode Equivalent:** [14. Longest Common Prefix](https://leetcode.com/problems/longest-common-prefix/)
- **Approach:** Vertical character scan or sort first and last string.
- **Complexity:** $O(S)$ Time.

#### 18. Find First and Last Position in Sorted Array
- **College/Drive:** University Placement 2023
- **Problem Statement:** Find boundary indices of target element in sorted array.
- **LeetCode Equivalent:** [34. Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
- **Approach:** Dual binary search.
- **Complexity:** $O(\log N)$ Time.

#### 19. Two Sum (Target Pair)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to `target`.
- **LeetCode Equivalent:** [1. Two Sum](https://leetcode.com/problems/two-sum/)
- **Approach:** One-pass Hash Map.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 20. Majority Element (Boyer-Moore Voting)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Find element appearing more than $n / 2$ times.
- **LeetCode Equivalent:** [169. Majority Element](https://leetcode.com/problems/majority-element/)
- **Approach:** Boyer-Moore Voting Algorithm.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 High-Frequency Deloitte Cognitive Aptitude Formulas
1. **Work & Time:**
   - If A takes $x$ days and B takes $y$ days, together they take $\frac{xy}{x+y}$ days.
2. **Speed, Distance & Relative Motion:**
   - Train crossing moving object in same direction: Relative speed = $|S_1 - S_2|$.
   - Opposite direction: Relative speed = $S_1 + S_2$.
3. **Compound Interest vs Simple Interest Difference for 2 Years:**
   - $\text{Difference} = P \times \left(\frac{R}{100}\right)^2$.
