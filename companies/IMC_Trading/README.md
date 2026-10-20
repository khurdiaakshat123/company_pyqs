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
- **Graph Reachability:** Shortest path with transfers, cycle detection in financial flows.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Underground Cavern Exploration (Grid 3D BFS Simulation)
- **College/Drive:** IIT Bombay / IIT Delhi Campus Hiring 2024
- **Problem Summary:** A robot explores an $N \times M$ underground cavern to collect minerals. Rocks and lava obstruct certain tiles. The robot starts with battery $B$. Moving consumes 1 battery; picking a mineral takes 0 battery. Return the maximum minerals reachable before battery drains to 0.
- **Approach:** 3D BFS tracking state `(row, col, battery_remaining)` with a visited 3D boolean array.
- **Complexity:** $O(N \times M \times B)$ Time, $O(N \times M \times B)$ Space.

#### 2. Matching Order Book Engine Simulation
- **College/Drive:** IIT Madras / BITS Pilani 2024
- **Problem Summary:** Design a simplified continuous limit order book (CLOB). Support operations `BUY(price, qty)` and `SELL(price, qty)`. When an incoming buy order price $\ge$ best sell order, execute trades at the maker price. Output total executed volume and remaining book state.
- **Approach:** Two Priority Queues: Max-Heap for Buy orders, Min-Heap for Sell orders.
- **Complexity:** $O(N \log N)$ Time.

#### 3. Range Frequency Query Data Structure
- **College/Drive:** IIT Roorkee / IIT Kharagpur 2024
- **Problem Summary:** Design a data structure to find the frequency of a given value in a subsegment of an array `[left, right]` in logarithmic time.
- **LeetCode Equivalent:** [2080. Range Frequency Queries](https://leetcode.com/problems/range-frequency-queries/)
- **Approach:** Hash Map mapping `value -> sorted vector of indices`. Use `std::upper_bound` and `std::lower_bound` on the index vector.
- **Complexity:** $O(\log K)$ per query where $K$ is frequency of value.

#### 4. Shortest Path in a Grid with Obstacles Elimination
- **College/Drive:** Off-Campus SWE Drive 2024
- **Problem Summary:** Given an $M \times N$ grid, find the minimum steps to walk from $(0, 0)$ to $(M-1, N-1)$ given you can eliminate at most $k$ obstacles.
- **LeetCode Equivalent:** [1293. Shortest Path in a Grid with Obstacles Elimination](https://leetcode.com/problems/shortest-path-in-a-grid-with-obstacles-elimination/)
- **Approach:** BFS state `(r, c, eliminated_count)` storing minimum obstacles eliminated to reach each cell.
- **Complexity:** $O(M \times N \times K)$ Time, $O(M \times N \times K)$ Space.

#### 5. Maximum Profit in Job Scheduling
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Given $N$ jobs with `startTime`, `endTime`, and `profit`, find the maximum profit you can achieve such that no two jobs overlap.
- **LeetCode Equivalent:** [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)
- **Approach:** Sort jobs by `endTime`. DP with Binary Search (`std::upper_bound` on `startTime`) to find the latest non-conflicting job.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Sliding Window Median / Stream Processing
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Median of elements in sliding window of size $k$.
- **LeetCode Equivalent:** [480. Sliding Window Median](https://leetcode.com/problems/sliding-window-median/)
- **Approach:** Dual balanced heaps (Max-Heap + Min-Heap) with hash map lazy deletion.
- **Complexity:** $O(N \log K)$ Time.

#### 7. Rotting Oranges / Multi-Source BFS
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Minimum minutes until no fresh orange remains in grid.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS starting from all rotten oranges simultaneously.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 8. Bus Routes / Multi-Stop Graph BFS
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Find least number of buses you must take to travel from source to target.
- **LeetCode Equivalent:** [815. Bus Routes](https://leetcode.com/problems/bus-routes/)
- **Approach:** BFS on bipartite graph of stops and bus routes.
- **Complexity:** $O(\sum \text{route lengths})$ Time.

#### 9. LRU Cache with Millisecond TTL
- **College/Drive:** Systems Screening 2023
- **Problem Summary:** Design LRU Cache where entries expire after a time-to-live (TTL).
- **Approach:** Hash Map + Doubly Linked List with Min-Heap tracking expiration timestamps.
- **Complexity:** $O(1)$ amortized `get`/`put`, $O(\log N)$ periodic expiration cleanup.

#### 10. Trapping Rain Water II (3D Grid)
- **College/Drive:** Advanced SWE Slot 2023
- **Problem Summary:** Given an $M \times N$ integer matrix representing height of each unit cell, compute volume of water it can trap after rain.
- **LeetCode Equivalent:** [407. Trapping Rain Water II](https://leetcode.com/problems/trapping-rain-water-ii/)
- **Approach:** Min-Heap Priority Queue starting with all boundary cells. Greedily expand lowest boundary inward.
- **Complexity:** $O(M \cdot N \log(M \cdot N))$ Time.

---

## 🧠 Frequent C++ & Systems MCQs Asked in IMC OA
1. **Memory Ordering in Multi-Threaded Trading:**
   - Why is `std::memory_order_acquire` paired with `std::memory_order_release`?
   - *Answer:* It guarantees that all memory writes before the release store in thread A are visible to thread B after its acquire load, establishing a happens-before relationship without a full memory barrier.
2. **TCP vs UDP in Low-Latency Data Feeds:**
   - Why do financial market exchanges distribute quote data via UDP Multicast rather than TCP?
   - *Answer:* UDP eliminates TCP connection handshake, ACK traffic, head-of-line blocking, and retransmission delays, allowing sub-microsecond multicast broadcasting to hundreds of subscribers simultaneously.
