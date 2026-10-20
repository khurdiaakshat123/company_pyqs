# TCS (Tata Consultancy Services) Online Assessment Guide & PYQs (2023 - 2025/2026) 🏢

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

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Number Theory & Math | Easy - Medium | Armstrong numbers, Prime factors, Base conversion, Harshad numbers |
| **Very High** | Strings & Palindromes | Easy - Medium | Longest palindromic substring, character frequency, word reversal |
| **High** | Arrays & Matrix Manipulations | Medium | 90-degree matrix rotation, spiral order, two-sum variations |
| **High** | Dynamic Programming (Prime/Digital) | Medium - Hard | Coin change, knapsack, longest increasing subsequence |
| **Medium** | Graph & Grid Traversals | Medium | Number of islands, grid path counting with obstacles |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Matrix Rotation by 90 Degrees Clockwise (TCS Digital)
- **Problem Summary:** Given an $N \times N$ integer matrix, rotate it clockwise by 90 degrees in-place without creating a secondary matrix.
- **Approach:** First transpose the matrix along the main diagonal (`swap(matrix[i][j], matrix[j][i])`), then reverse each row horizontally.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Extra Space.

### 2. Vehicle Production and Wheel Count
- **Problem Summary:** An automobile company manufactures 2-wheelers and 4-wheelers. Given total number of vehicles $V$ and total number of wheels $W$, find the exact number of 2-wheelers ($TW$) and 4-wheelers ($FW$).
- **Mathematical Formula:**
  - $TW + FW = V$
  - $2TW + 4FW = W \implies FW = \frac{W - 2V}{2}$, and $TW = V - FW$.
  - Return invalid if $W < 2$, $W \% 2 \ne 0$, or $FW < 0$.
- **Complexity:** $O(1)$ Time.

### 3. Longest Palindromic Substring (TCS Digital / Prime)
- **Problem Summary:** Given a string $s$, return the longest palindromic substring in $s$.
- **LeetCode Equivalent:** [5. Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/)
- **Approach:** Expand around center for all $2N-1$ candidate centers.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Space.

### 4. Prime Number Pairs with Difference K (Twin Primes Variant)
- **Problem Summary:** Given a range $[L, R]$ and integer $D$, find all pairs of prime numbers $(p_1, p_2)$ within the range such that $p_2 - p_1 = D$.
- **Approach:** Sieve of Eratosthenes up to $R$, then scan for valid pairs.
- **Complexity:** $O(R \log \log R)$ Time.

---

## 🧠 Frequent Quantitative Aptitude Formulas in TCS NQT
1. **Time and Work Equations:** If $A$ works at rate $\frac{1}{a}$ and $B$ at rate $\frac{1}{b}$, combined time = $\frac{ab}{a + b}$.
2. **Speed-Time Distance on Trains:** A train of length $L_1$ crossing a platform of length $L_2$ at speed $S$: Time = $\frac{L_1 + L_2}{S}$.
3. **Compound Interest vs Simple Interest:** Difference for 2 years = $P \times \left(\frac{R}{100}\right)^2$.
