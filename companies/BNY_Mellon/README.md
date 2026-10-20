# BNY Mellon Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Flagship Recruitment Programs:**
  - **BNY Mellon Code Divas:** National diversity hackathon & hiring challenge (18–25 LPA).
  - **Campus Placement Drives (IITs, NITs, BITS, Top State Universities).**
- **Test Duration:** 90 to 120 minutes
- **Structure Breakdown:**
  - 4 Coding Questions (1 Easy, 2 Medium, 1 Hard).
- **Cutoff Benchmark:** Clearing 3 to 4 coding questions completely is standard to qualify for the interview shortlist or Code Divas finalists.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Range Queries & Segment Trees:** First index meeting threshold, point updates.
- **Interval Coverage & Fountains:** Greedy fountain/sprinkler activation.
- **Number Theory & Smallest Prime Factor:** Sieve factorization range queries.
- **Graph & 2D Grid Traversals:** Island counting, connected components.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Fountains Activation / Minimum Sprinklers (BNY Classic)
- **College/Drive:** BNY Code Divas / Top NITs 2024
- **Problem Statement:** A garden of length $N$ has $N$ fountains at positions $1$ to $N$. The $i$-th fountain can cover range $[\max(1, i - A[i]), \min(N, i + A[i])]$. Return the minimum number of fountains that must be activated to cover the entire garden from $1$ to $N$.
- **LeetCode Equivalent:** [1326. Minimum Number of Taps to Open to Water a Garden](https://leetcode.com/problems/minimum-number-of-taps-to-open-to-water-a-garden/)
- **Approach:** Transform to Jump Game II: For each position $L$, track the maximum right reach $R$. Greedily jump to the farthest reachable point.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 2. Range Query: First Index Meeting Threshold (Segment Tree)
- **College/Drive:** IIT Varanasi / BITS Pilani 2024
- **Problem Statement:** Given an array $A$ of size $N$. Process $Q$ queries: Given $[L, R]$ and value $X$, find the smallest index $P \in [L, R]$ such that $A[P] \le X$. If no such index exists, return -1.
- **Approach:** Segment Tree storing the minimum value in each range. Recurse into left child first; if left child's minimum is $\le X$, proceed left; otherwise explore right child.
- **Complexity:** $O(N)$ build, $O(\log N)$ query.

#### 3. Divisor Reduction with Smallest Prime Factors
- **College/Drive:** DTU / NSUT 2024
- **Problem Statement:** Given an array of integers $A$. In each step, you can divide any composite element by its smallest prime factor (SPF). Find the minimum total operations to reduce all elements in the array to 1.
- **Approach:** Precompute SPF array up to $\max(A)$ using linear Sieve of Eratosthenes. The answer for each number is simply its total count of prime factors (with multiplicity).
- **Complexity:** $O(M \log \log M)$ precomputation where $M = \max(A)$, $O(\log A[i])$ per element.

#### 4. Maximal Square in Binary Grid
- **College/Drive:** Code Divas Final Round 2024
- **Problem Statement:** Given an $m \times n$ binary matrix filled with 0's and 1's, find the largest square containing only 1's and return its area.
- **LeetCode Equivalent:** [221. Maximal Square](https://leetcode.com/problems/maximal-square/)
- **Approach:** 2D DP: $dp[i][j] = \min(dp[i-1][j], dp[i][j-1], dp[i-1][j-1]) + 1$.
- **Complexity:** $O(M \times N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Connected Network of Financial Nodes (Islands)
- **College/Drive:** On-Campus Drive Slot 1 (2023)
- **Problem Statement:** Count isolated settlement subnetworks in an interconnected banking matrix.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Approach:** BFS / DFS or Disjoint Set Union (DSU).
- **Complexity:** $O(M \times N)$ Time.

#### 6. Coordinate Range Interval Merging
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Merge overlapping transaction settlement windows.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 7. Minimum Window Substring with Modulo Check
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Find the shortest continuous substring that contains a target frequency of alphanumeric tokens.
- **Complexity:** $O(N)$ Time.

#### 8. Maximum Subarray Sum of Size at Least K
- **College/Drive:** Code Divas 2023
- **Problem Statement:** Given an array of integers, find the maximum sum of any contiguous subarray of length $\ge K$.
- **Approach:** Sliding window of size $K$ combined with Kadane's algorithm for previous prefix.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.
