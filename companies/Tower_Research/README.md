# Tower Research Capital Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) ⚡

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / Proprietary low-latency testing environment
- **Test Duration:** 75 to 120 minutes
- **Structure Breakdown:**
  1. **Algorithmic Coding Section (60–90 mins, 2 to 3 Questions):** High-difficulty problems (Codeforces Div. 2 D/E level, 1800–2200 rating).
  2. **C++ Code Debugging Challenge (20–30 mins):** Fix subtle concurrency bugs, memory corruption, off-by-one errors, or algorithmic bottlenecks in pre-existing C++ production code with minimal diffs.
  3. **Low-Latency & Systems MCQs (20 mins):** C++ memory models, STL internals (allocators, `std::vector` reallocation amortized math), OS kernel bypass, TCP socket options (`TCP_NODELAY`, `SO_REUSEADDR`).
- **Evaluation Criteria:**
  - Tower Research is a premier global quantitative trading firm.
  - Strict computational execution bounds (strict 1.0s limit in C++). Even asymptotically optimal solutions with bloated overhead or heavy cache-miss rates will fail hidden performance checks.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Advanced Graph Algorithms:** Shortest path with transfer penalties, 0-1 BFS, Eulerian paths, DSU with bipartite verification.
- **C++ Code Debugging & STL Internals:** Iterator invalidation, memory alignment, memory leaks, multithreading race conditions.
- **Bit Manipulation & Number Theory:** Bitmask DP, Taxicab numbers, modular inverse, prime factorization, Fast Fourier Transform (FFT) basics.
- **Monotonic Deque & Sweepline:** Sliding window extrema with dynamic updates, interval scheduling, maximum area under histogram.
- **Systems & Architecture MCQs:** Cache line false sharing, atomic CAS, virtual memory page size, huge pages.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Minimal Edge Weight Adjustment in Graph (0-1 BFS)
- **College/Drive:** IIT Delhi / IIT Kanpur Campus Drive 2024
- **Problem Summary:** Given a directed graph with $N$ vertices and $M$ edges. You want to travel from node 1 to node $N$. Some edges are directed in the wrong direction; reversing a directed edge costs 1 unit. Find the minimum cost to reach node $N$.
- **Approach:** 0-1 BFS: For each existing edge $u \to v$, assign weight 0. Add a reverse edge $v \to u$ with weight 1. Use a `std::deque`: push weight-0 transitions to the front, weight-1 transitions to the back.
- **Complexity:** $O(V + E)$ Time, $O(V)$ Space.

#### 2. Taxicab Numbers (Dual Cube Representations)
- **College/Drive:** IIT Bombay / BITS Pilani 2024
- **Problem Summary:** The smallest number that can be expressed as the sum of two positive cubes in two different ways is $1729 = 1^3 + 12^3 = 9^3 + 10^3$. Find the $K$-th taxicab number or all pairs in a bounded range.
- **Approach:** Min-Heap storing triples $(i^3 + j^3, i, j)$ initialized with $(i^3 + (i+1)^3, i, i+1)$ for $1 \le i \le \sqrt[3]{N}$. Repeatedly pop and detect identical sums.
- **Complexity:** $O(K \log K)$ Time.

#### 3. Debugging Challenge: Iterator Invalidation in `std::vector`
- **College/Drive:** Tower C++ Systems Round 2024
- **Buggy Snippet:**
  ```cpp
  for (auto it = vec.begin(); it != vec.end(); ++it) {
      if (*it % 2 == 0) {
          vec.erase(it); // BUG: it is invalidated!
      }
  }
  ```
- **Fix:** Update iterator using return value of erase: `it = vec.erase(it);` or use modern C++20 erase-remove idiom: `std::erase_if(vec, [](int x) { return x % 2 == 0; });`.

#### 4. Sliding Window Maximum with Frequency Constraints
- **College/Drive:** IIT Madras / IIT Roorkee 2024
- **Problem Summary:** Find the maximum element in every sliding window of size $K$ such that no element in the window has a frequency $> 2$.
- **Approach:** Monotonic Decreasing Deque combined with a Hash Map / frequency counter tracking window counts.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 5. Shortest Distance After Road Additions (Dynamic Dijkstra / Floyd)
- **College/Drive:** Tower Research SWE Screening 2024
- **Problem Summary:** You are given $N$ cities numbered $0$ to $N-1$ connected in a line. Process $Q$ queries where each query adds a new unidirectional shortcut edge $(u, v)$ with weight 1. After each query, output the shortest distance from city 0 to city $N-1$.
- **LeetCode Equivalent:** [3243. Shortest Distance After Road Addition Queries I](https://leetcode.com/problems/shortest-distance-after-road-addition-queries-i/)
- **Approach:** BFS after each edge insertion or dynamic DP updates backward from $v$ to $0$.
- **Complexity:** $O(Q \cdot (V + E))$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Maximum Subarray Sum with Circular Array
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Find maximum subarray sum where array wraps around circularly.
- **LeetCode Equivalent:** [918. Maximum Sum Circular Subarray](https://leetcode.com/problems/maximum-sum-circular-subarray/)
- **Approach:** Kadane's algorithm for max subarray sum and min subarray sum; result is $\max(\text{max\_sum}, \text{total\_sum} - \text{min\_sum})$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Tree Path Queries with Edge Weights (LCA + Binary Lifting)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Compute maximum edge weight on path between two arbitrary tree nodes.
- **Approach:** Binary Lifting with $2^k$-ancestor table precomputation.
- **Complexity:** $O(N \log N)$ precomputation, $O(\log N)$ query.

#### 8. Smallest Range Covering Elements from K Lists
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Find smallest range that includes at least one number from each of the $K$ sorted lists.
- **LeetCode Equivalent:** [632. Smallest Range Covering Elements from K Lists](https://leetcode.com/problems/smallest-range-covering-elements-from-k-lists/)
- **Approach:** Min-Heap storing `(val, list_idx, elem_idx)` with running `max_val` tracker.
- **Complexity:** $O(N \log K)$ Time.

#### 9. Count Subarrays with Median K
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Find number of continuous subarrays whose median equals $K$.
- **LeetCode Equivalent:** [2448. Count Subarrays With Median K](https://leetcode.com/problems/count-subarrays-with-median-k/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Longest Increasing Path in a DAG
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Find longest weighted path in a directed acyclic graph.
- **Approach:** Kahn’s Topological Sort with DP relaxation.
- **Complexity:** $O(V + E)$ Time.

---

## 🧠 Frequent C++ & Systems MCQs in Tower Research OA
1. **`std::vector` Reallocation & Amortized Complexity:**
   - Why does `std::vector` grow by a factor of 1.5 or 2 instead of a fixed constant size (e.g. +100)?
   - *Answer:* Geometric expansion ensures that the amortized time complexity of `push_back` remains $O(1)$. Adding a fixed constant would result in $O(N^2)$ cumulative copying time over $N$ insertions.
2. **Memory Alignment & Cache Line False Sharing:**
   - How can you prevent false sharing between two adjacent atomic counters in C++?
   - *Answer:* Align each counter to a 64-byte boundary using `alignas(std::hardware_destructive_interference_size)` or `alignas(64)` to ensure they reside in separate L1 cache lines.
