# Sprinklr Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🦄

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **Mettl**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  - **3 Algorithmic Coding Questions** (Ranging from Medium to LeetCode Hard / Competitive Programming Div. 2 C/D/E level).
  - No MCQs, pure coding test with high problem statement complexity.
- **Evaluation Criteria:**
  - Sprinklr offers premier compensation packages (30+ LPA for SDE-1).
  - Problem statements are notoriously lengthy and disguised as complex business, social media, or gaming scenarios.
  - Partial marks are awarded for subtask test cases, but passing $\ge 2$ questions completely is usually mandatory for shortlisting.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Trees & Lowest Common Ancestor:** LCA with binary lifting, tree path queries, Tree DP, Euler tour techniques.
- **Binary Search on Answer Space:** Resource allocation, maximum minimum distance, chef/task scheduling, split array largest sum.
- **Graph Algorithms (BFS/DFS/Flow):** Network flow variations, shortest path with state expansion, topological DAG.
- **Advanced Sliding Window & Sets:** Ordered sets (`std::set`), multi-condition window substrings, at least $K$ repeating characters.
- **Dynamic Programming:** Digit DP, bitmask DP, non-overlapping interval scheduling with cooldown.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Restaurant Kitchen Chef Allocation (Binary Search on Answer)
- **College/Drive:** IIT Roorkee / DTU Campus Hiring 2024–2025
- **Problem Summary:** A restaurant receives $N$ orders, where order $i$ takes $T_i$ minutes to cook and must be delivered within $D_i$ minutes from start time. Cooking cannot be paused once started. Given arrival and departure times, find the minimum number of chefs required so that no order exceeds its deadline.
- **Constraints:** $1 \le N \le 10^5$.
- **Approach:** Binary Search on the number of chefs $C \in [1, N]$. For a fixed $C$, use a Min-Heap of chef available times and check deadline feasibility greedily.
- **Complexity:** $O(N \log N \times \log N)$ Time.

#### 2. Social Media Influencer Graph (LCA with Dynamic Weight)
- **College/Drive:** IIT Kharagpur / BITS Pilani 2024–2025
- **Problem Summary:** Given a tree of $N$ users where edge weights represent interaction strength. Process $Q$ queries: Given two users $U$ and $V$, find the maximum interaction bottleneck along the path between $U$ and $V$.
- **Constraints:** $1 \le N, Q \le 10^5$.
- **Approach:** Binary Lifting for Lowest Common Ancestor (LCA). Maintain `up[node][k]` (the $2^k$-th ancestor) and `max_edge[node][k]` (maximum edge weight on that jump).
- **Complexity:** Precomputation: $O(N \log N)$, Query: $O(\log N)$ Time.

