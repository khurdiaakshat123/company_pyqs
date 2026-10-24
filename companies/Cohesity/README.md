# Cohesity Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💾

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **CodeSignal** / **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  - 2 to 4 Algorithmic Coding Problems (LeetCode Medium to Hard).
  - (In select campus drives) 10 Technical MCQs covering Operating Systems, Multithreading, Distributed Storage, and Inodes.
- **Evaluation Criteria:**
  - Cohesity specializes in AI-powered enterprise backup, data protection, and distributed cloud file systems (45+ LPA CTC).
  - Robust algorithmic complexity, clean object-oriented modularity, and thread safety awareness are heavily evaluated.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Binary Search on Monotonic Predicates:** Capacity allocation, snapshot schedules, rate limiters.
- **Cache Eviction & Design:** LRU Cache, LFU Cache, Time-based key-value stores with version rollback.
- **Tree Structures & Lineage:** Lowest common ancestors, serialization/deserialization, tree DP.
- **Sliding Window & Monotonic Deques:** Window extrema over backup telemetry streams.
- **Graph BFS & Topological Sorting:** Build order dependencies, network cycle detection, shortest path in storage grids.
- **Distributed Systems MCQs:** Data deduplication (fixed-size vs variable-length chunking), snapshot mechanics, consistency models.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Minimum Days to Backup Files (Bouquets Binary Search Classic)
- **College/Drive:** IIT Roorkee / IIT Kharagpur 2024
- **Problem Statement:** You have $N$ files that need to be backed up on day `bloomDay[i]`. A snapshot requires $K$ adjacent files that are ready on the same day. You need to take $M$ total snapshots. Return the minimum number of days you need to wait to be able to take $M$ snapshots. If impossible, return -1.
- **LeetCode Equivalent:** [1482. Minimum Number of Days to Make m Bouquets](https://leetcode.com/problems/minimum-number-of-days-to-make-m-bouquets/)
- **Approach:** Binary Search on days in range $[\min, \max]$. Greedy verification counting contiguous blocks of size $K$.
- **Complexity:** $O(N \log(\max - \min))$ Time.

#### 2. LFU (Least Frequently Used) Cache Implementation
- **College/Drive:** BITS Pilani / IIIT Hyderabad 2024
- **Problem Statement:** Design and implement a data structure for a Least Frequently Used (LFU) cache with `get(key)` and `put(key, value)` running in $O(1)$ average time complexity.
- **LeetCode Equivalent:** [460. LFU Cache](https://leetcode.com/problems/lfu-cache/)
- **Approach:** Two Hash Maps: `key_table` mapping `key -> (value, freq, iterator)` and `freq_table` mapping `freq -> DoublyLinkedList<key>`. Maintain `min_freq` integer.
- **Complexity:** $O(1)$ Time per operation, $O(\text{Capacity})$ Space.

#### 3. Word Ladder / Incremental Data Block Transformation
- **College/Drive:** NIT Surathkal / DTU 2024
- **Problem Statement:** Given two file checksum strings `beginWord` and `endWord`, and a dictionary `wordList`, return the number of words in the shortest transformation sequence from `beginWord` to `endWord`.
- **LeetCode Equivalent:** [127. Word Ladder](https://leetcode.com/problems/word-ladder/)
- **Approach:** Bidirectional BFS or BFS with wildcard Hash Map.
- **Complexity:** $O(M^2 \times N)$ Time where $M$ is word length.

#### 4. Time-Based Key-Value Store (Snapshot Versioning)
- **College/Drive:** NSUT / IIIT Delhi 2024
- **Problem Statement:** Design a time-based key-value data structure that can store multiple values for the same key at different time stamps and retrieve the key's value at a certain timestamp.
- **LeetCode Equivalent:** [981. Time Based Key-Value Store](https://leetcode.com/problems/time-based-key-value-store/)
- **Approach:** Hash Map mapping `key -> vector<pair<timestamp, value>>`. Use `std::upper_bound` for $O(\log K)$ lookups.
- **Complexity:** $O(1)$ `set`, $O(\log K)$ `get`.

#### 5. Lowest Common Ancestor of Deepest Leaves (Snapshot Lineage)
- **College/Drive:** IIT Delhi / IIT Kanpur 2024
- **Problem Statement:** Given the root of a binary tree representing a file version branching tree, return the lowest common ancestor of its deepest leaves.
- **LeetCode Equivalent:** [1123. Lowest Common Ancestor of Deepest Leaves](https://leetcode.com/problems/lowest-common-ancestor-of-deepest-leaves/)
- **Approach:** Post-order traversal returning pair `(max_depth, lca_node)`. If left depth == right depth, current node is LCA. Otherwise, take the side with greater depth.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 6. Capacity To Ship Packages Within D Days (Minimum Backup Bandwidth)
- **College/Drive:** IIT Bombay 2024
- **Problem Statement:** A conveyor belt carries packages of weight `weights[i]`. We must ship all packages within `days` days in sequential order. Return the minimum ship capacity.
- **LeetCode Equivalent:** [1011. Capacity To Ship Packages Within D Days](https://leetcode.com/problems/capacity-to-ship-packages-within-d-days/)
- **Approach:** Binary search on capacity in range $[\max(\text{weights}), \sum \text{weights}]$. Greedy check in $O(N)$ time.
- **Complexity:** $O(N \log(\sum W))$ Time, $O(1)$ Space.

#### 7. Flatten Nested List Iterator (Snapshot Hierarchy Parser)
- **College/Drive:** BITS Pilani 2024
- **Problem Statement:** You are given a nested list of integers `nestedList`. Each element is either an integer or a list whose elements may also be integers or other lists. Implement an iterator to flatten it.
- **LeetCode Equivalent:** [341. Flatten Nested List Iterator](https://leetcode.com/problems/flatten-nested-list-iterator/)
- **Approach:** Stack storing iterators to the begin and end of nested vectors, lazily unpacking nested lists until top is an integer.
- **Complexity:** $O(1)$ amortized per `next()` call, $O(D)$ Space where $D$ is max nesting depth.

#### 8. Transactional In-Memory Key-Value Store (Begin, Commit, Rollback)
- **College/Drive:** Cohesity Campus Drive 2024 / IIIT Allahabad
- **Problem Statement:** Design an in-memory key-value store with transaction support: `SET(key, val)`, `GET(key)`, `DELETE(key)`, `BEGIN()`, `COMMIT()`, and `ROLLBACK()`. Transactions can be nested.
- **Approach:** Stack of Hash Maps representing transaction deltas. When `BEGIN()` is called, push an empty delta map. On `COMMIT()`, merge delta into parent map. On `ROLLBACK()`, discard top delta.
- **Complexity:** $O(1)$ average per operation, $O(T \times U)$ Space where $T$ is active transaction count.

#### 9. Redundant Connection (Storage Network Cycle Detection)
- **College/Drive:** IIT BHU 2024
- **Problem Statement:** Given a graph that started as a tree with $N$ nodes labeled $1$ to $N$, with one additional edge added. Return an edge that can be removed so that the resulting graph is a tree.
- **LeetCode Equivalent:** [684. Redundant Connection](https://leetcode.com/problems/redundant-connection/)
- **Approach:** Disjoint Set Union (DSU) with union-by-rank and path compression. The first edge connecting two nodes already in the same set is redundant.
- **Complexity:** $O(N \cdot \alpha(N))$ Time, $O(N)$ Space.

#### 10. Subarray Sum Equals K (Access Log Anomaly Detection)
- **College/Drive:** DTU Delhi 2024
- **Problem Statement:** Given an array of integers `nums` and an integer `k`, return the total number of continuous subarrays whose sum equals to `k`.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Running prefix sum with hash map storing frequency of prefix sums encountered so far.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Shortest Path in Binary Matrix (Storage Grid)
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Find shortest path in 8-directional binary grid from $(0, 0)$ to $(N-1, N-1)$.
- **LeetCode Equivalent:** [1091. Shortest Path in Binary Matrix](https://leetcode.com/problems/shortest-path-in-binary-matrix/)
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

#### 12. House Robber III (Tree Independent Node Sum)
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Maximum node sum in binary tree with no two directly connected nodes picked.
- **LeetCode Equivalent:** [337. House Robber III](https://leetcode.com/problems/house-robber-iii/)
- **Approach:** Post-order DFS returning pair `(rob_this_node, not_rob_this_node)`.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 13. Sliding Window Maximum (I/O Stream)
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Maximum write burst in every sliding window of size $K$.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 14. Merge Intervals (Backup Window De-duplication)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Merge overlapping backup schedule intervals.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time.

#### 15. Serialize and Deserialize Binary Tree
- **College/Drive:** IIT Roorkee 2023
- **Problem Statement:** Design an algorithm to serialize a binary tree to a string and deserialize that string back to the original tree structure.
- **LeetCode Equivalent:** [297. Serialize and Deserialize Binary Tree](https://leetcode.com/problems/serialize-and-deserialize-binary-tree/)
- **Approach:** Pre-order DFS traversal with delimiter and null-markers (`"#"`) or BFS level order queue.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 16. Find Minimum in Rotated Sorted Array
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** An array sorted in ascending order is rotated between 1 and $n$ times. Find the minimum element in $O(\log N)$ time.
- **LeetCode Equivalent:** [153. Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/)
- **Approach:** Binary search: compare `nums[mid]` with `nums[right]`. If `nums[mid] > nums[right]`, inflection point is on right (`left = mid + 1`); else `right = mid`.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 17. Course Schedule II / Task Dependency Resolution
- **College/Drive:** NIT Trichy 2023
- **Problem Statement:** Given $N$ tasks and prerequisite pairs, return the ordering of tasks you should pick to finish all tasks. If impossible, return empty array.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's algorithm using in-degree array and queue. If processed count $< N$, cycle exists.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 18. Trapping Rain Water
- **College/Drive:** NSUT Delhi 2023
- **Problem Statement:** Given $N$ non-negative integers representing an elevation map where the width of each bar is 1, compute how much water it can trap after raining.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers (`left = 0`, `right = n - 1`) maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 19. LRU Cache Implementation
- **College/Drive:** Campus Placement 2023
- **Problem Statement:** Implement Least Recently Used (LRU) cache with $O(1)$ `get` and `put`.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Hash Map pointing to Doubly Linked List nodes.
- **Complexity:** $O(1)$ Time per operation, $O(C)$ Space.

#### 20. Decode String / Chunked Decompression
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Given an encoded string like `"3[a2[c]]"`, return its decoded string `"accaccacc"`.
- **LeetCode Equivalent:** [394. Decode String](https://leetcode.com/problems/decode-string/)
- **Approach:** Two stacks: one for repeat counts `int`, one for current accumulated strings.
- **Complexity:** $O(\text{output length})$ Time and Space.

---

## 🧠 Frequent Systems & Storage MCQs Asked in Cohesity OA
1. **Fixed-Size vs Variable-Length Chunking for Deduplication:**
   - Why is content-defined chunking (e.g., using Rabin fingerprinting) superior to fixed-size chunking for file backups?
   - *Answer:* In fixed-size chunking, inserting a single byte at the beginning shifts all subsequent chunk boundaries, causing a total deduplication failure. Content-defined chunking finds boundaries based on rolling hash contents, isolating insertions to a single altered chunk.
2. **Snapshot Creation Mechanics (Copy-on-Write vs Redirect-on-Write):**
   - What is the performance difference between Copy-on-Write (COW) and Redirect-on-Write (ROW) snapshots during write operations?
   - *Answer:* COW incurs a double-write penalty (read old data, write old data to snapshot space, write new data to original block). ROW writes new data directly to a newly allocated block and updates pointers, eliminating the initial read overhead.
