# IMC Trading Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) ⚡

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** (SWE Track) / **BrainsFirst / NeurOlympics** (Trader Track)
- **Hiring Tracks & Durations:**
  1. **Software Engineering (SWE):** 90 to 120 minutes.
     - 2 Algorithmic Coding Problems (LeetCode Medium to Hard).
     - 10 to 15 Core CS MCQs (Operating Systems, Concurrency/Multithreading, Memory Management, C++ Internals, Network Sockets).
     - Automated Video Interview (1–2 behavioral questions via HireVue/HackerRank).
  2. **Quantitative Trader / Research Track:** Fast-paced mental math, probability distributions, market-making simulations, and gamified cognitive reaction games.
- **Passing Benchmark:** Flawless execution on both coding questions (100% test cases) + top percentile score on systems/multithreading MCQs.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Custom Data Structure Design:** Efficient point/range updates, frequency counters, order book engines, LRU cache with TTL.
- **Grid Traversals & Coordinate Search:** Multi-source BFS, underground obstacle navigation, shortest path matrices with battery/fuel limits.
- **Streaming Data & Greedy Simulation:** Transaction logs, priority order processing, sliding window rates, interval scheduling.
- **Multithreading & Systems MCQs:** Deadlock conditions, race conditions, atomic operations, cache invalidation, TCP vs UDP in financial feeds.
- **Graph Reachability:** Shortest path with transfers, cycle detection in financial flows, Eulerian paths.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Underground Cavern Exploration (Grid 3D BFS Simulation)
- **College/Drive:** IIT Bombay / IIT Delhi Campus Hiring 2024–2025
- **Problem Summary:** A robot explores an $N \times M$ underground cavern to collect minerals. Rocks and lava obstruct certain tiles. The robot starts with battery $B$. Moving consumes 1 battery; picking a mineral takes 0 battery. Return the maximum minerals reachable before battery drains to 0.
- **Constraints:** $N, M \le 50$, $B \le 100$.
- **Approach:** 3D BFS tracking state `(row, col, battery_remaining)` with a visited 3D boolean array.
- **Complexity:** $O(N \times M \times B)$ Time, $O(N \times M \times B)$ Space.

#### 2. Matching Order Book Engine Simulation
- **College/Drive:** IIT Madras / BITS Pilani 2024–2025
- **Problem Summary:** Design a simplified continuous limit order book (CLOB). Support operations `BUY(price, qty)` and `SELL(price, qty)`. When an incoming buy order price $\ge$ best sell order, execute trades at the maker price. Output total executed volume and remaining book state.
- **Constraints:** Up to $10^5$ orders.
- **Approach:** Two Priority Queues: Max-Heap for Buy orders, Min-Heap for Sell orders, with price-time priority matching.
- **Complexity:** $O(N \log N)$ Time.

