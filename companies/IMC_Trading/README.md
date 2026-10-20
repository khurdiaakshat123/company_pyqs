# IMC Trading Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) ⚡

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** (SWE Track) / **BrainsFirst / NeurOlympics** (Trader Track)
- **Hiring Tracks & Durations:**
  1. **Software Engineering (SWE):** 90 to 120 minutes.
     - 2 Algorithmic Coding Problems (LeetCode Medium to Hard).
     - 10 to 15 Core CS MCQs (Operating Systems, Concurrency/Multithreading, Memory Management, Algorithm Complexities).
     - Automated Video Interview (1–2 behavioral questions via HireVue/HackerRank).
  2. **Quantitative Trader / Research:** Rapid mental arithmetic, probability & statistical distributions, and gamified cognitive reaction games.
- **Passing Benchmark:** Flawless execution on both coding questions + top percentile score on systems/multithreading MCQs.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Custom Data Structure Design | Medium - Hard | Efficient point/range updates, frequency counters, order book simulations |
| **Very High** | Grid Traversals & Coordinate Search | Medium - Hard | Multi-source BFS, underground obstacle navigation, shortest path matrices |
| **High** | Streaming Data & Greedy Simulation | Medium - Hard | Transaction logs, priority order processing, sliding window rates |
| **High** | Multithreading & Systems MCQs | Medium | Deadlock conditions, race conditions, atomic operations, cache invalidation |
| **Medium** | Graph Reachability | Medium | Connected components, cycle detection in financial flows |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Underground Artifact Exploration (Grid BFS Simulation)
- **Problem Summary:** A robot explores an $N \times M$ underground cavern to collect minerals. Rocks and lava obstruct certain tiles. The robot starts with battery $B$. Moving consumes 1 battery; picking a mineral takes 0 battery. Return the maximum minerals reachable before battery drains to 0.
- **Approach:** BFS tracking state `(row, col, battery_remaining)` with a 3D visited boolean array.
- **Complexity:** $O(N \times M \times B)$ Time, $O(N \times M \times B)$ Space.

### 2. Matching Order Book Engine Simulation
- **Problem Summary:** Design a simplified continuous limit order book (CLOB). Support operations `BUY(price, qty)` and `SELL(price, qty)`. When an incoming buy order price $\ge$ best sell order, execute trades at the maker price. Output total executed volume and remaining book state.
- **Approach:** Two Priority Queues: Max-Heap for Buy orders, Min-Heap for Sell orders.
- **Complexity:** $O(N \log N)$ Time.

### 3. Range Frequency Query Data Structure
- **Problem Summary:** Design a data structure to find the frequency of a given value in a subsegment of an array `[left, right]` in logarithmic time.
- **LeetCode Equivalent:** [2080. Range Frequency Queries](https://leetcode.com/problems/range-frequency-queries/)
- **Approach:** Hash Map mapping `value -> sorted list of indices`. Use `std::upper_bound` and `std::lower_bound` on the index list.
- **Complexity:** $O(\log K)$ per query where $K$ is frequency of value.

### 4. Sliding Window Median / Stream Processing
- **Problem Summary:** Given an array of integers and a sliding window of size $k$, calculate the median of the current window for each step as the window slides from left to right.
- **LeetCode Equivalent:** [480. Sliding Window Median](https://leetcode.com/problems/sliding-window-median/)
- **Approach:** Two Heaps (Max-Heap for lower half, Min-Heap for upper half) with lazy removal, or multiset in C++.
- **Complexity:** $O(N \log K)$ Time.
