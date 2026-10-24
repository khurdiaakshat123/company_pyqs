# Graviton Research Capital Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) ⚡

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **HackerEarth**
- **Test Duration:** 90 to 120 minutes
- **Structure Breakdown:**
  1. **Low-Level & Systems MCQs (30 mins):** 10 to 15 Questions covering C++20 internals, Cache Locality / Memory Alignment, OS Concurrency (Lock-free queues, Mutex vs Spinlocks), Memory Barriers, and Network Sockets.
  2. **Algorithmic Coding Section (60–90 mins):** 2 to 3 Hard Algorithmic Problems (Codeforces Div. 2 C/D/E level, 1700–2200 rating).
- **Evaluation Criteria:**
  - Graviton is a premier Indian High-Frequency Trading (HFT) firm offering CTC packages reaching 1 Cr+ for freshers across IITs/BITS.
  - Test case evaluation includes rigorous execution time limits (strict 1.0s in C++, fast I/O required). Heavy constant factor solutions or dynamic heap allocations (`new`, `malloc` inside loops) will TLE.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Stream & Packet In-Order Commit:** Reordering out-of-order sequence packets, min-heaps with buffer watermarks, zero-copy queues.
- **Advanced Dynamic Programming:** Bitmask DP, state compression, Domino & Tromino tiling with matrix exponentiation, Digit DP.
- **Segment Trees & Fenwick Trees:** Range updates, point queries, lazy propagation, coordinate compression, dynamic trees.
- **Shortest Paths & Graph Optimization:** Multi-constraint Dijkstra, minimum bottleneck paths, 2-SAT / DSU.
- **Low-Latency Systems MCQs:** Cache lines (false sharing), atomic operations, branch prediction hints (`[[likely]]`), virtual table overhead.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Real-Time Packet Stream Sequencer (HFT Core)
- **College/Drive:** IIT Delhi / IIT Bombay Campus Hiring 2024–2025
- **Problem Summary:** A market data feed receives packets `(seq_num, data)` out of order over UDP. Packets must be processed and committed *strictly in ascending order* starting from sequence 1. If packet $k$ is missing, all subsequent packets must be buffered. When packet $k$ arrives, output all consecutive available packets up to the next missing sequence number. Return total peak memory buffer required over $N$ stream events.
- **Constraints:** $1 \le N \le 10^6$, $1 \le seq\_num \le N$.
- **Approach:** Min-Heap or boolean hash map / direct index array with running `expected_seq` pointer.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 2. Domino and Tromino Tiling (Matrix Exponentiation)
- **College/Drive:** IIT Kanpur / IIT Madras 2024–2025
- **Problem Summary:** You have two types of tiles: a $2 \times 1$ domino and an L-shaped tromino. Given an integer $n \le 10^9$, return the number of ways to tile a $2 \times n$ board modulo $10^9 + 7$.
- **Constraints:** $1 \le n \le 10^9$.
- **LeetCode Equivalent:** [790. Domino and Tromino Tiling](https://leetcode.com/problems/domino-and-tromino-tiling/)
- **Approach:** Linear recurrence $dp[i] = 2 \cdot dp[i-1] + dp[i-3]$. For $N \le 10^9$, formulate companion transition matrix $3 \times 3$ and compute via Binary Matrix Exponentiation.
- **Complexity:** $O(3^3 \cdot \log N) = O(\log N)$ Time, $O(1)$ Space.

#### 3. Range Maximum Queries with Coordinate Compression
- **College/Drive:** BITS Pilani / IIT Roorkee 2024–2025
- **Problem Summary:** Given $N$ intervals on a timeline with values, process $Q$ queries asking for the maximum value active at time $T$. Coordinates can be up to $10^9$.
- **Constraints:** $1 \le N, Q \le 10^5$, coordinates in $[1, 10^9]$.
- **Approach:** Coordinate Compression combined with a Segment Tree or Sweep Line with `std::map`.
- **Complexity:** $O((N + Q) \log N)$ Time, $O(N)$ Space.

#### 4. Increasing Triplet & Subsequence Counting (Fenwick Tree)
- **College/Drive:** IIT Kharagpur / IIT BHU 2024–2025
- **Problem Summary:** Count the number of triplets $(i, j, k)$ such that $i < j < k$ and $A[i] < A[j] < A[k]$ in an array of size $N \le 10^5$.
- **Constraints:** $1 \le N \le 10^5$, $-10^9 \le A[i] \le 10^9$.
- **Approach:** Coordinate compression + Fenwick Tree (Binary Indexed Tree) to count smaller elements on left and larger on right in $O(N \log N)$.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 5. Multi-Source Bottleneck Shortest Path (Modified Dijkstra)
- **College/Drive:** Graviton On-Campus Slot 2024–2025
- **Problem Summary:** In a weighted network with latency and bandwidth caps, find the path between source and target that minimizes latency while ensuring bandwidth is at least $B$.
- **Constraints:** $V \le 10^4, E \le 5 \times 10^4$.
- **Approach:** Binary Search on bandwidth bottleneck combined with Dijkstra's shortest path algorithm on valid edges.
- **Complexity:** $O(E \log V \cdot \log(\text{max\_bandwidth}))$ Time.

#### 6. Lowest Common Ancestor with Binary Lifting & Path Max Edge
- **College/Drive:** IIT Guwahati / IIT Roorkee 2024
- **Problem Summary:** Given a weighted tree with $N$ vertices, answer $Q$ queries asking for the maximum weight edge on the unique simple path between node $u$ and node $v$.
- **Constraints:** $N, Q \le 10^5$, edge weights $\le 10^9$.
- **Approach:** Binary Lifting table `up[node][i]` storing the $2^i$-th ancestor and `max_edge[node][i]` storing max edge along that jump.
- **Complexity:** $O(N \log N)$ preprocessing, $O(\log N)$ per query.

#### 7. Trapping Rain Water II (3D Elevation Priority Queue)
- **College/Drive:** Graviton Coding Challenge 2024
- **Problem Summary:** Given an $M \times N$ integer matrix `heightMap` representing the height of each unit cell in a 2D elevation map, return the volume of water it can trap after raining.
- **Constraints:** $1 \le M, N \le 200$, $0 \le heightMap[i][j] \le 2 \times 10^4$.
- **LeetCode Equivalent:** [407. Trapping Rain Water II](https://leetcode.com/problems/trapping-rain-water-ii/)
- **Approach:** Min-Heap prioritizing boundary cells. Greedily expand inwards from lowest boundary cell; water trapped at neighbor is $\max(0, \text{curr\_height} - \text{neighbor\_height})$.
- **Complexity:** $O(M \cdot N \log(M \cdot N))$ Time, $O(M \cdot N)$ Space.

#### 8. Longest Valid Parentheses Substring
- **College/Drive:** IIT Delhi / IIT Bombay Slot 2024
- **Problem Summary:** Given a string containing just the characters `'('` and `')'`, find the length of the longest valid (well-formed) parentheses substring.
- **Constraints:** $1 \le s.length \le 10^5$.
- **LeetCode Equivalent:** [32. Longest Valid Parentheses](https://leetcode.com/problems/longest-valid-parentheses/)
- **Approach:** Stack initialized with index `-1`. Push `'('` indices. On `')'`, pop top; if stack is empty, push current index as new boundary; else update `max_len = max(max_len, i - stack.top())`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 9. Count of Smaller Numbers After Self
- **College/Drive:** Graviton Quant Research Drive 2024
- **Problem Summary:** Given an integer array `nums`, return an integer array `counts` where `counts[i]` is the number of smaller elements to the right of `nums[i]`.
- **Constraints:** $1 \le nums.length \le 10^5$, $-10^4 \le nums[i] \le 10^4$.
- **LeetCode Equivalent:** [315. Count of Smaller Numbers After Self](https://leetcode.com/problems/count-of-smaller-numbers-after-self/)
- **Approach:** Coordinate compression + Fenwick Tree traversed from right to left, querying prefix sum of counts and adding 1 at the current value index.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 10. Sliding Window Median (Dual Multiset / PBDS)
- **College/Drive:** BITS Pilani Slot 2024
- **Problem Summary:** Given an integer array `nums` and a window size `k`, find the median of every sliding window of size `k`.
- **Constraints:** $1 \le nums.length \le 10^5$, $1 \le k \le nums.length$.
- **LeetCode Equivalent:** [480. Sliding Window Median](https://leetcode.com/problems/sliding-window-median/)
- **Approach:** Two balanced multisets or C++ Policy-Based Data Structure `tree<pair<int, int>, null_type, less<...>, rb_tree_tag, tree_order_statistics_node_update>`.
- **Complexity:** $O(N \log K)$ Time, $O(K)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Maximum XOR Subarray / Path in Tree
- **College/Drive:** IIT Delhi Slot 1 (2023)
- **Problem Summary:** Find maximum XOR sum along any simple path in a weighted tree.
- **Constraints:** $N \le 10^5$, edge weights $\le 2^{30}$.
- **Approach:** Compute root-to-node XOR distances for all nodes; insert into a 32-bit Binary Trie and query maximum XOR pair.
- **Complexity:** $O(N \log (\text{max\_val}))$ Time, $O(N)$ Space.

#### 12. Tree Center and Diameter with Dynamic Weighted Edges
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find the diameter and centers of a weighted tree where edge weights represent transmission delay.
- **Constraints:** $V \le 10^5, E = V - 1$.
- **Approach:** Two-pass BFS/DFS to find diameter endpoints, followed by path midpoint tracking.
- **Complexity:** $O(V + E)$ Time.

#### 13. Lock-Free Circular Ring Buffer Simulation
- **College/Drive:** Graviton Systems Round 2023
- **Problem Summary:** Design a Single Producer Single Consumer (SPSC) ring buffer with non-blocking push and pop operations using atomic sequence pointers.
- **Constraints:** Cache line padding (`alignas(64)`), zero lock contention.
- **Approach:** Fixed-size array with power-of-two capacity, cache line padding (`alignas(64)`) to prevent false sharing between head and tail pointers.
- **Complexity:** $O(1)$ per operation.

#### 14. Minimum Cost to Assign Tasks to Workers (Bitmask DP)
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Assign $N$ tasks to $N$ workers where cost of assigning task $i$ to worker $j$ is $C_{i, j}$. Minimize total assignment cost ($N \le 20$).
- **Constraints:** $N \le 20$, $C_{i, j} \le 10^4$.
- **Approach:** Bitmask Dynamic Programming: `dp[mask]` represents minimum cost to assign first `popcount(mask)` tasks to workers represented by `mask`.
- **Complexity:** $O(N \cdot 2^N)$ Time, $O(2^N)$ Space.

#### 15. Maximum Flow / Bipartite Matching on Trading Network
- **College/Drive:** IIT Bombay Slot 2 (2023)
- **Problem Summary:** Given orders and executing brokers with transaction limits, find maximum executable orders.
- **Constraints:** $V \le 5000, E \le 3 \times 10^4$.
- **Approach:** Dinic’s Algorithm for Max Flow or Hopcroft-Karp for Maximum Bipartite Matching.
- **Complexity:** $O(E \sqrt{V})$ Time.

#### 16. Word Break II with Trie & Backtracking
- **College/Drive:** IIT Madras Slot 2023
- **Problem Summary:** Given a string `s` and a dictionary of words `wordDict`, add spaces in `s` to construct a sentence where each word is a valid dictionary word. Return all possible sentences.
- **Constraints:** $1 \le s.length \le 20$, $1 \le wordDict.length \le 1000$.
- **LeetCode Equivalent:** [140. Word Break II](https://leetcode.com/problems/word-break-ii/)
- **Approach:** Trie of dictionary words combined with DFS and memoization to cache valid sentence suffixes.
- **Complexity:** $O(2^N)$ worst case, heavily pruned by Trie.

#### 17. Shortest Subarray with Sum at Least K
- **College/Drive:** IIT Kharagpur 2023
- **Problem Summary:** Given an integer array `nums` and an integer `k`, return the length of the shortest non-empty subarray of `nums` with a sum of at least `k`. If no such subarray exists, return -1. Array can contain negative numbers.
- **Constraints:** $1 \le nums.length \le 10^5$, $-10^5 \le nums[i] \le 10^5$, $1 \le k \le 10^9$.
- **LeetCode Equivalent:** [862. Shortest Subarray with Sum at Least K](https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/)
- **Approach:** Prefix sums with Monotonic Queue (Deque). Maintain deque of increasing prefix sums; pop from front when condition `P[i] - P[opt] >= k` is met, pop from back if `P[i] <= P[back]`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 18. Median of Two Sorted Arrays
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Given two sorted arrays `nums1` and `nums2` of size $m$ and $n$ respectively, return the median of the two sorted arrays in $O(\log(m+n))$ runtime.
- **Constraints:** $0 \le m, n \le 1000$, $m + n \ge 1$.
- **LeetCode Equivalent:** [4. Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)
- **Approach:** Binary search on the partition of the smaller array ensuring left half elements $\le$ right half elements.
- **Complexity:** $O(\log(\min(M, N)))$ Time, $O(1)$ Space.

#### 19. Substring with Concatenation of All Words
- **College/Drive:** IIT Roorkee 2023
- **Problem Summary:** Given a string `s` and an array of strings `words` of equal length, find all starting indices of substring(s) in `s` that is a concatenation of each word in `words` exactly once.
- **Constraints:** $1 \le s.length \le 10^4$, $1 \le words.length \le 5000$, word length $\le 30$.
- **LeetCode Equivalent:** [30. Substring with Concatenation of All Words](https://leetcode.com/problems/substring-with-concatenation-of-all-words/)
- **Approach:** Sliding window across word length offsets ($0$ to $L-1$). Maintain word frequency hash map within window.
- **Complexity:** $O(L \cdot (N / L)) = O(N)$ Time, $O(K \cdot L)$ Space.

#### 20. Maximum Frequency Stack (FreqStack)
- **College/Drive:** Off-Campus Screening 2023
- **Problem Summary:** Design a stack-like data structure to push elements and pop the most frequent element. If there is a tie, pop the element closest to the stack's top.
- **Constraints:** Up to $2 \times 10^4$ push and pop operations.
- **LeetCode Equivalent:** [895. Maximum Frequency Stack](https://leetcode.com/problems/maximum-frequency-stack/)
- **Approach:** Frequency map `freq[val]` + map of stacks `group[f]` storing elements with frequency $f$ + `max_freq` counter.
- **Complexity:** $O(1)$ Time per push and pop, $O(N)$ Space.

---

## 🧠 Frequent C++ & Systems MCQs in Graviton OA
1. **False Sharing:**
   - What causes false sharing in multi-threaded C++ applications?
   - *Answer:* Two threads on separate CPU cores modifying independent variables that reside within the same 64-byte cache line, causing constant cache invalidations. Resolved with `alignas(64)`.
2. **Move Semantics:**
   - What does `std::move` actually do?
   - *Answer:* It does NOT move any data; it unconditionally casts an lvalue to an rvalue reference (`T&&`), enabling move constructors and move assignment operators.
3. **Atomic Operations & Memory Orders:**
   - What is the difference between `std::memory_order_relaxed` and `std::memory_order_seq_cst`?
   - *Answer:* `relaxed` only guarantees atomicity for the variable without synchronization or memory ordering constraints across threads, while `seq_cst` enforces a single globally consistent order of execution across all threads with full memory barriers.
4. **Virtual Functions & VTable Overhead:**
   - Why do HFT low-latency systems strictly avoid dynamic polymorphism (`virtual` methods) on critical trading paths?
   - *Answer:* Virtual methods incur pointer indirection overhead (dereferencing `vptr` to access `vtable`), and more importantly prevent compiler inlining and branch prediction optimizations. CRTP (Curiously Recurring Template Pattern) is used instead for compile-time polymorphism.
