# Cognizant Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 💼

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

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Code Debugging (Automata Fix) | Easy - Medium | Infinite loops, missing base cases, boundary overflows, incorrect operators |
| **Very High** | Basic Math & Modulo Arithmetic | Easy | Prime checks, Armstrong, Palindromic numbers, GCD/LCM |
| **High** | Strings & Anagrams | Easy - Medium | Frequency maps, character removal to balance string, Caesar cipher |
| **High** | Arrays & Two Pointers | Easy - Medium | In-place removal, maximum subarray sum, balance points |
| **Medium** | Matrix Traversal (GenC Next) | Medium | Spiral matrix, snake pattern, diagonal sums |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Unique Character Frequency Balance
- **Problem Summary:** Given a string $S$, determine the minimum number of character deletions needed such that no two distinct characters have the same frequency.
- **LeetCode Equivalent:** [1647. Minimum Deletions to Make Character Frequencies Unique](https://leetcode.com/problems/minimum-deletions-to-make-character-frequencies-unique/)
- **Complexity:** $O(N)$ Time.

### 2. Array Leader Elements
- **Problem Summary:** Given an array $A$, find all "leaders" (elements that are strictly greater than all elements to their right). The rightmost element is always a leader.
- **Approach:** Traverse array from right to left maintaining `max_from_right`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 3. Missing Number in Arithmetic Progression
- **Problem Summary:** Given an array representing an arithmetic progression where exactly one element is missing, find the missing value.
- **Approach:** Common difference $d = \frac{A[n-1] - A[0]}{n}$. Linear scan or Binary Search.
- **Complexity:** $O(\log N)$ or $O(N)$ Time.

### 4. Matrix Spiral Form Traversal
- **Problem Summary:** Print elements of an $M \times N$ matrix in clockwise spiral form.
- **Complexity:** $O(M \times N)$ Time, $O(1)$ Extra Space.
