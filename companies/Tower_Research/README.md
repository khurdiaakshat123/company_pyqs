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
- **College/Drive:** IIT Delhi / IIT Kanpur Campus Drive 2024–2025
- **Problem Summary:** Given a directed graph with $N$ vertices and $M$ edges. You want to travel from node 1 to node $N$. Some edges are directed in the wrong direction; reversing a directed edge costs 1 unit. Find the minimum cost to reach node $N$.
- **Constraints:** $1 \le N \le 10^5$, $1 \le M \le 2 \times 10^5$.
- **Approach:** 0-1 BFS: For each existing edge $u \to v$, assign weight 0. Add a reverse edge $v \to u$ with weight 1. Use a `std::deque`: push weight-0 transitions to the front, weight-1 transitions to the back.
- **Complexity:** $O(V + E)$ Time, $O(V)$ Space.

#### 2. Taxicab Numbers (Dual Cube Representations)
- **College/Drive:** IIT Bombay / BITS Pilani 2024–2025
- **Problem Summary:** The smallest number that can be expressed as the sum of two positive cubes in two different ways is $1729 = 1^3 + 12^3 = 9^3 + 10^3$. Find the $K$-th taxicab number or all pairs in a bounded range.
- **Constraints:** $K \le 5000$.
- **Approach:** Min-Heap storing triples $(i^3 + j^3, i, j)$ initialized with $(i^3 + (i+1)^3, i, i+1)$ for $1 \le i \le \sqrt[3]{N}$. Repeatedly pop and detect identical sums.
- **Complexity:** $O(K \log K)$ Time.

