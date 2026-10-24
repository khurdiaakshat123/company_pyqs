# Rubrik Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🛡️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  - 2 to 4 Algorithmic Coding Questions (Competitive Programming / LeetCode Hard level).
  - (In some on-campus drives) 5 to 10 Technical MCQs covering Operating Systems, Multithreading, Concurrency, and Memory Alignment.
- **Evaluation Criteria:**
  - Rubrik builds cloud data management and zero-trust cybersecurity systems. Their OA is known as one of the most mathematically and algorithmically demanding assessments.
  - Test cases impose strict $10^5$ to $2 \times 10^5$ constraints requiring rigorous $O(N)$ or $O(N \log N)$ approaches with minimal constant factors.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Advanced Bit Manipulation & Ranges:** Bitwise AND/OR/XOR range combinations modulo $10^9+7$, bitmask DP, bitwise trie lookups.
- **Dynamic Programming on Trees & Intervals:** Tree DP, burst balloons, longest chunked palindromes, subsequence transitions.
- **Heaps & Custom Greedy Scheduling:** Priority queues, minimum cost to hire K workers, sliding window stream aggregation.
- **Trie & In-Memory Hierarchies:** In-memory file system trees, prefix lookups, string decomposition.
- **Graph Component Optimization:** Tarjan's bridges/SCCs, Eulerian paths, shortest path with state expansion.
- **Systems & Concurrency MCQs:** Deadlock prevention, lock-free queues, paging, virtual memory, copy-on-write semantics.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Sum of Bitwise AND Over All Subarrays
- **College/Drive:** IIT Delhi / IIT Kanpur 2024
- **Problem Summary:** Given an array of integers $A$ of length $N$, find the sum of bitwise AND of all possible contiguous subarrays modulo $10^9 + 7$.
- **Approach:** Bitwise contribution technique: For each of the 30 bits, evaluate the number of contiguous subarrays where that bit is 1 (all elements in the subsegment have that bit set). Multiply by $2^{\text{bit}}$ and sum modulo $10^9 + 7$.
- **Complexity:** $O(30 \times N) = O(N)$ Time, $O(1)$ Extra Space.

#### 2. File Snapshot Tree Synchronization (Tree DP + Bitmask)
- **College/Drive:** IIT Bombay / IIT Madras 2024
- **Problem Summary:** Given a tree representing a nested directory structure where each directory node contains an access permission bitmask. Find the minimum number of edge cuts required such that no connected component contains conflicting security permissions.
- **Approach:** Tree DP with bottom-up bitmask propagation or Disjoint Set Union (DSU) checking component validity.
- **Complexity:** $O(N \times 2^K)$ Time where $K \le 5$.

