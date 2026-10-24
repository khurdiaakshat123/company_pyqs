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
- **Dynamic Programming:** State DP, 0/1 Knapsack variants, longest valid palindromic subsequence, subarray sum with deletions, Tree DP.
- **Graph & Grid Traversals:** Multi-source BFS, shortest path with fuel/transfer limits (Dijkstra), topological sorting for workflow dependencies, Alien dictionary.
- **Trees & Binary Search Trees:** Lowest Common Ancestor (LCA), tree diameter, serialize/deserialize binary tree, house robber on trees.
- **Prefix Sums & Sliding Window:** Subarray sums divisible by K, monotonic queue sliding window maximum, minimum window substring.
- **System & OOP MCQs:** Java Garbage Collection, OOP design principles (SOLID), database indexing, isolation levels, transaction rollbacks.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Cloud Server Network Latency (Dijkstra Variant)
- **College/Drive:** IIT Roorkee / BITS Pilani 2024–2025
- **Problem Summary:** A multi-tenant cloud network connects $N$ regional data centers via weighted fiber links. One data center acts as the primary synchronization origin. Calculate the time it takes for all nodes to receive a broadcast update, or return -1 if any node is unreachable.
- **Constraints:** $1 \le N \le 100$, $1 \le \text{edges.length} \le 6000$, edge weight $\ge 0$.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's algorithm using Min-Heap (`std::priority_queue`). Return maximum shortest distance from source among all $N$ nodes.
- **Complexity:** $O((V + E) \log V)$ Time, $O(V + E)$ Space.

