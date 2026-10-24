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
- **Range Queries & Segment Trees:** First index meeting threshold, point updates, range minimum.
- **Interval Coverage & Fountains:** Greedy fountain/sprinkler activation, Jump Game II variants.
- **Number Theory & Prime Factorization:** Sieve factorization range queries, Smallest Prime Factor (SPF).
- **Graph & 2D Grid Traversals:** Island counting, connected components, rotting oranges, topological sort.
- **Dynamic Programming:** Maximal square, subarray sums, coin change, house robber.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Fountains Activation / Minimum Sprinklers (BNY Classic)
- **College/Drive:** BNY Code Divas / Top NITs 2024–2025
- **Problem Summary:** A garden of length $N$ has $N$ fountains at positions $1$ to $N$. The $i$-th fountain can cover range $[\max(1, i - A[i]), \min(N, i + A[i])]$. Return the minimum number of fountains that must be activated to cover the entire garden from $1$ to $N$.
- **Constraints:** $1 \le N \le 10^5$, $0 \le A[i] \le N$.
- **LeetCode Equivalent:** [1326. Minimum Number of Taps to Open to Water a Garden](https://leetcode.com/problems/minimum-number-of-taps-to-open-to-water-a-garden/)
- **Approach:** Transform to Jump Game II: For each position $L$, track the maximum right reach $R$. Greedily jump to the farthest reachable point.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 2. Range Query: First Index Meeting Threshold (Segment Tree)
- **College/Drive:** IIT Varanasi / BITS Pilani 2024–2025
- **Problem Summary:** Given an array $A$ of size $N$. Process $Q$ queries: Given $[L, R]$ and value $X$, find the smallest index $P \in [L, R]$ such that $A[P] \le X$. If no such index exists, return -1.
- **Constraints:** $1 \le N, Q \le 10^5$.
- **Approach:** Segment Tree storing the minimum value in each range. Recurse into left child first; if left child's minimum is $\le X$, proceed left; otherwise explore right child.
- **Complexity:** $O(N)$ build, $O(\log N)$ query.

#### 3. Divisor Reduction with Smallest Prime Factors
- **College/Drive:** DTU / NSUT 2024–2025
- **Problem Summary:** Given an array of integers $A$. In each step, you can divide any composite element by its smallest prime factor (SPF). Find the minimum total operations to reduce all elements in the array to 1.
- **Constraints:** $1 \le N \le 10^5$, $A[i] \le 10^6$.
- **Approach:** Precompute SPF array up to $\max(A)$ using linear Sieve of Eratosthenes. The answer for each number is simply its total count of prime factors (with multiplicity).
- **Complexity:** $O(M \log \log M)$ precomputation where $M = \max(A)$, $O(\log A[i])$ per element.

#### 4. Maximal Square in Binary Grid
- **College/Drive:** Code Divas Final Round 2024–2025
- **Problem Summary:** Given an $m \times n$ binary matrix filled with 0's and 1's, find the largest square containing only 1's and return its area.
- **Constraints:** $1 \le m, n \le 300$.
- **LeetCode Equivalent:** [221. Maximal Square](https://leetcode.com/problems/maximal-square/)
- **Approach:** 2D DP: $dp[i][j] = \min(dp[i-1][j], dp[i][j-1], dp[i-1][j-1]) + 1$.
- **Complexity:** $O(M \times N)$ Time, $O(N)$ Space.

#### 5. Connected Network of Financial Nodes (Islands)
- **College/Drive:** On-Campus Drive Slot 1 (2024–2025)
- **Problem Summary:** Count isolated settlement subnetworks in an interconnected banking matrix.
- **Constraints:** $M, N \le 300$.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Approach:** BFS / DFS or Disjoint Set Union (DSU).
- **Complexity:** $O(M \times N)$ Time.

#### 6. Subarray Sum Equals K
- **College/Drive:** BNY Mellon Pune Drive 2024
- **Problem Summary:** Count continuous subarrays summing to $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Hash Map tracking prefix sum frequencies.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Minimum Window Substring with Modulo Check
- **College/Drive:** Campus Hiring 2024
- **Problem Summary:** Find shortest continuous substring that contains a target frequency of alphanumeric tokens.
- **Constraints:** $1 \le |s|, |t| \le 10^5$.
- **LeetCode Equivalent:** [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- **Approach:** Two-pointer sliding window with frequency array.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 8. Maximum Subarray Sum of Size at Least K
- **College/Drive:** Code Divas 2024
- **Problem Summary:** Given an array of integers, find the maximum sum of any contiguous subarray of length $\ge K$.
- **Constraints:** $1 \le K \le N \le 10^5$.
- **Approach:** Sliding window of size $K$ combined with Kadane's algorithm for previous prefix.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Daily Temperatures / Metric Spike Monotonic Stack
- **College/Drive:** Campus Slot 2024
- **Problem Summary:** Find days to wait for a warmer day.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Off-Campus Screening 2024
- **Problem Summary:** Minimum minutes to infect all items in 2D grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Course Schedule II (Topological Sort)
- **College/Drive:** Campus Drive 2023–2024
- **Problem Summary:** Order tasks given dependencies.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm using indegrees and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 12. Coordinate Range Interval Merging
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Summary:** Merge overlapping transaction settlement windows.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time; merge overlaps.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 13. Coin Change (Fewest Coins)
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Minimum coins needed to make up amount.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 14. Trapping Rain Water
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 15. Lowest Common Ancestor in Binary Tree
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Find lowest common ancestor node in binary tree.
- **Constraints:** Nodes $\le 10^5$.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Approach:** Post-order DFS returning non-null branch.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 16. Product of Array Except Self without Division
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 17. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Sliding window with hash map storing last seen indices.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

#### 18. House Robber (1D Dynamic Programming)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Maximize stolen value without robbing two adjacent houses.
- **Constraints:** $1 \le nums.length \le 100$.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** DP: `dp[i] = max(dp[i-1], dp[i-2] + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 19. Search in Rotated Sorted Array
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Find target in rotated sorted array in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 5000$.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking sorted half.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 20. Container With Most Water
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Two pointers inward maximizing area between vertical lines.
- **Constraints:** $2 \le heights.length \le 10^5$.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 💡 Cracking BNY Mellon Code Divas & Campus OAs
1. **Prepare for 4 Full Coding Questions:** Unlike 2-question tests, BNY tests endurance and speed across 4 distinct problems.
2. **Master Segment Trees & Greedy Intervals:** Questions like *Fountain Activation* and *Range Query First Element $\le X$* are recurring BNY benchmarks.
3. **Number Theory Edge Cases:** Sieve preprocessing is mandatory when solving factorization problems with $10^5$ queries.
