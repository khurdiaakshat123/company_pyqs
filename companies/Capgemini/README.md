# Capgemini Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💼

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Mercer Mettl** / **Capgemini SpringBoard**
- **Hiring Tiers (Exceller Program):**
  - **Senior Analyst (Differential / High Package):** 5.75 to 7.5 LPA
  - **Analyst (Base Package):** 4.0 to 4.25 LPA
- **Structure Breakdown (Multi-Stage Elimination Process):**
  1. **Technical Pseudocode Assessment (30 mins, 30 Questions):** Tracing outputs of C, C++, and Java pseudocode snippets (Nested loops, recursion, bitwise operations, storage classes).
  2. **English Communication Test (30 mins, 30 Questions):** Grammar, vocabulary, error detection, sentence completion.
  3. **Game-Based Aptitude Assessment (24 mins, 4 Games):** Inductive reasoning grids, motion challenges, deductive logic games.
  4. **Hands-On Coding Assessment (45 mins, 2 Questions):** Easy to Medium algorithmic problems.
- **Negative Marking:** None.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Pseudocode Logic & Bitwise Operations:** Tracing `XOR`, `AND`, `OR`, bit-shifts, recursion trees.
- **Array Transformations:** In-place modifications, moving zeros, finding missing elements, second largest element.
- **String Manipulations:** Anagram checks, character frequency counting, vowel removals, palindrome verification.
- **Basic Algorithms & Dynamic Programming:** Kadane's maximum subarray, Boyer-Moore majority voting, binary search, two pointers.
- **Game-Based Aptitude:** Switch challenge, grid challenge, digit challenge.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. In-Place Segregation of Zeroes and Ones
- **College/Drive:** Pan-India Exceller Drive 2024
- **Problem Statement:** Given a binary array containing only 0s and 1s, segregate all 0s on the left side and all 1s on the right side of the array in a single traversal.
- **Approach:** Two Pointers (`left = 0`, `right = n - 1`). Swap when `arr[left] == 1` and `arr[right] == 0`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Count Vowels and Consonants in String
- **College/Drive:** Capgemini Pool Campus 2024
- **Problem Statement:** Given a string $S$, count the total number of vowels and consonants, ignoring digits, spaces, and punctuation.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. Sum of Distinct Elements in Array
- **College/Drive:** National Level Drive 2024
- **Problem Statement:** Given an array of integers with potential duplicate values, compute the sum of unique/distinct elements only.
- **Approach:** Hash Set or sorting with two pointers.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 4. Pseudocode Snippet: Nested Bitwise While Loop
- **College/Drive:** Exceller Assessment 2024
- **Pseudocode:**
  ```text
  Integer a, b, c
  Set a = 2, b = 5, c = 7
  if ((a ^ b) > (b & c))
      c = (a + b) ^ c
  else
      b = (a & b) + c
  End if
  Print a + b + c
  ```
- **Tracing:** `a ^ b = 2 ^ 5 = 7`. `b & c = 5 & 7 = 5`. Since `7 > 5` is true, `c = (2 + 5) ^ 7 = 7 ^ 7 = 0`. Output: `2 + 5 + 0 = 7`.