#### 2. Maximum Subarray Sum with One Deletion
- **College/Drive:** NIT Trichy / DTU 2024–2025
- **Problem Summary:** Given an array of integers, return the maximum sum for a non-empty subarray with at most one element deletion.
- **Constraints:** $1 \le \text{arr.length} \le 10^5$, $-10^4 \le \text{arr}[i] \le 10^4$.
- **LeetCode Equivalent:** [1186. Maximum Subarray Sum with One Deletion](https://leetcode.com/problems/maximum-subarray-sum-with-one-deletion/)
- **Approach:** Dynamic Programming with two state variables:
  - `no_del`: maximum subarray sum ending at index $i$ without any deletion.
  - `one_del`: maximum subarray sum ending at index $i$ with exactly one deletion (`max(prev_no_del, prev_one_del + x)`).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. Tree Diameter / Longest Server Communication Path
- **College/Drive:** IIIT Allahabad / NSUT 2024–2025
- **Problem Summary:** Given a tree with $N$ vertices, find the length of the longest path between any two vertices in the tree.
- **Constraints:** Number of nodes $\le 10^5$.
- **LeetCode Equivalent:** [543. Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/)
- **Approach:** Post-order DFS returning subtree height, updating `max_diameter = max(max_diameter, left_height + right_height)`.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 4. Minimum Window Substring / Log Message Filter
- **College/Drive:** Salesforce Futureforce Campus Drive 2024–2025
- **Problem Summary:** Given two strings `s` and `t`, return the minimum window substring of `s` such that every character in `t` (including duplicates) is included in the window.
- **Constraints:** $1 \le |s|, |t| \le 10^5$.
- **LeetCode Equivalent:** [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- **Approach:** Two pointers / Sliding window with character frequency count tracking and `required_chars` counter.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 5. Course Schedule II (Workflow Dependency Ordering)
- **College/Drive:** Campus Hiring 2024–2025
- **Problem Summary:** Given $N$ automated CRM workflows and prerequisites, return the execution order to finish all workflows, or empty array if impossible.
- **Constraints:** $1 \le \text{numCourses} \le 2000$, $0 \le \text{prerequisites.length} \le \text{numCourses} \times (\text{numCourses} - 1)$.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm for Topological Sort using indegree array and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 6. Daily Temperatures / Metric Alert Monotonic Stack
- **College/Drive:** Salesforce Bangalore Hiring Drive 2024
- **Problem Summary:** Given an array of integers `temperatures` representing daily temperatures, return an array `answer` such that `answer[i]` is the number of days you have to wait after the $i$-th day to get a warmer temperature.
- **Constraints:** $1 \le temperatures.length \le 10^5$, $30 \le temperatures[i] \le 100$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic decreasing stack storing indices. Pop elements smaller than current temperature and compute distance `i - prev_idx`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Subarray Sums Divisible by K
- **College/Drive:** IIT BHU / NIT Surathkal 2024
- **Problem Summary:** Given an integer array `nums` and an integer `k`, return the number of non-empty subarrays that have a sum divisible by `k`.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$, $-10^4 \le nums[i] \le 10^4$, $2 \le k \le 10^4$.
- **LeetCode Equivalent:** [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- **Approach:** Hash map tracking frequencies of prefix sum modulo $k$ (normalized to non-negative: `((sum % k) + k) % k`). Add current remainder count to total before incrementing.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 8. Alien Dictionary (Workflow Rule Precedence)
- **College/Drive:** Salesforce India Off-Campus 2024
- **Problem Summary:** Given a sorted dictionary of an alien language, derive the alphabetical order of characters. If invalid/cyclic, return `""`.
- **Constraints:** $1 \le words.length \le 100$, $1 \le words[i].length \le 100$.
- **LeetCode Equivalent:** [269. Alien Dictionary](https://leetcode.com/problems/alien-dictionary/)
- **Approach:** Compare adjacent words to deduce directed character edges. Detect prefix anomaly (longer word preceding shorter prefix). Apply Kahn's Algorithm or DFS cycle detection.
- **Complexity:** $O(C)$ Time where $C$ is total character count; $O(1)$ Space since alphabet size $\le 26$.

#### 9. Sliding Window Maximum / Cloud Burst Metric Monitor
- **College/Drive:** Salesforce University Hiring 2024
- **Problem Summary:** Given an array `nums` and a sliding window size `k`, find the maximum element in each sliding window moving from left to right.
- **Constraints:** $1 \le nums.length \le 10^5$, $1 \le k \le nums.length$.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Approach:** Monotonic Decreasing Double-Ended Queue (`std::deque`). Store indices, maintain elements in strictly decreasing order, evict out-of-window indices from the front.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 10. House Robber III (Tree Independent Set)
- **College/Drive:** Futureforce Internship 2024
- **Problem Summary:** A cloud resource cluster is structured as a binary tree. Two directly connected nodes cannot be simultaneously scheduled for maintenance. Find the maximum weight of maintenance jobs scheduled.
- **Constraints:** Number of nodes $\le 10^4$, node values $\le 10^4$.
- **LeetCode Equivalent:** [337. House Robber III](https://leetcode.com/problems/house-robber-iii/)
- **Approach:** Post-order Tree DP returning a pair `(rob, not_rob)`. `rob = node.val + left.not_rob + right.not_rob`; `not_rob = max(left.rob, left.not_rob) + max(right.rob, right.not_rob)`.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Design In-Memory File System
- **College/Drive:** Salesforce Senior SWE & Campus Slot 1 (2023–2024)
- **Problem Summary:** Design a data structure that simulates an in-memory file system with `ls`, `mkdir`, `addContentToFile`, and `readContentFromFile`.
- **Constraints:** Path length $\le 100$, up to 300 calls.
- **LeetCode Equivalent:** [588. Design In-Memory File System](https://leetcode.com/problems/design-in-memory-file-system/)
- **Approach:** Trie-like hierarchical directory structure where each node represents a directory or file with a map of child nodes and a string content buffer.
- **Complexity:** $O(L)$ Time per operation where $L$ is path length.

#### 12. Meeting Rooms II / Server Scheduling Optimization
- **College/Drive:** Campus Drive 2023–2024
- **Problem Summary:** Given an array of meeting time intervals `[start, end]`, find the minimum number of conference rooms (or server instances) required.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- **Approach:** Sort start times and end times separately, or sort intervals by start time and maintain a Min-Heap of end times.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 13. Partition Equal Subset Sum
- **College/Drive:** BITS Pilani / NIT Warangal 2023
- **Problem Summary:** Given an integer array `nums`, return `true` if you can partition the array into two subsets such that the sum of the elements in both subsets is equal.
- **Constraints:** $1 \le nums.length \le 200$, $1 \le nums[i] \le 100$.
- **LeetCode Equivalent:** [416. Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum/)
- **Approach:** 0/1 Knapsack DP targeting `target = total_sum / 2`. If total sum is odd, return false immediately. Use 1D boolean DP array traversed backwards.
- **Complexity:** $O(N \times \text{target})$ Time, $O(\text{target})$ Space.

#### 14. Reorganize String / Task Scheduler without Clashing
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Given a string $s$, rearrange characters so that no two adjacent characters are identical. Return `""` if impossible.
- **Constraints:** $1 \le s.length \le 500$.
- **LeetCode Equivalent:** [767. Reorganize String](https://leetcode.com/problems/reorganize-string/)
- **Approach:** Max-Heap of character frequencies. Greedily place the most frequent character, then second most frequent character to prevent adjacency collisions.
- **Complexity:** $O(N \log \Sigma)$ Time, $O(\Sigma)$ Space where $\Sigma = 26$.

#### 15. Shortest Path in Binary Matrix (8-Directional Grid)
- **College/Drive:** Salesforce SWE Screening 2023
- **Problem Summary:** Given an $N \times N$ binary matrix `grid`, return the length of the shortest clear path from top-left $(0, 0)$ to bottom-right $(N-1, N-1)$ moving in 8 directions.
- **Constraints:** $1 \le N \le 100$.
- **LeetCode Equivalent:** [1091. Shortest Path in Binary Matrix](https://leetcode.com/problems/shortest-path-in-binary-matrix/)
- **Approach:** Breadth-First Search (BFS) starting at $(0, 0)$ exploring all 8 neighboring coordinates with distance layers.
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

#### 16. Longest Palindromic Subsequence
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Find length of longest palindromic subsequence in a string.
- **Constraints:** $1 \le s.length \le 1000$.
- **LeetCode Equivalent:** [516. Longest Palindromic Subsequence](https://leetcode.com/problems/longest-palindromic-subsequence/)
- **Approach:** 2D DP table: `dp[i][j] = dp[i+1][j-1] + 2` if `s[i] == s[j]`.
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

#### 17. Lowest Common Ancestor in Binary Tree
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Find lowest common ancestor node of two given nodes in a binary tree.
- **Constraints:** Number of nodes $\le 10^5$.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Approach:** Recursive post-order traversal: if current node matches $p$ or $q$, return current node. If both left and right return non-null, root is LCA.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 18. Word Break
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Determine if string `s` can be segmented into a space-separated sequence of dictionary words.
- **Constraints:** $1 \le s.length \le 300$, $1 \le wordDict.length \le 1000$.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Approach:** 1D DP array with Hash Set dictionary lookup: `dp[i]` is true if any `dp[j]` is true and `s[j...i]` is in dictionary.
- **Complexity:** $O(N^2 \cdot L)$ Time where $L$ is max word length.

#### 19. Coin Change 2 (Number of Combinations)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Return number of combinations that make up given amount from coin denominations.
- **Constraints:** $1 \le amount \le 5000$, $1 \le coins.length \le 300$.
- **LeetCode Equivalent:** [518. Coin Change 2](https://leetcode.com/problems/coin-change-2/)
- **Approach:** Unbounded Knapsack DP: iterate coins on outer loop, amount on inner loop.
- **Complexity:** $O(N \times \text{amount})$ Time, $O(\text{amount})$ Space.

#### 20. Rotting Oranges / Multi-Source Infection
- **College/Drive:** Campus Slot 3 (2023)
- **Problem Summary:** Compute minimum time required for all fresh elements to spoil in a 2D matrix.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing all initially rotten oranges at time 0, decrementing fresh count with each minute layer.
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
4. **Database ACID & WAL:**
   - Why do relational databases write transaction logs to a Write-Ahead Log (WAL) before updating the main database pages on disk?
   - *Answer:* Writing sequentially to disk (append-only) is orders of magnitude faster than random I/O writes to B-Tree pages, ensuring atomicity and durability (durability guarantee) even during a sudden power loss.
