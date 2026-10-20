# Meesho Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🛍️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **HackerEarth**
- **Test Duration:** 90 to 110 minutes
- **Structure Breakdown:**
  - **3 Algorithmic Coding Questions** (Ranging from Medium to Hard).
  - 10 to 15 Core Computer Science MCQs (DBMS/SQL, Operating Systems, Computer Networks).
- **Evaluation Criteria:**
  - Meesho is renowned for setting exceptionally demanding Online Assessments with CP-style problems and massive numerical constraints ($K \le 10^{12}$ or $N \le 36$).
  - Solving 2 questions completely with all test cases passed + strong MCQ accuracy is typically necessary for an interview callback.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Meet-in-the-Middle & Bitmask DP | Hard | Subset sum with $N \le 36$, partition problems |
| **Very High** | Array Optimization with Large K | Hard | Periodic simulation, modular arithmetic for $K \le 10^{12}$ |
| **High** | Strings & Sliding Window Frequencies | Medium - Hard | Character frequency thresholds, anagram substrings, rolling hash |
| **High** | Greedy Array Rearrangement | Medium - Hard | Maximizing index-weighted products after element swaps |
| **Medium** | Core CS MCQs (DBMS / OS) | Medium | SQL indexing, B+ Trees, CPU scheduling, deadlocks |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Partition with Meet-in-the-Middle ($N \le 36$)
- **Problem Summary:** Given an array of $N$ integers ($N \le 36$) and a target $T$, find the number of subsets whose sum is at most $T$.
- **Approach:** Standard recursion $O(2^{36})$ times out; dynamic programming memory limit exceeded due to large element values ($10^9$).
  - Split array into two halves of size $N/2 \le 18$.
  - Generate and sort all $2^{18}$ subset sums of the second half.
  - For each subset sum in the first half, use `std::upper_bound` to binary search compatible subsets in the second half.
- **Complexity:** $O(2^{N/2} \log(2^{N/2})) = O(N \cdot 2^{N/2})$ Time.

### 2. Large K Periodic Bitwise Array Simulation ($K \le 10^{12}$)
- **Problem Summary:** Given an array of integers $A$. In each step, replace $A[i]$ with $A[i] \oplus A[(i + 1) \% N]$. Determine the array configuration after $K$ steps, where $K$ can be up to $10^{12}$.
- **Approach:** The operation is linear over $GF(2)$. By Lucas' Theorem and properties of binomial coefficients modulo 2, after $2^p$ steps, $A[i] \to A[i] \oplus A[(i + 2^p) \% N]$. Decompose $K$ into powers of 2.
- **Complexity:** $O(N \log K)$ Time.

### 3. Maximizing Index-Weighted Difference Sum
- **Problem Summary:** Given two arrays $A$ and $B$ of size $N$. You can permute $B$ in any order. Maximize the sum $\sum_{i=1}^N i \cdot (B[i] - A[i])$.
- **Approach:** Rearrangement inequality: To maximize $\sum i \cdot B[i]$, sort array $B$ in strictly ascending order and align larger elements with larger indices $i$.
- **Complexity:** $O(N \log N)$ Time.

### 4. Substring Frequency Thresholds
- **Problem Summary:** Return the count of substrings in $S$ where the most frequent character appears at least $K$ times and at most $M$ times.
- **Approach:** Two Pointers / Sliding window iterating over unique characters.
- **Complexity:** $O(26 \times N)$ Time.