#### 3. Trapping Rain Water II (3D Elevation Grid)
- **College/Drive:** BITS Pilani / IIT Roorkee 2024
- **Problem Summary:** Given an $M \times N$ integer matrix `heightMap` representing the height of each unit cell in a 2D elevation map, return the volume of water it can trap after raining.
- **LeetCode Equivalent:** [407. Trapping Rain Water II](https://leetcode.com/problems/trapping-rain-water-ii/)
- **Approach:** Min-Heap storing boundary cells. Pop the lowest boundary cell, explore its 4 neighbors, update trapped water if neighbor is lower, push neighbor with $\max(\text{neighbor}, \text{current})$ into heap.
- **Complexity:** $O(M \times N \log(M \times N))$ Time.

#### 4. Longest Chunked Palindrome Decomposition
- **College/Drive:** IIIT Hyderabad / IIT BHU 2024
- **Problem Summary:** You are given a string `text`. Split it into $k$ non-empty substrings $(sub_1, sub_2, \dots, sub_k)$ such that $sub_1 == sub_k$, $sub_2 == sub_{k-1}$, etc. Return the largest possible $k$.
- **LeetCode Equivalent:** [1147. Longest Chunked Palindrome Decomposition](https://leetcode.com/problems/longest-chunked-palindrome-decomposition/)
- **Approach:** Greedy matching from outer ends inward using Rolling Hash (Rabin-Karp) or Two Pointers.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Critical Connections in a Network (Tarjan's Bridges)
- **College/Drive:** Campus Placement Drive 2024
- **Problem Summary:** Find all critical connections (bridges) in a network of servers such that removal of any of these edges disconnects the network.
- **LeetCode Equivalent:** [1192. Critical Connections in a Network](https://leetcode.com/problems/critical-connections-in-a-network/)
- **Approach:** Tarjan’s DFS algorithm maintaining `discovery_time` and `lowest_reachable_time`.
- **Complexity:** $O(V + E)$ Time, $O(V)$ Space.

#### 6. Design In-Memory File System with Directory Search
- **College/Drive:** IIT Roorkee / IIT Kharagpur 2025
- **Problem Summary:** Design a data structure that simulates an in-memory file system with APIs: `ls(path)`, `mkdir(path)`, `addContentToFile(filePath, content)`, and `readContentFromFile(filePath)`.
- **LeetCode Equivalent:** [588. Design In-Memory File System](https://leetcode.com/problems/design-in-memory-file-system/)
- **Approach:** Trie-like hierarchical structure where each `Node` contains a dictionary of child directory/file names and string content for files.
- **Complexity:** $O(L)$ where $L$ is path depth and string length.

#### 7. Minimum Interval to Include Each Query
- **College/Drive:** IIT Kanpur / BITS Pilani 2024
- **Problem Summary:** Given a 2D integer array `intervals` and an array of integers `queries`, for each query, find the size of the smallest interval `[left, right]` such that `left <= query <= right`. If no interval contains it, return `-1`.
- **LeetCode Equivalent:** [1851. Minimum Interval to Include Each Query](https://leetcode.com/problems/minimum-interval-to-include-each-query/)
- **Approach:** Sort intervals by start time and sort queries with their original indices. Use a Min-Heap ordered by interval length `(right - left + 1, right)`: push eligible intervals starting $\le \text{query}$, lazily pop expired intervals whose `right < query`.
- **Complexity:** $O(N \log N + Q \log Q)$ Time, $O(N + Q)$ Space.

#### 8. Sliding Window Maximum / Stream Deduplication
- **College/Drive:** IIT Bombay 2024
- **Problem Summary:** You are given an array of integers `nums`, there is a sliding window of size `k` moving from the very left to the very right. Return the max sliding window.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Approach:** Monotonic Decreasing Deque storing indices. Maintain deque in strictly decreasing order of values and evict indices outside current window.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 9. Substring with Concatenation of All Words
- **College/Drive:** IIT Madras / IIIT Hyderabad 2024
- **Problem Summary:** Given a string `s` and an array of strings `words` of the same length, return the starting indices of all concatenated substrings that contain each word exactly once without intervening characters.
- **LeetCode Equivalent:** [30. Substring with Concatenation of All Words](https://leetcode.com/problems/substring-with-concatenation-of-all-words/)
- **Approach:** Sliding window over word boundaries (offsets $0$ to $\text{word\_len} - 1$) with frequency hash maps.
- **Complexity:** $O(N \times \text{word\_len})$ Time.

#### 10. Word Break II (Reconstruct File Path Tokens)
- **College/Drive:** IIT Kharagpur 2024
- **Problem Summary:** Given a string `s` and a dictionary of strings `wordDict`, add spaces in `s` to construct a sentence where each word is a valid dictionary word. Return all such possible sentences.
- **LeetCode Equivalent:** [140. Word Break II](https://leetcode.com/problems/word-break-ii/)
- **Approach:** DFS backtracking memoized with a Hash Map `unordered_map<string, vector<string>> memo` or Trie.
- **Complexity:** $O(2^N)$ worst-case output, optimal with memoization.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Minimum Cost to Hire K Workers
- **College/Drive:** IIT Delhi Slot 1 (2023)
- **Problem Summary:** Choose $K$ workers paid proportionally to their quality such that total wage is minimized.
- **LeetCode Equivalent:** [857. Minimum Cost to Hire K Workers](https://leetcode.com/problems/minimum-cost-to-hire-k-workers/)
- **Approach:** Sort by `wage/quality` ratio; maintain Max-Heap of quality values of size $K$.
- **Complexity:** $O(N \log N)$ Time, $O(K)$ Space.

#### 12. Burst Balloons (Interval Dynamic Programming)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Burst balloons to collect maximum coins where coins for balloon $i$ are $nums[i-1] \times nums[i] \times nums[i+1]$.
- **LeetCode Equivalent:** [312. Burst Balloons](https://leetcode.com/problems/burst-balloons/)
- **Approach:** Interval DP: `dp[left][right] = max(dp[left][i-1] + nums[left-1]*nums[i]*nums[right+1] + dp[i+1][right])`.
- **Complexity:** $O(N^3)$ Time, $O(N^2)$ Space.

#### 13. Count Subarrays with Median K
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Given array of distinct integers, find number of non-empty subarrays that have median equal to $K$.
- **LeetCode Equivalent:** [2448. Count Subarrays With Median K](https://leetcode.com/problems/count-subarrays-with-median-k/)
- **Approach:** Map elements to $+1$ if $>K$, $-1$ if $<K$, $0$ if $==K$. Compute prefix sums with hash map.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 14. Shortest Path in Binary Matrix with Direction Constraints
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** 8-directional shortest path on binary grid from top-left to bottom-right.
- **LeetCode Equivalent:** [1091. Shortest Path in Binary Matrix](https://leetcode.com/problems/shortest-path-in-binary-matrix/)
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

#### 15. Maximum XOR of Two Numbers in an Array
- **College/Drive:** Campus Slot 3 (2023)
- **Problem Summary:** Return maximum XOR value among any two integers in array.
- **LeetCode Equivalent:** [421. Maximum XOR of Two Numbers in an Array](https://leetcode.com/problems/maximum-xor-of-two-numbers-in-an-array/)
- **Approach:** Binary Prefix Trie (Bit 31 down to 0).
- **Complexity:** $O(32 \cdot N)$ Time, $O(32 \cdot N)$ Space.

#### 16. Find Median from Data Stream
- **College/Drive:** IIT Madras 2023
- **Problem Summary:** Design a data structure that supports adding numbers from a data stream and finding the median of all elements.
- **LeetCode Equivalent:** [295. Find Median from Data Stream](https://leetcode.com/problems/find-median-from-data-stream/)
- **Approach:** Two heaps: Max-Heap for lower half, Min-Heap for upper half, keeping sizes balanced within 1 element difference.
- **Complexity:** $O(\log N)$ for `addNum()`, $O(1)$ for `findMedian()`.

#### 17. Course Schedule III (Greedy with Max-Heap)
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Given $N$ courses where `courses[i] = [duration, lastDay]`, find the maximum number of courses you can take if you start on day 1.
- **LeetCode Equivalent:** [630. Course Schedule III](https://leetcode.com/problems/course-schedule-iii/)
- **Approach:** Sort courses by deadline `lastDay`. Iterate through courses, tracking cumulative time and pushing duration into a Max-Heap. If cumulative time exceeds `lastDay`, pop the largest duration course from the heap.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 18. Longest Increasing Path in a Matrix
- **College/Drive:** BITS Pilani 2023
- **Problem Summary:** Given an $M \times N$ integer matrix, return the length of the longest increasing path.
- **LeetCode Equivalent:** [329. Longest Increasing Path in a Matrix](https://leetcode.com/problems/longest-increasing-path-in-a-matrix/)
- **Approach:** DFS with memoization or topological sort (Kahn's algorithm on DAG).
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 19. Reconstruct Itinerary (Eulerian Path)
- **College/Drive:** IIT Guwahati 2023
- **Problem Summary:** Given a list of airline tickets represented by pairs of departure and arrival airports `[from, to]`, reconstruct the itinerary in order, starting from `"JFK"` and using all tickets.
- **LeetCode Equivalent:** [332. Reconstruct Itinerary](https://leetcode.com/problems/reconstruct-itinerary/)
- **Approach:** Hierholzer's algorithm for finding Eulerian Path using DFS and adjacency lists sorted lexicographically.
- **Complexity:** $O(E \log E)$ Time, $O(V + E)$ Space.

#### 20. Binary Tree Maximum Path Sum
- **College/Drive:** Rubrik Off-Campus Assessment 2023
- **Problem Summary:** A path in a binary tree is a sequence of nodes where each pair of adjacent nodes has an edge. Return the maximum path sum of any non-empty path.
- **LeetCode Equivalent:** [124. Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/)
- **Approach:** Post-order DFS returning the maximum branch gain (`max(0, dfs(child))`). Update global max at each node with `node->val + left_gain + right_gain`.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

---

## 🧠 Frequent Systems & OS MCQs Asked in Rubrik OA
1. **Copy-on-Write (COW):**
   - How does Unix `fork()` optimize memory consumption when creating child processes?
   - *Answer:* Instead of duplicating all physical memory pages, both parent and child processes share the same read-only pages. A page is only duplicated when either process attempts to write to it.
2. **Lock-Free Single-Producer Single-Consumer (SPSC) Queue:**
   - Why can an SPSC queue operate without mutexes or atomic CAS instructions?
   - *Answer:* Because the head pointer is only written by the consumer and the tail pointer is only written by the producer. Memory fences (`acquire`/`release`) ensure visibility without contention.
3. **Write Amplification in Log-Structured File Systems:**
   - What causes write amplification in Log-Structured Merge (LSM) trees and Flash SSDs?
   - *Answer:* Background compaction and garbage collection processes rewrite and merge existing data blocks multiple times to reclaim stale blocks and optimize read locality.
