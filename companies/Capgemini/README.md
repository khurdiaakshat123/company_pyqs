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
- **Array Transformations:** In-place modifications, moving zeros, finding missing elements.
- **String Manipulations:** Anagram checks, character frequency counting, vowel removals.
- **Basic Mathematics:** Factorial, prime numbers, Armstrong numbers, GCD.

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

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Missing Element in Sequence
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Find missing number from an unsorted array of size $N-1$ from $1$ to $N$.
- **LeetCode Equivalent:** [268. Missing Number](https://leetcode.com/problems/missing-number/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 6. Valid Anagram String Verification
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Check if two strings contain identical character counts.
- **LeetCode Equivalent:** [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- **Complexity:** $O(N)$ Time.

#### 7. Reverse Words in a Sentence
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Reverse word order in a string while maintaining single space separation.
- **LeetCode Equivalent:** [151. Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/)
- **Complexity:** $O(N)$ Time.

#### 8. Greatest Common Divisor (Euclid's Algorithm)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Compute GCD of two large numbers.
- **Complexity:** $O(\log(\min(A, B)))$ Time.
