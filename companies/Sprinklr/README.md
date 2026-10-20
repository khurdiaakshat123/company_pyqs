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
- **College/Drive:** IIT Roorkee / DTU Campus Hiring 2024
- **Problem Summary:** A restaurant receives $N$ orders, where order $i$ takes $T_i$ minutes to cook and must be delivered within $D_i$ minutes from start time. Cooking cannot be paused once started. Given arrival and departure times, find the minimum number of chefs required so that no order exceeds its deadline.
- **Approach:** Binary Search on the number of chefs $C \in [1, N]$. For a fixed $C$, use a Min-Heap of chef available times and check deadline feasibility greedily.
- **Complexity:** $O(N \log N \times \log N)$ Time.

#### 2. Social Media Influencer Graph (LCA with Dynamic Weight)
- **College/Drive:** IIT Kharagpur / BITS Pilani 2024
- **Problem Summary:** Given a tree of $N$ users where edge weights represent interaction strength. Process $Q$ queries: Given two users $U$ and $V$, find the maximum interaction bottleneck along the path between $U$ and $V$.
- **Approach:** Binary Lifting for Lowest Common Ancestor (LCA). Maintain `up[node][k]` (the $2^k$-th ancestor) and `max_edge[node][k]` (maximum edge weight on that jump).
- **Complexity:** Precomputation: $O(N \log N)$, Query: $O(\log N)$ Time.

#### 3. Longest Substring with At Least K Repeating Characters
- **College/Drive:** NSUT / IIIT Delhi 2024
- **Problem Summary:** Given a string $s$ and an integer $k$, return the length of the longest substring of $s$ such that the frequency of each character in this substring is greater than or equal to $k$.
- **LeetCode Equivalent:** [395. Longest Substring with At Least K Repeating Characters](https://leetcode.com/problems/longest-substring-with-at-least-k-repeating-characters/)
- **Approach:** Divide and Conquer or Sliding Window iterating over the number of unique characters from 1 to 26.
- **Complexity:** $O(26 \times N) = O(N)$ Time.

#### 4. Maximum Non-Overlapping Interval Weights with Cooldown
- **College/Drive:** IIT BHU / NIT Trichy 2024
- **Problem Summary:** Given $N$ ad campaigns with start time $S_i$, end time $E_i$, revenue $R_i$, and a mandatory cooldown period $C$ between consecutive campaigns. Find the maximum total revenue achievable.
- **Approach:** Dynamic programming with binary search: Sort intervals by end time; for each interval, find the latest interval ending $\le S_i - C$ via `std::upper_bound`.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 5. Split Array Largest Sum (Minimax Binary Search)
- **College/Drive:** Sprinklr On-Campus 2024
- **Problem Summary:** Given an array `nums` which consists of non-negative integers and an integer $k$, split the array into $k$ non-empty continuous subarrays such that the largest sum among any of them is minimized.
- **LeetCode Equivalent:** [410. Split Array Largest Sum](https://leetcode.com/problems/split-array-largest-sum/)
- **Approach:** Binary Search on answer space range $[\max(\text{nums}), \sum \text{nums}]$. Greedily count required sub-arrays for a mid value.
- **Complexity:** $O(N \log(\sum \text{nums}))$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Minimum Swaps to Make Sequences Strictly Increasing
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Given two integer arrays `nums1` and `nums2` of equal length, find minimum swaps at same indices to make both arrays strictly increasing.
- **LeetCode Equivalent:** [801. Minimum Swaps To Make Sequences Increasing](https://leetcode.com/problems/minimum-swaps-to-make-sequences-increasing/)
- **Approach:** 2-state DP: `keep[i]` and `swap[i]` maintaining transitions based on comparisons with index $i-1$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Minimum Window Substring with Multi-Condition Counters
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Find minimum length substring containing all target characters in frequency.
- **LeetCode Equivalent:** [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 8. Subtree Weight Queries (Euler Tour + Fenwick Tree)
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Update node value and query sum of all node values in a given subtree on a dynamic tree.
- **Approach:** Flatten tree into an array using Euler Tour (DFS entry and exit times); apply Fenwick Tree / Segment Tree for range sums.
- **Complexity:** $O(\log N)$ per update/query, $O(N)$ space.

#### 9. Shortest Path with Fuel Constraints (State Expansion BFS)
- **College/Drive:** Off-Campus Drive 2023
- **Problem Summary:** Shortest path on graph where vehicle has capacity $C$ and gas stations exist at select nodes.
- **Approach:** Dijkstra on expanded graph state `(node, fuel_remaining)`.
- **Complexity:** $O(C \cdot (V + E) \log(C \cdot V))$ Time.

#### 10. Distinct Subsequences II
- **College/Drive:** Campus Slot 3 (2023)
- **Problem Summary:** Given a string $s$, return the number of distinct non-empty subsequences of $s$ modulo $10^9+7$.
- **LeetCode Equivalent:** [940. Distinct Subsequences II](https://leetcode.com/problems/distinct-subsequences-ii/)
- **Approach:** DP with last occurrence array: `dp[i] = 2 * dp[i-1] - dp[last[s[i]] - 1]`.
- **Complexity:** $O(N)$ Time, $O(1)$ Auxiliary Space.

---

## 💡 Sprinklr OA Problem-Solving Strategy
1. **Deconstruct the Story:** Sprinklr problem statements often have 400–600 words of background story (e.g., social feed ranking, ad auctions). Strip away flavor text to isolate inputs, outputs, and constraints.
2. **Watch for Binary Search on Answer:** Whenever a problem asks for "minimize the maximum" or "maximize the minimum", test whether the predicate function is monotonic.
3. **Precompute LCA Ancestors:** Keep binary lifting templates ready for tree path queries.
