# Cognizant Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💼

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **AMCAT (Aspiring Minds)** / **Superset**
- **Hiring Tiers:**
  - **GenC Next:** 6.75 LPA (Requires high score in Advanced Coding)
  - **GenC Elevate:** 4.25 LPA (Intermediate Coding + Cognitive score)
  - **GenC:** 4.0 LPA (Cognitive + Basic Coding)
- **Structure Breakdown:**
  1. **Cognitive Ability Section (40 mins):** Quantitative Ability (16 Q), Logical Ability (14 Q), Verbal Ability (18 Q).
  2. **Technical Assessment & Automata Fix (35 mins):** 7 Code debugging / syntax and logic bug-fixing snippets.
  3. **Hands-On Coding Section (45 mins, 2 Questions):**
     - Question 1: Easy (Strings, Math, Array frequency)
     - Question 2: Medium (Two pointers, Matrix traversal, DP basics for GenC Next)
- **Adaptive Scoring:** AMCAT dynamically scales question difficulty based on consecutive correct responses.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Code Debugging (Automata Fix):** Infinite loops, missing base cases, boundary overflows, incorrect comparison operators.
- **Basic Math & Modulo Arithmetic:** Prime checks, Armstrong, Palindromic numbers, arithmetic progression missing terms.
- **Strings & Anagrams:** Frequency maps, character removal to balance string, Caesar cipher, longest substring.
- **Arrays & Two Pointers:** In-place removal, maximum subarray sum, balance points, rotated array search.
- **Linked Lists & Stacks:** Reverse linked list, valid parentheses.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Unique Character Frequency Balance
- **College/Drive:** Cognizant GenC Next Campus 2024
- **Problem Summary:** Given a string $S$, determine the minimum number of character deletions needed such that no two distinct characters have the same frequency.
- **LeetCode Equivalent:** [1647. Minimum Deletions to Make Character Frequencies Unique](https://leetcode.com/problems/minimum-deletions-to-make-character-frequencies-unique/)
- **Approach:** Count frequencies of each character. Use a Hash Set of used frequencies; decrement frequency and count deletions until an unused frequency or 0 is reached.
- **Complexity:** $O(N)$ Time, $O(1)$ Space (alphabet bounded).

#### 2. Array Leader Elements
- **College/Drive:** GenC Elevate 2024
- **Problem Summary:** Given an array $A$, find all "leaders" (elements that are strictly greater than all elements to their right). The rightmost element is always a leader.
- **Approach:** Traverse array from right to left maintaining `max_from_right`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. Missing Number in Arithmetic Progression
- **College/Drive:** National Level Drive 2024
- **Problem Summary:** Given an array representing an arithmetic progression where exactly one element is missing, find the missing value.
- **Approach:** Common difference $d = \frac{A[n-1] - A[0]}{n}$. Linear scan or Binary Search comparing expected value $A[0] + i \times d$.
- **Complexity:** $O(\log N)$ or $O(N)$ Time.

#### 4. Matrix Spiral Form Traversal
- **College/Drive:** GenC Next Slot 1 (2024)
- **Problem Summary:** Print elements of an $M \times N$ matrix in clockwise spiral form.
- **LeetCode Equivalent:** [54. Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
- **Approach:** Four boundaries (`top`, `bottom`, `left`, `right`) shrunk cyclically.
- **Complexity:** $O(M \times N)$ Time, $O(1)$ Extra Space.

#### 5. Move Zeroes to End of Array
- **College/Drive:** Campus Slot 2 (2024)
- **Problem Summary:** In-place move zeroes to end maintaining relative order.
- **LeetCode Equivalent:** [283. Move Zeroes](https://leetcode.com/problems/move-zeroes/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 6. Trapping Rain Water (GenC Next Advanced Track)
- **College/Drive:** Cognizant GenC Next 2024 / VIT Vellore
- **Problem Summary:** Given elevation map of width 1, compute total trapped water.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers inward from left and right maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Longest Substring Without Repeating Characters
- **College/Drive:** SRM / Manipal 2024
- **Problem Summary:** Find length of longest substring without duplicate characters.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with hash map storing character positions.
- **Complexity:** $O(N)$ Time.

#### 8. Subarray Sum Equals K
- **College/Drive:** Pan-India GenC Next 2024
- **Problem Summary:** Total number of continuous subarrays whose sum equals $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency tracking.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 9. Search in Rotated Sorted Array
- **College/Drive:** GenC Next Off-Campus 2024
- **Problem Summary:** Find target index in rotated sorted array in $O(\log N)$ time.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Modified binary search.
- **Complexity:** $O(\log N)$ Time.

#### 10. Reverse Singly Linked List In-Place
- **College/Drive:** Thapar University 2024
- **Problem Summary:** Reverse singly linked list in-place and return new head.
- **LeetCode Equivalent:** [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
- **Approach:** Three pointers (`prev`, `curr`, `next`).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Missing Number in Sequence 0 to N
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Find missing number in array.
- **LeetCode Equivalent:** [268. Missing Number](https://leetcode.com/problems/missing-number/)
- **Complexity:** $O(N)$ Time.

#### 12. Valid Anagram String Verification
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Check if two strings are anagrams.
- **LeetCode Equivalent:** [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- **Complexity:** $O(N)$ Time.

#### 13. Maximum Subarray Sum (Kadane's)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Largest sum contiguous subarray.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time.

#### 14. Palindrome Number Check
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Modulo arithmetic palindrome check.
- **Complexity:** $O(\log_{10} N)$ Time.

#### 15. Matrix Diagonal Difference
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Absolute difference between primary and secondary diagonal sums.
- **Complexity:** $O(N)$ Time.

#### 16. Two Sum (Target Pair)
- **College/Drive:** Pan-India Drive 2023
- **Problem Statement:** Find indices of two numbers that add up to target.
- **LeetCode Equivalent:** [1. Two Sum](https://leetcode.com/problems/two-sum/)
- **Approach:** One-pass Hash Map.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 17. Merge Two Sorted Arrays In-Place
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Merge `nums2` into `nums1` in sorted order.
- **LeetCode Equivalent:** [88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)
- **Approach:** Three pointers filling backwards.
- **Complexity:** $O(M + N)$ Time, $O(1)$ Space.

#### 18. Valid Parentheses Expression
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Check if bracket sequence is valid.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Stack data structure.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 19. Automata Fix Snippet: Selection Sort Boundary Bug
- **College/Drive:** Cognizant Automata Fix 2023
- **Buggy Code:**
  ```c
  for (i = 0; i <= n; i++) { // Bug: out of bounds
      min_idx = i;
      for (j = i + 1; j < n; j++) {
          if (arr[j] > arr[min_idx]) // Bug: reverse comparison for ascending
              min_idx = j;
      }
      swap(&arr[min_idx], &arr[i]);
  }
  ```
- **Fix:** Change outer loop to `i < n - 1` and inner comparison to `arr[j] < arr[min_idx]`.

#### 20. Automata Fix Snippet: Matrix Transpose Off-By-One
- **College/Drive:** Cognizant Automata Fix 2023
- **Buggy Code:**
  ```c
  for (int i = 0; i < n; i++) {
      for (int j = 0; j < n; j++) { // Bug: re-swapping reverts transpose
          int temp = mat[i][j];
          mat[i][j] = mat[j][i];
          mat[j][i] = temp;
      }
  }
  ```
- **Fix:** Change inner loop to `for (int j = i + 1; j < n; j++)`.
