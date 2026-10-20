# Sprinklr Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🦄

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **Mettl**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  - **3 Algorithmic Coding Questions** (Ranging from Medium to LeetCode Hard / Competitive Programming Div. 2 level).
  - No MCQs, pure coding test with high problem statement complexity.
- **Evaluation Criteria:**
  - Sprinklr offers premier compensation packages (30+ LPA for SDE-1).
  - Problem statements are notoriously lengthy and disguised as complex business, social media, or gaming scenarios.
  - Partial marks are awarded for subtask test cases, but passing $\ge 2$ questions completely is usually mandatory for shortlisting.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Trees & Lowest Common Ancestor | Hard | LCA with binary lifting, tree path queries, Tree DP, centroid decomposition |
| **Very High** | Binary Search on Answer Space | Medium - Hard | Resource allocation, maximum minimum distance, chef/task scheduling |
| **High** | Graph Algorithms (BFS/DFS/Flow) | Hard | Network flow variations, shortest path with state expansion, topological DAG |
| **High** | Advanced Sliding Window & Sets | Medium - Hard | Ordered sets (`std::set`), multi-condition window substrings |
| **Medium** | Dynamic Programming | Hard | Digit DP, bitmask DP, grid path optimization with penalties |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Restaurant Kitchen Chef Allocation (Binary Search on Answer)
- **Problem Summary:** A restaurant receives $N$ orders, where order $i$ takes $T_i$ minutes to cook and must be delivered within $D_i$ minutes from start time. Cooking cannot be paused once started. Given arrival and departure times, find the minimum number of chefs required so that no order exceeds its deadline.
- **Approach:** Binary Search on the number of chefs $C \in [1, N]$. For a fixed $C$, use a Min-Heap of chef available times and check deadline feasibility greedily.
- **Complexity:** $O(N \log N \times \log N)$ Time.

### 2. Social Media Influencer Graph (LCA with Dynamic Weight)
- **Problem Summary:** Given a tree of $N$ users where edge weights represent interaction strength. Process $Q$ queries: Given two users $U$ and $V$, find the maximum interaction bottleneck along the path between $U$ and $V$.
- **Approach:** Binary Lifting for Lowest Common Ancestor (LCA). Maintain `up[node][k]` (the $2^k$-th ancestor) and `max_edge[node][k]` (maximum edge weight on that jump).
- **Complexity:** Precomputation: $O(N \log N)$, Query: $O(\log N)$ Time.

### 3. Longest Substring with At Least K Repeating Characters
- **Problem Summary:** Given a string $s$ and an integer $k$, return the length of the longest substring of $s$ such that the frequency of each character in this substring is greater than or equal to $k$.
- **LeetCode Equivalent:** [395. Longest Substring with At Least K Repeating Characters](https://leetcode.com/problems/longest-substring-with-at-least-k-repeating-characters/)
- **Approach:** Divide and Conquer or Sliding Window iterating over the number of unique characters from 1 to 26.
- **Complexity:** $O(26 \times N) = O(N)$ Time.

### 4. Maximum Non-Overlapping Interval Weights with Cooldown
- **Problem Summary:** Given $N$ ad campaigns with start time $S_i$, end time $E_i$, revenue $R_i$, and an mandatory cooldown period $C$ between consecutive campaigns. Find the maximum total revenue achievable.
- **Approach:** Dynamic programming with binary search: Sort intervals by end time; for each interval, find the latest interval ending $\le S_i - C$ via `std::upper_bound`.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.