#### 3. Longest Substring with At Least K Repeating Characters
- **College/Drive:** NSUT / IIIT Delhi 2024–2025
- **Problem Summary:** Given a string $s$ and an integer $k$, return the length of the longest substring of $s$ such that the frequency of each character in this substring is greater than or equal to $k$.
- **Constraints:** $1 \le s.length \le 10^4$, $1 \le k \le 10^5$.
- **LeetCode Equivalent:** [395. Longest Substring with At Least K Repeating Characters](https://leetcode.com/problems/longest-substring-with-at-least-k-repeating-characters/)
- **Approach:** Divide and Conquer or Sliding Window iterating over the number of unique characters from 1 to 26.
- **Complexity:** $O(26 \times N) = O(N)$ Time.

#### 4. Maximum Non-Overlapping Interval Weights with Cooldown
- **College/Drive:** IIT BHU / NIT Trichy 2024–2025
- **Problem Summary:** Given $N$ ad campaigns with start time $S_i$, end time $E_i$, revenue $R_i$, and a mandatory cooldown period $C$ between consecutive campaigns. Find the maximum total revenue achievable.
- **Constraints:** $1 \le N \le 5 \times 10^4$.
- **Approach:** Dynamic programming with binary search: Sort intervals by end time; for each interval, find the latest interval ending $\le S_i - C$ via `std::upper_bound`.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 5. Split Array Largest Sum (Minimax Binary Search)
- **College/Drive:** Sprinklr On-Campus 2024–2025
- **Problem Summary:** Given an array `nums` which consists of non-negative integers and an integer $k$, split the array into $k$ non-empty continuous subarrays such that the largest sum among any of them is minimized.
- **Constraints:** $1 \le nums.length \le 1000$, $1 \le k \le \min(50, nums.length)$.
- **LeetCode Equivalent:** [410. Split Array Largest Sum](https://leetcode.com/problems/split-array-largest-sum/)
- **Approach:** Binary Search on answer space range $[\max(\text{nums}), \sum \text{nums}]$. Greedily count required sub-arrays for a mid value.
- **Complexity:** $O(N \log(\sum \text{nums}))$ Time, $O(1)$ Space.

#### 6. Minimum Swaps to Make Sequences Strictly Increasing
- **College/Drive:** Campus Slot 1 (2024)
- **Problem Summary:** Given two integer arrays `nums1` and `nums2` of equal length, find minimum swaps at same indices to make both arrays strictly increasing.
- **Constraints:** $2 \le nums1.length \le 10^5$.
- **LeetCode Equivalent:** [801. Minimum Swaps To Make Sequences Increasing](https://leetcode.com/problems/minimum-swaps-to-make-sequences-increasing/)
- **Approach:** 2-state DP: `keep[i]` and `swap[i]` maintaining transitions based on comparisons with index $i-1$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Minimum Window Substring with Multi-Condition Counters
- **College/Drive:** Campus Slot 2 (2024)
- **Problem Summary:** Find minimum length substring containing all target characters in frequency.
- **Constraints:** $1 \le |s|, |t| \le 10^5$.
- **LeetCode Equivalent:** [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 8. Subtree Weight Queries (Euler Tour + Fenwick Tree)
- **College/Drive:** Campus Hiring 2024
- **Problem Summary:** Update node value and query sum of all node values in a given subtree on a dynamic tree.
- **Constraints:** $1 \le N, Q \le 10^5$.
- **Approach:** Flatten tree into an array using Euler Tour (DFS entry and exit times); apply Fenwick Tree / Segment Tree for range sums.
- **Complexity:** $O(\log N)$ per update/query, $O(N)$ space.

#### 9. Shortest Path with Fuel Constraints (State Expansion BFS)
- **College/Drive:** Off-Campus Drive 2024
- **Problem Summary:** Shortest path on graph where vehicle has capacity $C$ and gas stations exist at select nodes.
- **Constraints:** $V \le 1000, C \le 100$.
- **Approach:** Dijkstra on expanded graph state `(node, fuel_remaining)`.
- **Complexity:** $O(C \cdot (V + E) \log(C \cdot V))$ Time.

#### 10. Distinct Subsequences II
- **College/Drive:** Campus Slot 3 (2024)
- **Problem Summary:** Given a string $s$, return the number of distinct non-empty subsequences of $s$ modulo $10^9+7$.
- **Constraints:** $1 \le s.length \le 2000$.
- **LeetCode Equivalent:** [940. Distinct Subsequences II](https://leetcode.com/problems/distinct-subsequences-ii/)
- **Approach:** DP with last occurrence array: `dp[i] = 2 * dp[i-1] - dp[last[s[i]] - 1]`.
- **Complexity:** $O(N)$ Time, $O(1)$ Auxiliary Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Trapping Rain Water
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Network Delay Time / Influence Propagation
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Calculate time for all social nodes to receive notification from origin.
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

#### 14. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Minimum minutes to spread contagion across entire grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 15. Daily Temperatures / Metric Spike Monotonic Stack
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Find days to wait for a higher value.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 16. Coin Change (Fewest Coins)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Minimum coins needed to make change.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 17. Merge Intervals
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Merge all overlapping intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time and merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 18. Product of Array Except Self without Division
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 19. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Sliding window with hash map storing last seen indices.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

#### 20. House Robber (1D Dynamic Programming)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Maximize stolen value without robbing two adjacent houses.
- **Constraints:** $1 \le nums.length \le 100$.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** DP: `dp[i] = max(dp[i-1], dp[i-2] + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 💡 Sprinklr OA Problem-Solving Strategy
1. **Deconstruct the Story:** Sprinklr problem statements often have 400–600 words of background story (e.g., social feed ranking, ad auctions). Strip away flavor text to isolate inputs, outputs, and constraints.
2. **Watch for Binary Search on Answer:** Whenever a problem asks for "minimize the maximum" or "maximize the minimum", test whether the predicate function is monotonic.
3. **Precompute LCA Ancestors:** Keep binary lifting templates ready for tree path queries.
