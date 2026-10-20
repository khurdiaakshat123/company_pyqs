# PhonePe Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🟣

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **DoSelect** / **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  - 3 to 4 Algorithmic Coding Problems (Competitive Programming / LeetCode Hard level).
  - No MCQs, pure high-difficulty algorithmic challenges.
- **Evaluation Criteria:**
  - PhonePe is known for setting some of the hardest OAs in the Indian product tech ecosystem (33+ LPA CTC).
  - Complex narrative problem statements with tight computational limits.
  - Solving 2 to 3 problems completely typically secures an interview shortlist.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Binary Search on Answer Space:** Minimum speed, delivery thresholds, capacity limits.
- **Grid Traversal & Shortest Path with Barriers:** Swim in rising water, 0-1 BFS.
- **Advanced Dynamic Programming:** Job scheduling, knapsack with non-standard weights.
- **Trees & Lowest Common Ancestor:** Heavy-Light decomposition, tree path queries.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Minimum Speed to Arrive on Time / Fast Payment Routing
- **College/Drive:** IIT Bombay / IIT Delhi 2024
- **Problem Statement:** You are given a floating point number `hour` representing the amount of time you have to reach the office, and an integer array `dist` where `dist[i]` is the distance of the $i$-th train ride. Each ride takes $\lceil \text{dist}[i] / \text{speed} \rceil$ hours (except the last which is fractional). Return the minimum positive integer speed that all trains must travel at, or -1 if impossible.
- **LeetCode Equivalent:** [1883. Minimum Skips to Arrive at Meeting On Time](https://leetcode.com/problems/minimum-skips-to-arrive-at-meeting-on-time/) / [1870. Minimum Speed to Arrive on Time](https://leetcode.com/problems/minimum-speed-to-arrive-on-time/)
- **Approach:** Binary Search on speed in range $[1, 10^7]$.
- **Complexity:** $O(N \log(\text{MaxSpeed}))$ Time.

#### 2. Swim in Rising Water / Grid Flood Bottleneck
- **College/Drive:** IIT Roorkee / BITS Pilani 2024
- **Problem Statement:** You are given an $n \times n$ integer matrix `grid` where each elevation is distinct. You start at $(0, 0)$ and want to reach $(n - 1, n - 1)$. At time $t$, you can swim infinitely anywhere with elevation $\le t$. Return the least time until you can reach the bottom right.
- **LeetCode Equivalent:** [778. Swim in Rising Water](https://leetcode.com/problems/swim-in-rising-water/)
- **Approach:** Modified Dijkstra's with Min-Heap tracking maximum elevation along path, or Binary Search on answer + BFS.
- **Complexity:** $O(N^2 \log N)$ Time.

#### 3. Maximum Profit in Weighted Job Scheduling
- **College/Drive:** IIIT Hyderabad / NIT Trichy 2024
- **Problem Statement:** You have $n$ jobs, where every job is scheduled to be done from `startTime[i]` to `endTime[i]`, obtaining a profit of `profit[i]`. Find the maximum profit you can take such that no two jobs in the subset overlap.
- **LeetCode Equivalent:** [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)
- **Approach:** Sort jobs by end time. $dp[i] = \max(dp[i-1], \text{profit}[i] + dp[\text{prev}])$ where `prev` is found via `std::upper_bound`.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 4. Custom Matrix Sorting by Row Frequencies
- **College/Drive:** On-Campus Drive 2024
- **Problem Statement:** Given an $M \times N$ matrix, sort each row based on frequency of distinct numbers, and rearrange entire columns to minimize adjacent difference penalties.
- **Approach:** HashMap frequency tracking combined with custom matrix row/column comparators.
- **Complexity:** $O(M \times N \log N)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Maximum Path Quality of a Graph
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** There is an undirected graph with $n$ nodes where each node has a value. Return the maximum quality of a valid path that starts and ends at node 0 and takes at most `maxTime` seconds.
- **LeetCode Equivalent:** [2065. Maximum Path Quality of a Graph](https://leetcode.com/problems/maximum-path-quality-of-a-graph/)
- **Approach:** Backtracking / DFS: Constraints on `maxTime` ($\le 100$) and node degree ensure recursion tree depth is small.
- **Complexity:** $O(4^{10})$ bounded search.

#### 6. Shortest Path with Alternating Colors
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Find shortest path from node 0 to all other nodes where edge colors alternate between RED and BLUE.
- **LeetCode Equivalent:** [1129. Shortest Path with Alternating Colors](https://leetcode.com/problems/shortest-path-with-alternating-colors/)
- **Approach:** BFS with state `(node, last_edge_color)`.
- **Complexity:** $O(V + E)$ Time.

#### 7. Split Array Largest Sum
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Partition array into $k$ non-empty subarrays minimizing the maximum subarray sum.
- **LeetCode Equivalent:** [410. Split Array Largest Sum](https://leetcode.com/problems/split-array-largest-sum/)
- **Complexity:** $O(N \log(\sum A))$ Time.

#### 8. Maximum Points You Can Obtain from Cards
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Pick $k$ cards from ends to maximize score.
- **LeetCode Equivalent:** [1423. Maximum Points You Can Obtain from Cards](https://leetcode.com/problems/maximum-points-you-can-obtain-from-cards/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.
