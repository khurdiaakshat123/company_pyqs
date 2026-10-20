# Tower Research Capital Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) ⚡

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

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Advanced Graph Algorithms | Hard | Shortest path with transfer penalties, 0-1 BFS, Eulerian paths, DSU |
| **Very High** | C++ Code Debugging & STL Internals | Hard | Iterator invalidation, memory alignment, memory leaks, multithreading |
| **High** | Bit Manipulation & Number Theory | Hard | Bitmask DP, Taxicab numbers, modular inverse, prime factorization |
| **High** | Monotonic Deque & Sweepline | Hard | Sliding window extrema with dynamic updates, interval scheduling |
| **Medium** | Systems & Architecture MCQs | Medium - Hard | Cache line false sharing, atomic CAS, virtual memory page size |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Minimal Edge Weight Adjustment in Graph (0-1 BFS / Dijkstra)
- **Problem Summary:** Given a directed graph with $N$ vertices and $M$ edges. You want to travel from node 1 to node $N$. Some edges are directed in the wrong direction; reversing a directed edge costs 1 unit. Find the minimum cost to reach node $N$.
- **Approach:** 0-1 BFS: For each existing edge $u \to v$, assign weight 0. Add a reverse edge $v \to u$ with weight 1. Use a `std::deque`: push weight-0 transitions to the front, weight-1 transitions to the back.
- **Complexity:** $O(V + E)$ Time, $O(V)$ Space.

### 2. Taxicab Numbers / Sum of Two Cubes in Multiple Ways
- **Problem Summary:** The smallest number that can be expressed as the sum of two positive cubes in two different ways is $1729 = 1^3 + 12^3 = 9^3 + 10^3$. Find the $K$-th taxicab number or all pairs in a bounded range.
- **Approach:** Min-Heap storing triples $(i^3 + j^3, i, j)$ initialized with $(i^3 + (i+1)^3, i, i+1)$ for $1 \le i \le \sqrt[3]{N}$. Repeatedly pop and detect identical sums.
- **Complexity:** $O(K \log K)$ Time.

### 3. Debugging Challenge: Iterator Invalidation in `std::vector`
- **Buggy Snippet:**
  ```cpp
  for (auto it = vec.begin(); it != vec.end(); ++it) {
      if (*it % 2 == 0) {
          vec.erase(it); // BUG: it is invalidated!
      }
  }
  ```
- **Fix:** Update iterator using return value of erase: `it = vec.erase(it);` or use modern C++20 erase-remove idiom: `std::erase_if(vec, [](int x) { return x % 2 == 0; });`.

### 4. Sliding Window Maximum with Frequency Constraints
- **Problem Summary:** Find the maximum element in every sliding window of size $K$ such that no element in the window has a frequency $> 2$.
- **Approach:** Monotonic Decreasing Deque combined with a Hash Map / frequency counter tracking window counts.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.
