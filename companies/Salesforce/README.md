# Salesforce Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) ☁️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  - 2 to 3 Algorithmic Coding Problems (LeetCode Medium to Hard).
  - (In select campus drives) 10 to 15 Core CS MCQs (OOPs concepts, Database Queries, Operating Systems, Algorithm Time Complexities).
- **Passing Benchmark:** Solving both coding problems with 100% test-case clearance is standard for an interview callback.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Dynamic Programming | Medium - Hard | State DP, 0/1 Knapsack variants, longest valid palindromic subsequence |
| **Very High** | Graph & Grid Traversals | Medium - Hard | Multi-source BFS, shortest path with fuel/transfer limits, cycle detection |
| **High** | Trees & Binary Search Trees | Medium | Lowest Common Ancestor (LCA), tree diameter, serialize/deserialize |
| **High** | Prefix Sums & Sliding Window | Medium | Subarray sums, maximum frequency in window, balanced subsegments |
| **Medium** | System & OOP MCQs | Medium | Java Garbage Collection, OOP design principles (SOLID), database indexing |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Cloud Server Network Latency (Dijkstra Variant)
- **Problem Summary:** A multi-tenant cloud network connects $N$ regional data centers via weighted fiber links. One data center acts as the primary synchronization origin. Calculate the time it takes for all nodes to receive a broadcast update, or return -1 if any node is unreachable.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's algorithm using Min-Heap (`std::priority_queue`). Return maximum shortest distance from source.
- **Complexity:** $O((V + E) \log V)$ Time, $O(V + E)$ Space.

### 2. Maximum Subarray Sum with One Deletion
- **Problem Summary:** Given an array of integers, return the maximum sum for a non-empty subarray with at most one element deletion.
- **LeetCode Equivalent:** [1186. Maximum Subarray Sum with One Deletion](https://leetcode.com/problems/maximum-subarray-sum-with-one-deletion/)
- **Approach:** Dynamic Programming with two states:
  - `no_del`: maximum subarray sum ending at index $i$ without any deletion.
  - `one_del`: maximum subarray sum ending at index $i$ with exactly one deletion.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 3. Tree Diameter / Longest Server Communication Path
- **Problem Summary:** Given a tree with $N$ vertices, find the length of the longest path between any two vertices in the tree.
- **LeetCode Equivalent:** [543. Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/)
- **Approach:** Post-order DFS returning height, updating `max_diameter = max(max_diameter, left_height + right_height)`.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

### 4. Minimum Window Substring / Log Message Filter
- **Problem Summary:** Given two strings `s` and `t`, return the minimum window substring of `s` such that every character in `t` (including duplicates) is included in the window.
- **LeetCode Equivalent:** [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- **Approach:** Two pointers / Sliding window with character frequency count tracking.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.
