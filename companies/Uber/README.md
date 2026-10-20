# Uber Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🚗

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

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Matrix & 2D Grid Algorithms:** Diagonal traversals, bounded rectangle counts, connected components.
- **Sliding Window & Monotonic Deque:** Window maximum/minimum, subsegment frequency matching.
- **Intervals & Sweep Line:** Overlapping intervals, meeting room scheduling, interval intersections.
- **Graph Traversal (BFS / Dijkstra):** Shortest path with transfer penalties, bus routes, bipartite matching.
- **Spatial / Tree Structures:** QuadTree decomposition, Trie-based autocomplete.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Sliding Window Maximum / Bounded Stream Peak
- **College/Drive:** IIT Roorkee / IIT BHU 2024
- **Problem Summary:** You are given an array of integers `nums`, there is a sliding window of size `k` which is moving from the very left of the array to the very right. Return the max sliding window.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Approach:** Monotonic Decreasing Deque (`std::deque` in C++ / `collections.deque` in Python) storing indices.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 2. Bus Routes / Minimum Transfers
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** You are given an array `routes` representing bus routes where `routes[i]` is a bus route that the $i$-th bus repeats forever. Return the least number of buses you must take to travel from `source` to `target`.
- **LeetCode Equivalent:** [815. Bus Routes](https://leetcode.com/problems/bus-routes/)
- **Approach:** Breadth-First Search (BFS) over bus routes rather than bus stops to reduce graph nodes.
- **Complexity:** $O(\sum |routes[i]|)$.

#### 3. Submatrix Full Match / Rectangle Pattern Count
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Summary:** Given a large matrix $A$ and a pattern matrix $B$. Find the number of submatrices in $A$ that match $B$ under rotational or numerical transformation rules.
- **Approach:** 2D sliding window hash (2D Rabin-Karp) or direct simulation with early exit.
- **Complexity:** $O(M \times N)$ Time.

#### 4. Meeting Rooms II (Sweep Line / Min-Heap)
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Summary:** Given an array of meeting time intervals consisting of start and end times `[[s1,e1],[s2,e2],...]`, find the minimum number of conference rooms required.
- **LeetCode Equivalent:** [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- **Approach:** Separate start and end times, sort both arrays, use two pointers or a Min-Heap of active meeting end times.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 5. Shortest Path Visiting All Nodes / Driver Route Coverage
- **College/Drive:** Uber HackTag / Campus 2024
- **Problem Summary:** An Uber driver needs to visit all $N$ client pickup locations in a city graph ($N \le 12$). Return the length of the shortest path that visits every node.
- **LeetCode Equivalent:** [847. Shortest Path Visiting All Nodes](https://leetcode.com/problems/shortest-path-visiting-all-nodes/)
- **Approach:** BFS with Bitmask State: Queue stores `(node, mask)` where `mask` is a bitmask of visited nodes.
- **Complexity:** $O(N^2 \cdot 2^N)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Word Ladder I (BFS Shortest Transformation)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Shortest transformation path between start and end words.
- **LeetCode Equivalent:** [127. Word Ladder](https://leetcode.com/problems/word-ladder/)
- **Complexity:** $O(M^2 \times N)$ Time.

#### 7. Construct Quad Tree (Spatial Grid Partition)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Partition $N \times N$ matrix into Quad Tree recursively.
- **LeetCode Equivalent:** [427. Construct Quad Tree](https://leetcode.com/problems/construct-quad-tree/)
- **Complexity:** $O(N^2)$ Time.

#### 8. Design Search Autocomplete System (Trie + Min-Heap)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Return top 3 historical search sentences matching prefix.
- **LeetCode Equivalent:** [642. Design Search Autocomplete System](https://leetcode.com/problems/design-search-autocomplete-system/)
- **Complexity:** $O(L)$ per character.

#### 9. Alien Dictionary (Topological Sort)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Find character order in dictionary words using DAG.
- **LeetCode Equivalent:** [269. Alien Dictionary](https://leetcode.com/problems/alien-dictionary/)
- **Complexity:** $O(C)$ Time.

#### 10. Trapping Rain Water
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Calculate trapped rain water between vertical columns.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time.

---

## 💡 CodeSignal Strategy for Uber
1. **Solve in order 1 $\to$ 2 $\to$ 4 $\to$ 3:** Task 4 is often purely algorithmic (e.g., sliding window, array logic) and quicker to implement if you know the pattern, whereas Task 3 often has tedious rules and heavy edge cases.
2. **Speed is scored:** The CodeSignal score factors in completion time. A candidate solving 4/4 in 40 minutes receives a higher score than one finishing in 69 minutes.