#### 5. Find Second Largest Element in Array Without Sorting
- **College/Drive:** Pan-India Exceller 2024 / VIT Vellore
- **Problem Statement:** Given an array of integers `nums`, find the second largest distinct element without sorting the array. If no second largest exists, return $-1$.
- **Approach:** Single traversal maintaining `first_max` and `second_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 6. Longest Substring Without Repeating Characters
- **College/Drive:** Capgemini Senior Analyst Drive 2024
- **Problem Statement:** Find the length of the longest substring without repeating characters.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with a hash map storing the latest index of each character.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 7. Majority Element (Boyer-Moore Voting)
- **College/Drive:** SRM Institute of Science and Technology 2024
- **Problem Statement:** Given an array `nums` of size $n$, return the majority element that appears more than $\lfloor n / 2 \rfloor$ times.
- **LeetCode Equivalent:** [169. Majority Element](https://leetcode.com/problems/majority-element/)
- **Approach:** Boyer-Moore Voting Algorithm: maintain `candidate` and `count`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Manipal Institute of Technology 2024
- **Problem Statement:** Find contiguous subarray with maximum sum in an integer array.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Approach:** Running sum: `curr = max(num, curr + num)`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Pseudocode Snippet: Recursive Modulo Function
- **College/Drive:** Capgemini Exceller Test 2024
- **Pseudocode:**
  ```text
  function fun(Integer x, Integer y)
      if (y == 0)
          return x
      return fun(y, x mod y)
  end function
  Print fun(48, 18)
  ```
- **Tracing:** Tracing Euclid's GCD: `fun(48, 18) -> fun(18, 12) -> fun(12, 6) -> fun(6, 0) -> returns 6`.

#### 10. Search in a 2D Matrix (Senior Analyst Track)
- **College/Drive:** Capgemini Senior Analyst 2024
- **Problem Statement:** Search for target value in an $M \times N$ matrix sorted row-wise and column-wise.
- **LeetCode Equivalent:** [74. Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/)
- **Approach:** Binary search on flattened 1D array coordinates.
- **Complexity:** $O(\log(M \times N))$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Missing Element in Sequence
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Find missing number from an unsorted array of size $N-1$ from $1$ to $N$.
- **LeetCode Equivalent:** [268. Missing Number](https://leetcode.com/problems/missing-number/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Valid Anagram String Verification
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Check if two strings contain identical character counts.
- **LeetCode Equivalent:** [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- **Complexity:** $O(N)$ Time.

#### 13. Reverse Words in a Sentence
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Reverse word order in a string while maintaining single space separation.
- **LeetCode Equivalent:** [151. Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/)
- **Complexity:** $O(N)$ Time.

#### 14. Greatest Common Divisor (Euclid's Algorithm)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Compute GCD of two large numbers.
- **Complexity:** $O(\log(\min(A, B)))$ Time.

#### 15. Palindrome Number Verification Without String Conversion
- **College/Drive:** Pan-India Drive 2023
- **Problem Statement:** Determine if an integer is a palindrome without converting it to a string.
- **LeetCode Equivalent:** [9. Palindrome Number](https://leetcode.com/problems/palindrome-number/)
- **Approach:** Revert second half of the number using modulo arithmetic: `rev = rev * 10 + x % 10`.
- **Complexity:** $O(\log_{10} N)$ Time, $O(1)$ Space.

#### 16. Move Zeroes to End of Array
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Move all 0's to the end of array while maintaining relative order of non-zero elements.
- **LeetCode Equivalent:** [283. Move Zeroes](https://leetcode.com/problems/move-zeroes/)
- **Approach:** Two pointers: `insert_pos` tracks location to place next non-zero element.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 17. Merge Two Sorted Arrays In-Place
- **College/Drive:** Capgemini Pool Campus 2023
- **Problem Statement:** Merge two sorted arrays `nums1` and `nums2` into `nums1`.
- **LeetCode Equivalent:** [88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)
- **Approach:** Three pointers filling backwards from index $m + n - 1$.
- **Complexity:** $O(M + N)$ Time, $O(1)$ Space.

#### 18. Find First and Last Position of Element in Sorted Array
- **College/Drive:** University Drive 2023
- **Problem Statement:** Given an array sorted in ascending order, find starting and ending position of a target value in $O(\log N)$ time.
- **LeetCode Equivalent:** [34. Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
- **Approach:** Two binary searches: one finding leftmost occurrence (`nums[mid] >= target`), one finding rightmost (`nums[mid] <= target`).
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 19. Frequency of Characters in String
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Given a string, output each character along with its frequency in order of first appearance.
- **Approach:** Fixed array of size 256 or Hash Map tracking counts.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 20. Check for Balanced Parentheses
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Determine if a string containing parentheses `'()[]{}'` is valid.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Stack data structure.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

## 🎮 Capgemini Game-Based Aptitude Breakdown
1. **Switch Challenge:**
   - Involves finding the rule that changes an initial sequence of 4 geometric symbols into an altered sequence using switch conduits.
2. **Digit Challenge:**
   - Rapid mental arithmetic equations where candidates complete mathematical expressions ($+, -, \times, \div$) to equal a target number using digits $1-9$.
3. **Motion Challenge:**
   - Grid-based marble maze where candidates remove obstacles in minimum moves to allow a ball to roll to the exit hole.
