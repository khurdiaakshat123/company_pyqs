# TCS (Tata Consultancy Services) Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) 🏢

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **TCS iON**
- **Hiring Tiers:**
  - **TCS Prime:** 9.0 LPA (Top performance in Advanced Section)
  - **TCS Digital:** 7.0 LPA (High score in Advanced Section)
  - **TCS Ninja:** 3.36 LPA (Foundation Section cleared)
- **Exam Architecture:**
  1. **Part A: Foundation Section (75 minutes)**
     - Numerical Ability (20 Questions, 25 mins)
     - Verbal Ability (25 Questions, 25 mins)
     - Reasoning Ability (20 Questions, 25 mins)
  2. **Part B: Advanced Section (90 minutes)**
     - Advanced Quantitative & Reasoning (15 Questions, 25 mins)
     - Advanced Coding (2 Questions, 65 mins)
- **Sectional Lock:** Sections are strictly timed; once time for a section expires, you are automatically transitioned to the next and cannot return.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Number Theory & Math:** Armstrong numbers, Prime factors, Base conversion, Harshad numbers.
- **Strings & Palindromes:** Longest palindromic substring, character frequency, word reversal.
- **Arrays & Matrix Manipulations:** 90-degree matrix rotation, spiral order, two-sum variations.
- **Dynamic Programming (Prime/Digital):** Coin change, knapsack, longest increasing subsequence.
- **Graph & Grid Traversals:** Number of islands, grid path counting with obstacles.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Matrix Rotation by 90 Degrees Clockwise (TCS Digital)
- **College/Drive:** TCS NQT Pan-India 2024
- **Problem Summary:** Given an $N \times N$ integer matrix, rotate it clockwise by 90 degrees in-place without creating a secondary matrix.
- **Approach:** First transpose the matrix along the main diagonal (`swap(matrix[i][j], matrix[j][i])`), then reverse each row horizontally.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Extra Space.

#### 2. Vehicle Production and Wheel Count (Mathematical Linear System)
- **College/Drive:** TCS Ninja National Drive 2024
- **Problem Summary:** An automobile company manufactures 2-wheelers and 4-wheelers. Given total vehicles $V$ and total wheels $W$, find the exact number of 2-wheelers ($TW$) and 4-wheelers ($FW$).
- **Mathematical Formula:** $FW = \frac{W - 2V}{2}$ and $TW = V - FW$.
- **Complexity:** $O(1)$ Time.

#### 3. Longest Palindromic Substring (TCS Digital / Prime)
- **College/Drive:** TCS Prime Special Drive 2024
- **Problem Summary:** Given a string $s$, return the longest palindromic substring in $s$.
- **LeetCode Equivalent:** [5. Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/)
- **Approach:** Expand around center for all $2N-1$ candidate centers.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Space.

#### 4. Prime Number Pairs with Difference K (Twin Primes Variant)
- **College/Drive:** TCS NQT Slot 2 (2024)
- **Problem Summary:** Given a range $[L, R]$ and integer $D$, find all pairs of prime numbers $(p_1, p_2)$ within the range such that $p_2 - p_1 = D$.
- **Approach:** Sieve of Eratosthenes up to $R$, then scan for valid pairs.
- **Complexity:** $O(R \log \log R)$ Time.

#### 5. Maximum Element in Array After M Operations
- **College/Drive:** TCS Digital 2024
- **Problem Summary:** Given an array initialized to zeroes, execute $M$ range update operations adding value $K$ to range $[L, R]$ and return the maximum value in the array.
- **Approach:** Difference array (Prefix Sum technique).
- **Complexity:** $O(N + M)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Armstrong Number Verification
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Check if number equals sum of digits raised to power of count of digits.
- **Complexity:** $O(\log_{10} N)$ Time.

#### 7. Find Second Largest Element in Array
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Find second maximum distinct integer in array.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Remove Duplicates from Sorted Array
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Remove duplicate values in-place.
- **LeetCode Equivalent:** [26. Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Coin Change (Fewest Coins)
- **College/Drive:** TCS Prime 2023
- **Problem Statement:** Minimum coins to form payment sum.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 10. Valid Parentheses
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Balanced brackets check using Stack.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Complexity:** $O(N)$ Time.
