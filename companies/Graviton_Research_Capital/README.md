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
- **College/Drive:** IIT Delhi / IIT Bombay Campus Hiring 2024
- **Problem Summary:** A market data feed receives packets `(seq_num, data)` out of order over UDP. Packets must be processed and committed *strictly in ascending order* starting from sequence 1. If packet $k$ is missing, all subsequent packets must be buffered. When packet $k$ arrives, output all consecutive available packets up to the next missing sequence number. Return total peak memory buffer required over $N$ stream events.
- **Approach:** Min-Heap or boolean hash map / direct index array with running `expected_seq` pointer.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 2. Domino and Tromino Tiling (Matrix Exponentiation)
- **College/Drive:** IIT Kanpur / IIT Madras 2024
- **Problem Summary:** You have two types of tiles: a $2 \times 1$ domino and an L-shaped tromino. Given an integer $n \le 10^9$, return the number of ways to tile a $2 \times n$ board modulo $10^9 + 7$.
- **LeetCode Equivalent:** [790. Domino and Tromino Tiling](https://leetcode.com/problems/domino-and-tromino-tiling/)
- **Approach:** Linear recurrence $dp[i] = 2 \cdot dp[i-1] + dp[i-3]$. For $N \le 10^9$, formulate companion transition matrix $3 \times 3$ and compute via Binary Matrix Exponentiation.
- **Complexity:** $O(3^3 \cdot \log N) = O(\log N)$ Time, $O(1)$ Space.

#### 3. Range Maximum Queries with Coordinate Compression
- **College/Drive:** BITS Pilani / IIT Roorkee 2024
- **Problem Summary:** Given $N$ intervals on a timeline with values, process $Q$ queries asking for the maximum value active at time $T$. Coordinates can be up to $10^9$.
- **Approach:** Coordinate Compression combined with a Segment Tree or Sweep Line with `std::map`.
- **Complexity:** $O((N + Q) \log N)$ Time, $O(N)$ Space.

#### 4. Increasing Triplet & Subsequence Counting (Fenwick Tree)
- **College/Drive:** IIT Kharagpur / IIT BHU 2024
- **Problem Summary:** Count the number of triplets $(i, j, k)$ such that $i < j < k$ and $A[i] < A[j] < A[k]$ in an array of size $N \le 10^5$.
- **Approach:** Coordinate compression + Fenwick Tree (Binary Indexed Tree) to count smaller elements on left and larger on right in $O(N \log N)$.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 5. Multi-Source Bottleneck Shortest Path (Modified Dijkstra)
- **College/Drive:** Graviton On-Campus Slot 2024
- **Problem Summary:** In a weighted network with latency and bandwidth caps, find the path between source and target that minimizes latency while ensuring bandwidth is at least $B$.
- **Approach:** Binary Search on bandwidth bottleneck combined with Dijkstra's shortest path algorithm on valid edges.
- **Complexity:** $O(E \log V \cdot \log(\text{max\_bandwidth}))$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Maximum XOR Subarray / Path in Tree
- **College/Drive:** IIT Delhi Slot 1 (2023)
- **Problem Summary:** Find maximum XOR sum along any simple path in a weighted tree.
- **Approach:** Compute root-to-node XOR distances for all nodes; insert into a 32-bit Binary Trie and query maximum XOR pair.
- **Complexity:** $O(N \log (\text{max\_val}))$ Time, $O(N)$ Space.

#### 7. Tree Center and Diameter with Dynamic Weighted Edges
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find the diameter and centers of a weighted tree where edge weights represent transmission delay.
- **Approach:** Two-pass BFS/DFS to find diameter endpoints, followed by path midpoint tracking.
- **Complexity:** $O(V + E)$ Time.

#### 8. Lock-Free Circular Ring Buffer Simulation
- **College/Drive:** Graviton Systems Round 2023
- **Problem Summary:** Design a Single Producer Single Consumer (SPSC) ring buffer with non-blocking push and pop operations using atomic sequence pointers.
- **Approach:** Fixed-size array with power-of-two capacity, cache line padding (`alignas(64)`) to prevent false sharing between head and tail pointers.
- **Complexity:** $O(1)$ per operation.

#### 9. Minimum Cost to Assign Tasks to Workers (Bitmask DP)
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Assign $N$ tasks to $N$ workers where cost of assigning task $i$ to worker $j$ is $C_{i, j}$. Minimize total assignment cost ($N \le 20$).
- **Approach:** Bitmask Dynamic Programming: `dp[mask]` represents minimum cost to assign first `popcount(mask)` tasks to workers represented by `mask`.
- **Complexity:** $O(N \cdot 2^N)$ Time, $O(2^N)$ Space.

#### 10. Maximum Flow / Bipartite Matching on Trading Network
- **College/Drive:** IIT Bombay Slot 2 (2023)
- **Problem Summary:** Given orders and executing brokers with transaction limits, find maximum executable orders.
- **Approach:** Dinic’s Algorithm for Max Flow or Hopcroft-Karp for Maximum Bipartite Matching.
- **Complexity:** $O(E \sqrt{V})$ Time.

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
