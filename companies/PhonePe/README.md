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
- **Binary Search on Answer Space:** Minimum speed, delivery thresholds, capacity limits, split array largest sum.
- **Grid Traversal & Shortest Path with Barriers:** Swim in rising water, 0-1 BFS, alternating edge colors.
- **Advanced Dynamic Programming:** Job scheduling with binary search, knapsack with non-standard weights, path quality.
- **Trees & Lowest Common Ancestor:** Heavy-Light decomposition, tree path queries, diameter.
- **Sliding Window & Two Pointers:** Subarray sum equals K, card points max score, longest substring without repeats.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Minimum Speed to Arrive on Time / Fast Payment Routing
- **College/Drive:** IIT Bombay / IIT Delhi 2024–2025
- **Problem Summary:** You are given a floating point number `hour` representing the amount of time you have to reach the office, and an integer array `dist` where `dist[i]` is the distance of the $i$-th train ride. Each ride takes $\lceil \text{dist}[i] / \text{speed} \rceil$ hours (except the last which is fractional). Return the minimum positive integer speed that all trains must travel at, or -1 if impossible.
- **Constraints:** $1 \le dist.length \le 10^5$, $1 \le dist[i] \le 10^5$, $1 \le hour \le 10^9$.
- **LeetCode Equivalent:** [1870. Minimum Speed to Arrive on Time](https://leetcode.com/problems/minimum-speed-to-arrive-on-time/)
- **Approach:** Binary Search on speed in range $[1, 10^7]$.
- **Complexity:** $O(N \log(\text{MaxSpeed}))$ Time.

#### 2. Swim in Rising Water / Grid Flood Bottleneck
- **College/Drive:** IIT Roorkee / BITS Pilani 2024–2025
- **Problem Summary:** You are given an $n \times n$ integer matrix `grid` where each elevation is distinct. You start at $(0, 0)$ and want to reach $(n - 1, n - 1)$. At time $t$, you can swim infinitely anywhere with elevation $\le t$. Return the least time until you can reach the bottom right.
- **Constraints:** $1 \le n \le 50$, $0 \le grid[i][j] < n^2$.
- **LeetCode Equivalent:** [778. Swim in Rising Water](https://leetcode.com/problems/swim-in-rising-water/)
- **Approach:** Modified Dijkstra's with Min-Heap tracking maximum elevation along path, or Binary Search on answer + BFS.
- **Complexity:** $O(N^2 \log N)$ Time.

#### 3. Maximum Profit in Weighted Job Scheduling
- **College/Drive:** IIIT Hyderabad / NIT Trichy 2024–2025
- **Problem Summary:** You have $n$ jobs, where every job is scheduled to be done from `startTime[i]` to `endTime[i]`, obtaining a profit of `profit[i]`. Find the maximum profit you can take such that no two jobs in the subset overlap.
- **Constraints:** $1 \le n \le 5 \times 10^4$.
- **LeetCode Equivalent:** [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)
- **Approach:** Sort jobs by end time. $dp[i] = \max(dp[i-1], \text{profit}[i] + dp[\text{prev}])$ where `prev` is found via `std::upper_bound`.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 4. Custom Matrix Sorting by Row Frequencies
- **College/Drive:** On-Campus Drive 2024–2025
- **Problem Summary:** Given an $M \times N$ matrix, sort each row based on frequency of distinct numbers, and rearrange entire columns to minimize adjacent difference penalties.
- **Constraints:** $1 \le M, N \le 500$.
- **Approach:** HashMap frequency tracking combined with custom matrix row/column comparators.
- **Complexity:** $O(M \times N \log N)$ Time.

#### 5. Maximum Path Quality of a Graph
- **College/Drive:** Campus Drive Slot 1 (2024–2025)
- **Problem Summary:** There is an undirected graph with $n$ nodes where each node has a value. Return the maximum quality of a valid path that starts and ends at node 0 and takes at most `maxTime` seconds.
- **Constraints:** $n \le 100$, $10 \le maxTime \le 100$, max node degree $\le 4$.
- **LeetCode Equivalent:** [2065. Maximum Path Quality of a Graph](https://leetcode.com/problems/maximum-path-quality-of-a-graph/)
- **Approach:** Backtracking / DFS: Constraints on `maxTime` ($\le 100$) and node degree ensure recursion tree depth is small.
- **Complexity:** $O(4^{10})$ bounded search.

#### 6. Shortest Path with Alternating Colors
- **College/Drive:** Campus Drive Slot 2 (2024)
- **Problem Summary:** Find shortest path from node 0 to all other nodes where edge colors alternate between RED and BLUE.
- **Constraints:** $1 \le n \le 100$.
- **LeetCode Equivalent:** [1129. Shortest Path with Alternating Colors](https://leetcode.com/problems/shortest-path-with-alternating-colors/)
- **Approach:** BFS with state `(node, last_edge_color)`.
- **Complexity:** $O(V + E)$ Time.

#### 7. Split Array Largest Sum
- **College/Drive:** Off-Campus Drive 2024
- **Problem Summary:** Partition array into $k$ non-empty subarrays minimizing the maximum subarray sum.
- **Constraints:** $1 \le nums.length \le 1000$, $1 \le k \le \min(50, nums.length)$.
- **LeetCode Equivalent:** [410. Split Array Largest Sum](https://leetcode.com/problems/split-array-largest-sum/)
- **Approach:** Binary search on answer $[\max(A), \sum A]$ with greedy verification.
- **Complexity:** $O(N \log(\sum A))$ Time.

#### 8. Maximum Points You Can Obtain from Cards
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Pick $k$ cards from ends to maximize score.
- **Constraints:** $1 \le cardPoints.length \le 10^5$, $1 \le k \le cardPoints.length$.
- **LeetCode Equivalent:** [1423. Maximum Points You Can Obtain from Cards](https://leetcode.com/problems/maximum-points-you-can-obtain-from-cards/)
- **Approach:** Sliding window of size $N - k$ minimizing sum of non-selected elements.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Rotting Oranges / Payment Failure Contagion
- **College/Drive:** PhonePe Bangalore Drive 2024
- **Problem Summary:** Minimum minutes to spread infection across entire 2D matrix.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 10. Course Schedule II (Topological Sort)
- **College/Drive:** Campus Slot 2024
- **Problem Summary:** Order tasks given prerequisites.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm using indegrees and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Trapping Rain Water
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Network Delay Time / Payment Gateway Hub
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Calculate time for all hubs to receive broadcast from central server.
- **Constraints:** $1 \le N \le 100$, $1 \le edges \le 6000$.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's algorithm with Min-Heap.
- **Complexity:** $O(E \log V)$ Time.

#### 13. Subarray Sum Equals K
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Count total continuous subarrays whose sum equals $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency counter.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 14. Coin Change (Fewest Coins)
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Minimum coins needed to make change.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 15. Merge Intervals
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Merge all overlapping execution intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time and merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

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

## 💡 PhonePe High-Difficulty OA Strategy
1. **Expect Non-Standard CP Stories:** PhonePe rarely asks vanilla LeetCode problems; questions are framed in lengthy real-world transaction routing or network topologies. Extract the underlying graph/DP model before writing code.
2. **Prioritize Binary Search on Answer:** When an optimization problem asks for "minimum maximum" or "minimum capacity/speed", check monotonic feasibility for Binary Search immediately.
3. **Handle Edge Cases Early:** Check for unreachable nodes (return -1), disconnected components, and floating-point rounding precision.
