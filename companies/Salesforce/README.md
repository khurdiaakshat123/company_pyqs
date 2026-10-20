# Salesforce Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) ☁️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  - 2 to 3 Algorithmic Coding Problems (LeetCode Medium to Hard).
  - (In select campus drives) 10 to 15 Core CS MCQs (OOPs concepts, Database Queries, Operating Systems, Algorithm Time Complexities).
- **Passing Benchmark:** Solving both coding problems with 100% test-case clearance is standard for an interview callback.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Dynamic Programming:** State DP, 0/1 Knapsack variants, longest valid palindromic subsequence, subarray sum with deletions.
- **Graph & Grid Traversals:** Multi-source BFS, shortest path with fuel/transfer limits (Dijkstra), topological sorting for workflow dependencies.
- **Trees & Binary Search Trees:** Lowest Common Ancestor (LCA), tree diameter, serialize/deserialize binary tree.
- **Prefix Sums & Sliding Window:** Subarray sums, maximum frequency in window, minimum window substring.
- **System & OOP MCQs:** Java Garbage Collection, OOP design principles (SOLID), database indexing, isolation levels.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Cloud Server Network Latency (Dijkstra Variant)
- **College/Drive:** IIT Roorkee / BITS Pilani 2024
- **Problem Summary:** A multi-tenant cloud network connects $N$ regional data centers via weighted fiber links. One data center acts as the primary synchronization origin. Calculate the time it takes for all nodes to receive a broadcast update, or return -1 if any node is unreachable.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's algorithm using Min-Heap (`std::priority_queue`). Return maximum shortest distance from source.
- **Complexity:** $O((V + E) \log V)$ Time, $O(V + E)$ Space.

#### 2. Maximum Subarray Sum with One Deletion
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Summary:** Given an array of integers, return the maximum sum for a non-empty subarray with at most one element deletion.
- **LeetCode Equivalent:** [1186. Maximum Subarray Sum with One Deletion](https://leetcode.com/problems/maximum-subarray-sum-with-one-deletion/)
- **Approach:** Dynamic Programming with two states:
  - `no_del`: maximum subarray sum ending at index $i$ without any deletion.
  - `one_del`: maximum subarray sum ending at index $i$ with exactly one deletion.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. Tree Diameter / Longest Server Communication Path
- **College/Drive:** IIIT Allahabad / NSUT 2024
- **Problem Summary:** Given a tree with $N$ vertices, find the length of the longest path between any two vertices in the tree.
- **LeetCode Equivalent:** [543. Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/)
- **Approach:** Post-order DFS returning height, updating `max_diameter = max(max_diameter, left_height + right_height)`.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 4. Minimum Window Substring / Log Message Filter
- **College/Drive:** Salesforce Futureforce Campus Drive 2024
- **Problem Summary:** Given two strings `s` and `t`, return the minimum window substring of `s` such that every character in `t` (including duplicates) is included in the window.
- **LeetCode Equivalent:** [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- **Approach:** Two pointers / Sliding window with character frequency count tracking.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 5. Course Schedule II (Workflow Dependency Ordering)
- **College/Drive:** Campus Hiring 2024
- **Problem Summary:** Given $N$ automated CRM workflows and prerequisites, return the execution order to finish all workflows, or empty array if impossible.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm for Topological Sort using indegree array and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Longest Palindromic Subsequence
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Find length of longest palindromic subsequence in a string.
- **LeetCode Equivalent:** [516. Longest Palindromic Subsequence](https://leetcode.com/problems/longest-palindromic-subsequence/)
- **Approach:** 2D DP table: `dp[i][j] = dp[i+1][j-1] + 2` if `s[i] == s[j]`.
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

#### 7. Lowest Common Ancestor in Binary Tree
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Find lowest common ancestor node of two given nodes in a binary tree.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 8. Word Break
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Determine if string `s` can be segmented into a space-separated sequence of dictionary words.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Approach:** 1D DP array with Hash Set dictionary lookup.
- **Complexity:** $O(N^2 \cdot L)$ Time.

#### 9. Coin Change 2 (Number of Combinations)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Return number of combinations that make up given amount from coin denominations.
- **LeetCode Equivalent:** [518. Coin Change 2](https://leetcode.com/problems/coin-change-2/)
- **Approach:** Unbounded Knapsack DP: iterate coins on outer loop, amount on inner loop.
- **Complexity:** $O(N \times \text{amount})$ Time, $O(\text{amount})$ Space.

#### 10. Rotting Oranges / Multi-Source Infection
- **College/Drive:** Campus Slot 3 (2023)
- **Problem Summary:** Compute minimum time required for all fresh elements to spoil in a 2D matrix.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

---

## 🧠 Frequent Technical & Java MCQs Asked in Salesforce OA
1. **Database Isolation Levels:**
   - What anomaly is prevented by the `SERIALIZABLE` isolation level that `REPEATABLE READ` does not prevent?
   - *Answer:* Phantom Reads (where a concurrent transaction inserts new rows matching a `WHERE` range query).
2. **Java Garbage Collection:**
   - What is the difference between Minor GC and Major GC (Full GC)?
   - *Answer:* Minor GC collects garbage only from the Young Generation (Eden and Survivor spaces). Major GC sweeps the Old (Tenured) Generation, causing longer "Stop-The-World" pauses.
3. **Polymorphism & Late Binding:**
   - Which method calls cannot be dynamically bound at runtime in Java?
   - *Answer:* `static`, `private`, and `final` methods (they are resolved at compile time via static binding).