#### 3. Debugging Challenge: Iterator Invalidation in `std::vector`
- **College/Drive:** Tower C++ Systems Round 2024–2025
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
- **College/Drive:** IIT Madras / IIT Roorkee 2024–2025
- **Problem Summary:** Find the maximum element in every sliding window of size $K$ such that no element in the window has a frequency $> 2$.
- **Constraints:** $1 \le nums.length \le 10^5$, $1 \le K \le nums.length$.
- **Approach:** Monotonic Decreasing Deque combined with a Hash Map / frequency counter tracking window counts.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 5. Shortest Distance After Road Additions (Dynamic BFS / DP)
- **College/Drive:** Tower Research SWE Screening 2024–2025
- **Problem Summary:** You are given $N$ cities numbered $0$ to $N-1$ connected in a line. Process $Q$ queries where each query adds a new unidirectional shortcut edge $(u, v)$ with weight 1. After each query, output the shortest distance from city 0 to city $N-1$.
- **Constraints:** $3 \le N \le 500$, $1 \le Q \le 500$.
- **LeetCode Equivalent:** [3243. Shortest Distance After Road Addition Queries I](https://leetcode.com/problems/shortest-distance-after-road-addition-queries-i/)
- **Approach:** BFS after each edge insertion or dynamic DP updates backward from $v$ to $0$.
- **Complexity:** $O(Q \cdot (V + E))$ Time.

#### 6. Find Minimum Cost Walk with Graph Queries
- **College/Drive:** IIT BHU / BITS Pilani 2024
- **Problem Summary:** Given an undirected weighted graph and a set of queries `[start, end]`, find the minimum cost of a walk from `start` to `end` where the cost of a walk is the bitwise AND of all edge weights in the walk.
- **Constraints:** $N \le 10^5$, $M \le 10^5$, $Q \le 10^5$.
- **LeetCode Equivalent:** [3108. Minimum Cost Walk in Weighted Graph](https://leetcode.com/problems/minimum-cost-walk-in-weighted-graph/)
- **Approach:** Disjoint Set Union (DSU). Compute the cumulative bitwise AND of all edge weights within each connected component. If `u` and `v` are in the same component, return component bitwise AND; otherwise -1.
- **Complexity:** $O(N + M + Q)$ Time, $O(N)$ Space.

#### 7. Count Distinct Substrings with Trie and Rolling Hash
- **College/Drive:** Tower Research Quant Dev 2024
- **Problem Summary:** Given a string $s$, return the number of distinct substrings of $s$.
- **Constraints:** $1 \le s.length \le 1000$.
- **LeetCode Equivalent:** [1698. Number of Distinct Substrings in a String](https://leetcode.com/problems/number-of-distinct-substrings-in-a-string/)
- **Approach:** Prefix Trie insertion counting newly allocated nodes or 2D Rabin-Karp polynomial rolling hash pairs.
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

#### 8. Longest Subarray with At Most Two Distinct Elements
- **College/Drive:** IIT Kharagpur 2024
- **Problem Summary:** Given an integer array `nums`, find the length of the longest continuous subarray that contains at most two distinct integers.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [159. Longest Substring with At Most Two Distinct Characters](https://leetcode.com/problems/longest-substring-with-at-most-two-distinct-characters/)
- **Approach:** Sliding window with hash map storing element frequencies. Shrink left pointer when map size exceeds 2.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Parallel Job Execution with Precedence & Limited Cores
- **College/Drive:** Systems Infrastructure 2024
- **Problem Summary:** Given $N$ tasks with execution times, precedence DAG constraints, and $P$ available CPU cores, find the minimum time to complete all tasks.
- **Constraints:** $N \le 16$, $P \le 4$.
- **Approach:** Bitmask Dynamic Programming over sets of completed tasks, finding independent subsets of tasks ready to run concurrently.
- **Complexity:** $O(3^N)$ Time, $O(2^N)$ Space.

#### 10. Number of Atoms / Chemical Formula Parser
- **College/Drive:** Tower Off-Campus 2024
- **Problem Summary:** Given a chemical formula string like `"K4(ON(SO3)2)2"`, return the count of all atoms sorted in alphabetical order.
- **Constraints:** $1 \le formula.length \le 1000$.
- **LeetCode Equivalent:** [726. Number of Atoms](https://leetcode.com/problems/number-of-atoms/)
- **Approach:** Stack of Hash Maps. Push a new empty map upon encountering `'('`. On `')'`, pop top map, multiply all counts by following integer multiplier, and merge into preceding map.
- **Complexity:** $O(N^2)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Maximum Subarray Sum with Circular Array
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Find maximum subarray sum where array wraps around circularly.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [918. Maximum Sum Circular Subarray](https://leetcode.com/problems/maximum-sum-circular-subarray/)
- **Approach:** Kadane's algorithm for max subarray sum and min subarray sum; result is $\max(\text{max\_sum}, \text{total\_sum} - \text{min\_sum})$ (handling all-negative case).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Tree Path Queries with Edge Weights (LCA + Binary Lifting)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Compute maximum edge weight on path between two arbitrary tree nodes.
- **Constraints:** $N, Q \le 10^5$.
- **Approach:** Binary Lifting with $2^k$-ancestor table precomputation.
- **Complexity:** $O(N \log N)$ precomputation, $O(\log N)$ query.

#### 13. Smallest Range Covering Elements from K Lists
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Find smallest range that includes at least one number from each of the $K$ sorted lists.
- **Constraints:** $1 \le k \le 3500$, total numbers $\le 2 \times 10^4$.
- **LeetCode Equivalent:** [632. Smallest Range Covering Elements from K Lists](https://leetcode.com/problems/smallest-range-covering-elements-from-k-lists/)
- **Approach:** Min-Heap storing `(val, list_idx, elem_idx)` with running `max_val` tracker.
- **Complexity:** $O(N \log K)$ Time, $O(K)$ Space.

#### 14. Count Subarrays with Median K
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Find number of continuous subarrays whose median equals $K$.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [2448. Count Subarrays With Median K](https://leetcode.com/problems/count-subarrays-with-median-k/)
- **Approach:** Transform array elements to $+1$ (if $> K$), $-1$ (if $< K$), and $0$ (if $= K$). Prefix sum balance hash map across index of $K$.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 15. Longest Increasing Path in a DAG
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Find longest weighted path in a directed acyclic graph.
- **Constraints:** $V \le 10^5, E \le 2 \times 10^5$.
- **Approach:** Kahn’s Topological Sort with DP relaxation.
- **Complexity:** $O(V + E)$ Time.

#### 16. Find the Duplicate Number in $O(1)$ Space
- **College/Drive:** Tower Research Technical Slot 2023
- **Problem Summary:** Given an array of integers `nums` containing $n + 1$ integers where each integer is in range $[1, n]$, find duplicate number without modifying array and using $O(1)$ extra space.
- **Constraints:** $1 \le n \le 10^5$.
- **LeetCode Equivalent:** [287. Find the Duplicate Number](https://leetcode.com/problems/find-the-duplicate-number/)
- **Approach:** Floyd's Cycle-Finding Algorithm (Tortoise and Hare) viewing array indices as next pointers in a linked list.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 17. Design Underground Railway System
- **College/Drive:** Tower SWE Slot 2023
- **Problem Summary:** Design a system tracking passenger check-ins and check-outs to calculate average travel time between pairs of stations.
- **Constraints:** Up to $2 \times 10^4$ operations.
- **LeetCode Equivalent:** [1396. Design Underground System](https://leetcode.com/problems/design-underground-system/)
- **Approach:** Two Hash Maps: `checkInMap[id] = (station, time)` and `routeMap[stationA + "->" + stationB] = (total_time, trip_count)`.
- **Complexity:** $O(1)$ Time per operation.

#### 18. Minimum Window Substring
- **College/Drive:** Off-Campus Screening 2023
- **Problem Summary:** Find minimum window substring of $s$ that contains all characters of $t$.
- **Constraints:** $1 \le |s|, |t| \le 10^5$.
- **LeetCode Equivalent:** [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- **Approach:** Sliding window with character counts.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 19. Subarray with Bitwise AND Equal to K
- **College/Drive:** Advanced Algo Round 2023
- **Problem Summary:** Count total number of subarrays whose bitwise AND equals $K$.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **Approach:** Monotonic logarithmic bitwise AND property: for any fixed right endpoint, there are at most $\approx 30$ distinct bitwise AND values. Maintain list of `(and_val, count)` and merge backwards.
- **Complexity:** $O(N \log(\max A))$ Time, $O(\log(\max A))$ Space.

#### 20. Burst Balloons (Interval Dynamic Programming)
- **College/Drive:** IIT Delhi Slot 2023
- **Problem Summary:** Given $n$ balloons with coins. If you burst balloon $i$, you get `nums[i-1] * nums[i] * nums[i+1]` coins. Maximize total coins collected.
- **Constraints:** $1 \le n \le 300$.
- **LeetCode Equivalent:** [312. Burst Balloons](https://leetcode.com/problems/burst-balloons/)
- **Approach:** Interval DP: `dp[i][j]` represents max coins from bursting all balloons between $i$ and $j$. Pick the *last* balloon $k$ to burst in $(i, j)$: `dp[i][j] = max(dp[i][k] + dp[k][j] + nums[i]*nums[k]*nums[j])`.
- **Complexity:** $O(N^3)$ Time, $O(N^2)$ Space.

---

## 🧠 Frequent C++ & Systems MCQs in Tower Research OA
1. **`std::vector` Reallocation & Amortized Complexity:**
   - Why does `std::vector` grow by a factor of 1.5 or 2 instead of a fixed constant size (e.g. +100)?
   - *Answer:* Geometric expansion ensures that the amortized time complexity of `push_back` remains $O(1)$. Adding a fixed constant would result in $O(N^2)$ cumulative copying time over $N$ insertions.
2. **Memory Alignment & Cache Line False Sharing:**
   - How can you prevent false sharing between two adjacent atomic counters in C++?
   - *Answer:* Align each counter to a 64-byte boundary using `alignas(std::hardware_destructive_interference_size)` or `alignas(64)` to ensure they reside in separate L1 cache lines.
3. **Branch Prediction Hints (`[[likely]]` / `[[unlikely]]`):**
   - How do C++20 branch prediction attributes affect machine code generation?
   - *Answer:* They allow the compiler to reorder basic blocks such that the likely code path is placed in sequential instruction stream (fallthrough), maximizing instruction cache utilization and minimizing CPU pipeline flushes.
