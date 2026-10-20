# Graviton Research Capital Online Assessment Guide & PYQs (2023 - 2025/2026) ⚡

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **HackerEarth**
- **Test Duration:** 90 to 120 minutes
- **Structure Breakdown:**
  1. **Low-Level & Systems MCQs (30 mins):** 10 to 15 Questions covering C++20 internals, Cache Locality / Memory Alignment, OS Concurrency (Lock-free queues, Mutex vs Spinlocks), and Network Sockets.
  2. **Algorithmic Coding Section (60–90 mins):** 2 to 3 Hard Algorithmic Problems (Codeforces Div. 2 C/D/E level, 1600–2100 rating).
- **Evaluation Criteria:**
  - Graviton is a premier Indian High-Frequency Trading (HFT) firm with compensation reaching 1 Cr+ for freshers.
  - Test case evaluation includes rigorous execution time limits (strict 1.0s in C++, often 2.0s in Python). Solutions that use $O(N \log N)$ with heavy constant factor or unnecessary heap allocations will time out.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Stream & Packet In-Order Commit | Hard | Reordering out-of-order sequence packets, min-heaps with buffer watermarks |
| **Very High** | Advanced Dynamic Programming | Hard | Bitmask DP, state compression, Domino & Tromino tiling, Digit DP |
| **High** | Segment Trees & Fenwick Trees | Hard | Range updates, point queries, lazy propagation, coordinate compression |
| **High** | Shortest Paths & Graph Optimization | Hard | Multi-constraint Dijkstra, minimum bottleneck paths, 2-SAT / DSU |
| **Medium** | Low-Latency Systems MCQs | Medium - Hard | Cache lines (false sharing), atomic operations, branch prediction hints (`[[likely]]`) |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Real-Time Packet Stream Sequencer (HFT Core)
- **Problem Summary:** A market data feed receives packets `(seq_num, data)` out of order over UDP. Packets must be processed and committed *strictly in ascending order* starting from sequence 1. If packet $k$ is missing, all subsequent packets must be buffered. When packet $k$ arrives, output all consecutive available packets up to the next missing sequence number. Return total memory buffer required over $N$ stream events.
- **Approach:** Min-Heap or boolean hash map / direct index array with running `expected_seq` pointer.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

### 2. Domino and Tromino Tiling (Variation)
- **Problem Summary:** You have two types of tiles: a $2 \times 1$ domino and a tromino (L-shaped). Given an integer $n$, return the number of ways to tile a $2 \times n$ board modulo $10^9 + 7$.
- **LeetCode Equivalent:** [790. Domino and Tromino Tiling](https://leetcode.com/problems/domino-and-tromino-tiling/)
- **Approach:** Dynamic Programming with state transitions:
  $$dp[i] = (2 \times dp[i-1] + dp[i-3]) \pmod{10^9 + 7}$$
- **Complexity:** $O(N)$ Time or $O(\log N)$ via Matrix Exponentiation.

### 3. Range Maximum Queries with Coordinate Compression
- **Problem Summary:** Given $N$ intervals on a timeline with values, process $Q$ queries asking for the maximum value active at time $T$. Coordinates can be up to $10^9$.
- **Approach:** Coordinate Compression combined with a Segment Tree or Sweep Line with `std::map`.
- **Complexity:** $O((N + Q) \log N)$ Time.

### 4. Triplet Subsequence with Condition
- **Problem Summary:** Count the number of triplets $(i, j, k)$ such that $i < j < k$ and $A[i] < A[j] < A[k]$ in an array of size $N \le 10^5$.
- **Approach:** Coordinate compression + Fenwick Tree (Binary Indexed Tree) to count smaller elements on left and larger on right in $O(N \log N)$.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

---

## 🧠 Frequent C++ & Systems MCQs in Graviton OA
1. **False Sharing:** What causes false sharing in multi-threaded C++ applications?
   - *Answer:* Two threads running on separate CPU cores modifying independent variables that reside within the same 64-byte cache line, causing constant cache invalidations.
2. **Move Semantics:** What does `std::move` actually do?
   - *Answer:* It does NOT move any data; it unconditionally casts an expression to an rvalue reference (`T&&`), enabling move constructors and move assignment operators.
3. **Lock-Free Programming:** Which CPU instruction is foundational for implementing atomic compare-and-swap (CAS)? (`CMPXCHG` on x86/x64).