#### 3. Range Frequency Query Data Structure
- **College/Drive:** IIT Roorkee / IIT Kharagpur 2024–2025
- **Problem Summary:** Design a data structure to find the frequency of a given value in a subsegment of an array `[left, right]` in logarithmic time.
- **Constraints:** Array size $\le 10^5$, queries $\le 10^5$.
- **LeetCode Equivalent:** [2080. Range Frequency Queries](https://leetcode.com/problems/range-frequency-queries/)
- **Approach:** Hash Map mapping `value -> sorted vector of indices`. Use `std::upper_bound` and `std::lower_bound` on the index vector.
- **Complexity:** $O(\log K)$ per query where $K$ is frequency of value.

#### 4. Shortest Path in a Grid with Obstacles Elimination
- **College/Drive:** Off-Campus SWE Drive 2024–2025
- **Problem Summary:** Given an $M \times N$ grid, find the minimum steps to walk from $(0, 0)$ to $(M-1, N-1)$ given you can eliminate at most $k$ obstacles.
- **Constraints:** $1 \le M, N \le 40$, $1 \le k \le M \times N$.
- **LeetCode Equivalent:** [1293. Shortest Path in a Grid with Obstacles Elimination](https://leetcode.com/problems/shortest-path-in-a-grid-with-obstacles-elimination/)
- **Approach:** BFS state `(r, c, eliminated_count)` storing minimum obstacles eliminated to reach each cell.
- **Complexity:** $O(M \times N \times K)$ Time, $O(M \times N \times K)$ Space.

#### 5. Maximum Profit in Job Scheduling
- **College/Drive:** Campus Drive 2024–2025
- **Problem Summary:** Given $N$ jobs with `startTime`, `endTime`, and `profit`, find the maximum profit you can achieve such that no two jobs overlap.
- **Constraints:** $1 \le N \le 5 \times 10^4$.
- **LeetCode Equivalent:** [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)
- **Approach:** Sort jobs by `endTime`. DP with Binary Search (`std::upper_bound` on `startTime`) to find the latest non-conflicting job.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 6. Minimum Number of Taps to Open to Water a Garden
- **College/Drive:** IIT Kanpur / IIT BHU 2024
- **Problem Summary:** There is a 1D garden of length $n$. Given $n+1$ taps with coverage radius `ranges[i]`, determine the minimum number of taps to open to water the entire garden $[0, n]$, or -1 if impossible.
- **Constraints:** $1 \le n \le 10^4$, $0 \le ranges[i] \le 100$.
- **LeetCode Equivalent:** [1326. Minimum Number of Taps to Open to Water a Garden](https://leetcode.com/problems/minimum-number-of-taps-to-open-to-water-a-garden/)
- **Approach:** Convert each tap to an interval $[ \max(0, i - ranges[i]), \min(n, i + ranges[i]) ]$. Apply Jump Game II greedy interval leapfrogging tracking `curr_end` and `farthest_reach`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Course Schedule IV (Prerequisite Reachability)
- **College/Drive:** IMC Amsterdam / Sydney Campus 2024
- **Problem Summary:** Given $N$ courses and prerequisite pairs, answer $Q$ queries asking whether course $u$ is a prerequisite of course $v$.
- **Constraints:** $N \le 100$, $Q \le 10^4$.
- **LeetCode Equivalent:** [1462. Course Schedule IV](https://leetcode.com/problems/course-schedule-iv/)
- **Approach:** Transitive closure using Floyd-Warshall on boolean reachability matrix `isPrereq[i][j] = isPrereq[i][j] || (isPrereq[i][k] && isPrereq[k][j])`.
- **Complexity:** $O(N^3)$ preprocessing, $O(1)$ query time.

#### 8. Longest Consecutive Sequence in $O(N)$
- **College/Drive:** IIT Delhi Slot 2024
- **Problem Summary:** Given an unsorted array of integers `nums`, return the length of the longest consecutive elements sequence in $O(N)$ time.
- **Constraints:** $0 \le nums.length \le 10^5$, $-10^9 \le nums[i] \le 10^9$.
- **LeetCode Equivalent:** [128. Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/)
- **Approach:** Insert all numbers into an `unordered_set`. Only initiate count expansion if `num - 1` is NOT in the set (guaranteeing each sequence is traversed only once).
- **Complexity:** $O(N)$ average Time, $O(N)$ Space.

#### 9. Reconstruct Itinerary (Hierholzer's Eulerian Path)
- **College/Drive:** Off-Campus SWE Drive 2024
- **Problem Summary:** Given a list of airline tickets represented by pairs of departure and arrival airports `[from, to]`, reconstruct the itinerary in order that uses all tickets, breaking ties lexicographically.
- **Constraints:** $1 \le tickets.length \le 300$.
- **LeetCode Equivalent:** [332. Reconstruct Itinerary](https://leetcode.com/problems/reconstruct-itinerary/)
- **Approach:** Hierholzer's Algorithm for Eulerian path using adjacency list with `std::multiset` or priority queues. Post-order DFS and reverse list.
- **Complexity:** $O(E \log E)$ Time, $O(V + E)$ Space.

#### 10. Swim in Rising Water
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** In an $N \times N$ grid where elevation at $(r, c)$ is $grid[r][c]$, rain falls continuously. You can swim from a square to any 4-directionally adjacent square if elevation of both is at most $t$. Find least time $t$ to reach $(N-1, N-1)$.
- **Constraints:** $N \le 50$.
- **LeetCode Equivalent:** [778. Swim in Rising Water](https://leetcode.com/problems/swim-in-rising-water/)
- **Approach:** Modified Dijkstra / Min-Heap prioritizing lowest water elevation, or Binary Search on time $T$ combined with BFS/DFS reachability.
- **Complexity:** $O(N^2 \log N)$ Time, $O(N^2)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Sliding Window Median / Stream Processing
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Median of elements in sliding window of size $k$.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [480. Sliding Window Median](https://leetcode.com/problems/sliding-window-median/)
- **Approach:** Dual balanced heaps (Max-Heap + Min-Heap) with hash map lazy deletion.
- **Complexity:** $O(N \log K)$ Time.

#### 12. Rotting Oranges / Multi-Source BFS
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Minimum minutes until no fresh orange remains in grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS starting from all rotten oranges simultaneously.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 13. Bus Routes / Multi-Stop Graph BFS
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Find least number of buses you must take to travel from source to target.
- **Constraints:** $1 \le routes.length \le 500$, total stops $\le 10^5$.
- **LeetCode Equivalent:** [815. Bus Routes](https://leetcode.com/problems/bus-routes/)
- **Approach:** BFS on bipartite graph of stops and bus routes.
- **Complexity:** $O(\sum \text{route lengths})$ Time.

#### 14. LRU Cache with Millisecond TTL
- **College/Drive:** Systems Screening 2023
- **Problem Summary:** Design LRU Cache where entries expire after a time-to-live (TTL).
- **Constraints:** $10^5$ operations.
- **Approach:** Hash Map + Doubly Linked List with Min-Heap tracking expiration timestamps.
- **Complexity:** $O(1)$ amortized `get`/`put`, $O(\log N)$ periodic expiration cleanup.

#### 15. Trapping Rain Water II (3D Grid)
- **College/Drive:** Advanced SWE Slot 2023
- **Problem Summary:** Given an $M \times N$ integer matrix representing height of each unit cell, compute volume of water it can trap after rain.
- **Constraints:** $1 \le M, N \le 200$.
- **LeetCode Equivalent:** [407. Trapping Rain Water II](https://leetcode.com/problems/trapping-rain-water-ii/)
- **Approach:** Min-Heap Priority Queue starting with all boundary cells. Greedily expand lowest boundary inward.
- **Complexity:** $O(M \cdot N \log(M \cdot N))$ Time.

#### 16. Find All Anagrams in a String
- **College/Drive:** Campus Slot 3 (2023)
- **Problem Summary:** Given two strings `s` and `p`, return an array of all the start indices of `p`'s anagrams in `s`.
- **Constraints:** $1 \le s.length, p.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [438. Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string/)
- **Approach:** Fixed-size sliding window of length $|p|$ tracking character frequency array difference.
- **Complexity:** $O(N)$ Time, $O(1)$ Space (alphabet size 26).

#### 17. Word Search II (Trie + 2D Backtracking)
- **College/Drive:** IIT Roorkee Slot 2023
- **Problem Summary:** Given an $M \times N$ board of characters and a list of strings `words`, return all words on the board.
- **Constraints:** $M, N \le 12$, $words.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [212. Word Search II](https://leetcode.com/problems/word-search-ii/)
- **Approach:** Build Prefix Trie from dictionary words. Run DFS on 2D board with Trie traversal, pruning visited branches immediately.
- **Complexity:** $O(M \cdot N \cdot 4^L)$ Time where $L$ is max word length.

#### 18. Alien Dictionary
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Derive alphabet order from a lexicographically sorted dictionary in an alien language.
- **Constraints:** Words length $\le 100$.
- **LeetCode Equivalent:** [269. Alien Dictionary](https://leetcode.com/problems/alien-dictionary/)
- **Approach:** Directed graph of character edges + Topological Sort with Kahn's algorithm or DFS cycle check.
- **Complexity:** $O(C)$ Time, $O(1)$ Space.

#### 19. Task Scheduler with Cooldown
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Given a characters array `tasks` and a cooling interval `n`, find minimum number of CPU intervals to finish all tasks.
- **Constraints:** $1 \le tasks.length \le 10^4$, $0 \le n \le 100$.
- **LeetCode Equivalent:** [621. Task Scheduler](https://leetcode.com/problems/task-scheduler/)
- **Approach:** Greedy math formula based on maximum frequency character: `(max_freq - 1) * (n + 1) + count_max_freq`, bounded below by total tasks.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 20. Evaluate Division (Weighted Graph Reachability)
- **College/Drive:** IMC SWE Slot 2023
- **Problem Summary:** Given variable pairs and quotient values $A / B = 2.0$, evaluate queries $C / D$.
- **Constraints:** $1 \le equations.length \le 20$.
- **LeetCode Equivalent:** [399. Evaluate Division](https://leetcode.com/problems/evaluate-division/)
- **Approach:** Graph representation where edge $(u, v)$ has weight $w = u/v$ and $(v, u)$ has weight $1/w$. DFS traversal computing path weight products.
- **Complexity:** $O(Q \times (V + E))$ Time, $O(V + E)$ Space.

---

## 🧠 Frequent C++ & Systems MCQs Asked in IMC OA
1. **Memory Ordering in Multi-Threaded Trading:**
   - Why is `std::memory_order_acquire` paired with `std::memory_order_release`?
   - *Answer:* It guarantees that all memory writes before the release store in thread A are visible to thread B after its acquire load, establishing a happens-before relationship without a full memory barrier.
2. **TCP vs UDP in Low-Latency Data Feeds:**
   - Why do financial market exchanges distribute quote data via UDP Multicast rather than TCP?
   - *Answer:* UDP eliminates TCP connection handshake, ACK traffic, head-of-line blocking, and retransmission delays, allowing sub-microsecond multicast broadcasting to hundreds of subscribers simultaneously.
3. **Deadlock Conditions (Coffman Conditions):**
   - What four conditions must hold simultaneously for a deadlock to occur?
   - *Answer:* Mutual Exclusion, Hold and Wait, No Preemption, and Circular Wait. Breaking any one condition prevents deadlocks.
