# Uber Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🚗

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **CodeSignal** (General Coding Assessment - GCA Framework) / **HackerRank**
- **Test Structure & Duration:**
  - **CodeSignal GCA:** 4 Tasks in 70 minutes.
    - **Task 1 (Easy):** Basic implementation / String or Array manipulation.
    - **Task 2 (Easy-Medium):** Array / 2D Matrix traversal or simulation.
    - **Task 3 (Medium-Hard):** Business logic / Complex string manipulation / Hash table design.
    - **Task 4 (Hard):** Advanced sliding window, dynamic programming, or 2D matrix optimization.
- **Scoring & Cutoff:** CodeSignal calculates an automated score between **300 and 850**. Uber typically sets a strict interview threshold of **$\ge 820$** (passing virtually 100% of test cases with optimal time complexity across all 4 tasks).

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Matrix & 2D Grid Algorithms | Medium - Hard | Diagonal traversals, bounded rectangle counts, connected components |
| **Very High** | Sliding Window & Monotonic Deque | Hard | Window maximum/minimum, subsegment frequency matching |
| **High** | Intervals & Sweep Line | Medium - Hard | Overlapping intervals, meeting room scheduling, interval intersections |
| **High** | Graph Traversal (BFS / Dijkstra) | Medium - Hard | Shortest path with transfer penalties, bus routes, bipartite matching |
| **Medium** | Spatial / Tree Structures | Hard | QuadTree decomposition, Trie-based autocomplete |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Sliding Window Maximum / Bounded Stream Peak
- **Problem Summary:** You are given an array of integers `nums`, there is a sliding window of size `k` which is moving from the very left of the array to the very right. Return the max sliding window.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Approach:** Monotonic Decreasing Deque (`std::deque` in C++ / `collections.deque` in Python) storing indices.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

### 2. Bus Routes / Minimum Transfers
- **Problem Summary:** You are given an array `routes` representing bus routes where `routes[i]` is a bus route that the $i$-th bus repeats forever. Return the least number of buses you must take to travel from `source` to `target`.
- **LeetCode Equivalent:** [815. Bus Routes](https://leetcode.com/problems/bus-routes/)
- **Approach:** Breadth-First Search (BFS) over bus routes rather than bus stops to reduce graph nodes.
- **Complexity:** $O(\sum |routes[i]|)$.

### 3. Submatrix Full Match / Rectangle Pattern Count
- **Problem Summary:** Given a large matrix $A$ and a pattern matrix $B$. Find the number of submatrices in $A$ that match $B$ under rotational or numerical transformation rules.
- **Approach:** 2D sliding window hash (2D Rabin-Karp) or direct simulation with early exit.
- **Complexity:** $O(M \times N)$ Time.

### 4. Meeting Rooms II (Sweep Line / Min-Heap)
- **Problem Summary:** Given an array of meeting time intervals consisting of start and end times `[[s1,e1],[s2,e2],...]`, find the minimum number of conference rooms required.
- **LeetCode Equivalent:** [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- **Approach:** Separate start and end times, sort both arrays, use two pointers or a Min-Heap of active meeting end times.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

---

## 💡 CodeSignal Strategy for Uber
1. **Solve in order 1 $\to$ 2 $\to$ 4 $\to$ 3:** Task 4 is often purely algorithmic (e.g., sliding window, array logic) and quicker to implement if you know the pattern, whereas Task 3 often has tedious rules and heavy edge cases.
2. **Speed is scored:** The CodeSignal score factors in completion time. A candidate solving 4/4 in 40 minutes receives a higher score than one finishing in 69 minutes.
