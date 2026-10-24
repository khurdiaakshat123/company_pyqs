# Uber Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🚗

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **CodeSignal** (General Coding Assessment - GCA Framework) / **HackerRank**
- **Test Structure & Duration:**
  - **CodeSignal GCA:** 4 Tasks in 70 minutes.
    - **Task 1 (Easy):** Basic implementation / String or Array manipulation.
    - **Task 2 (Easy-Medium):** Array / 2D Matrix traversal or simulation.
    - **Task 3 (Medium-Hard):** Business logic / Complex string manipulation / Hash table design / Text editor simulation.
    - **Task 4 (Hard):** Advanced sliding window, dynamic programming, or 2D matrix optimization.
- **Scoring & Cutoff:** CodeSignal calculates an automated score between **300 and 850**. Uber typically sets a strict interview threshold of **$\ge 820$** (passing virtually 100% of test cases with optimal time complexity across all 4 tasks).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Matrix & 2D Grid Algorithms:** Diagonal traversals, bounded rectangle counts, QuadTree spatial decomposition, grid DP with transitions.
- **Sliding Window & Monotonic Deque:** Window maximum/minimum, subsegment frequency matching, shortest subarrays.
- **Intervals & Sweep Line:** Overlapping intervals, meeting room scheduling, interval intersections, dispatch slots.
- **Graph Traversal (BFS / Dijkstra):** Shortest path with transfer penalties, bus routes, city neighbor thresholds.
- **Dynamic Programming:** Maximum points with cost, optimal account balancing, ride split combinations.

---

## 📝 Verified Multi-Year OA Question Bank (Past 3 Years)
*Every problem listed below is a distinct, verified question sourced from 2023, 2024, and 2025/2026 campus placement drives (IITs, NITs, BITS, DTU) and off-campus Uber CodeSignal assessments. Duplicates across college slots have been strictly merged.*

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
- **Complexity:** $O(\sum |routes[i]|)$ Time.

#### 3. Submatrix Full Match / Rectangle Pattern Count
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Summary:** Given a large matrix $A$ and a pattern matrix $B$. Find the number of submatrices in $A$ that match $B$ under rotational or numerical transformation rules.
- **Approach:** 2D sliding window hash (2D Rabin-Karp) or direct simulation with early exit.
- **Complexity:** $O(M \times N)$ Time.

#### 4. Meeting Rooms II (Sweep Line / Min-Heap)
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Summary:** Given an array of meeting time intervals consisting of start and end times `[[s1,e1],[s2,e2],...]`, find the minimum number of conference rooms required.
- **LeetCode Equivalent:** [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- **Approach:** Sweep Line with start and end events or Min-Heap tracking active room end times.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 5. Array Pairs with Index-Value Invariant Matching (Uber OA 2024)
- **College/Drive:** Uber USA / India SWE New Grad 2024
- **Problem Summary:** Given two arrays $A$ and $B$ of length $N$, count the number of pairs $(i, j)$ with $i < j$ such that $A[i] - B[j] == A[j] - B[i]$.
- **Approach:**
  - Rearrange equation: $A[i] + B[i] == A[j] + B[j]$.
  - Compute $C[i] = A[i] + B[i]$ for each index.
  - Count frequencies of each value in $C$ using a Hash Map; for a value with frequency $f$, add $\binom{f}{2} = \frac{f(f-1)}{2}$ to total.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 6. Text Editor with Undo/Redo & Selection (CodeSignal Task 3)
- **College/Drive:** Uber CodeSignal GCA 2024
- **Problem Summary:** Implement a text editor supporting commands: `INSERT(text)`, `DELETE()`, `SELECT(start, end)`, `COPY()`, `PASTE()`, and `UNDO()`.
- **Approach:** String builder / buffer with a Stack storing prior snapshots for undo operations.
- **Complexity:** $O(1)$ amortized per operation, $O(K \times L)$ space.

#### 7. Maximum Points with Cost (Grid Dynamic Programming)
- **College/Drive:** Uber Engineering Campus 2024
- **Problem Summary:** You are given an $m \times n$ integer matrix `points`. You want to maximize the number of points you can get by picking one cell from each row, subject to a penalty equal to the column distance $|c_1 - c_2|$ between adjacent rows.
- **LeetCode Equivalent:** [1937. Maximum Number of Points with Cost](https://leetcode.com/problems/maximum-number-of-points-with-cost/)
- **Approach:** DP optimized from $O(M \cdot N^2)$ to $O(M \cdot N)$ using left-to-right and right-to-left prefix maximum passes for column distances.
- **Complexity:** $O(M \times N)$ Time, $O(N)$ Space.

#### 8. Construct Quad Tree (2D Spatial Matrix Decomposition)
- **College/Drive:** Uber SDE Slot 2024
- **Problem Summary:** Given an $n \times n$ matrix of 0s and 1s, construct a QuadTree representation where leaf nodes represent uniform blocks and internal nodes divide into 4 children.
- **LeetCode Equivalent:** [427. Construct Quad Tree](https://leetcode.com/problems/construct-quad-tree/)
- **Approach:** Recursive divide and conquer; check if subgrid has uniform value. If yes, return leaf; else recurse on 4 quadrants.
- **Complexity:** $O(N^2 \log N)$ Time.

#### 9. Minimum Window Substring
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Given two strings $s$ and $t$, return the minimum window substring of $s$ containing all characters of $t$.
- **LeetCode Equivalent:** [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- **Approach:** Sliding window with two pointers and character frequency hash map.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 10. Find the City With the Smallest Number of Neighbors at Threshold Distance
- **College/Drive:** Off-Campus Drive 2024
- **Problem Summary:** There are $n$ cities numbered from $0$ to $n-1$. Given edges with weights, find the city with the smallest number of cities that are reachable through some path whose distance is at most `distanceThreshold`.
- **LeetCode Equivalent:** [1334. Find the City With the Smallest Number of Neighbors at a Threshold Distance](https://leetcode.com/problems/find-the-city-with-the-smallest-number-of-neighbors-at-a-threshold-distance/)
- **Approach:** Floyd-Warshall all-pairs shortest paths algorithm in $O(N^3)$, then count valid pairs.
- **Complexity:** $O(N^3)$ Time, $O(N^2)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Word Ladder (Bidirectional BFS)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Shortest transformation sequence from `beginWord` to `endWord` using word dictionary.
- **LeetCode Equivalent:** [127. Word Ladder](https://leetcode.com/problems/word-ladder/)
- **Approach:** Bidirectional BFS checking 1-letter substitutions.
- **Complexity:** $O(M^2 \times N)$ Time.

#### 12. Network Delay Time / Dispatch Latency
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Calculate minimum time for all dispatch nodes to receive broadcast signal.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's algorithm using Priority Queue.
- **Complexity:** $O(E \log V)$ Time.

#### 13. Trapping Rain Water
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Elevation histogram water capacity.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 14. LRU Cache Implementation
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Implement $O(1)$ LRU Cache with hash map and doubly linked list.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Complexity:** $O(1)$ Time per op.

#### 15. Course Schedule II (Topological Sort)
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Valid ordering of course dependencies.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Complexity:** $O(V + E)$ Time.

#### 16. Subarray Sum Equals K (Ride Fare Reconciliation)
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Count subarrays whose sum equals target $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 17. Reorganize String (Max-Heap Priority)
- **College/Drive:** Uber Tech Slot 2023
- **Problem Summary:** Rearrange string characters such that no two adjacent characters are identical.
- **LeetCode Equivalent:** [767. Reorganize String](https://leetcode.com/problems/reorganize-string/)
- **Complexity:** $O(N \log 26) = O(N)$ Time.

#### 18. Rotting Oranges (Multi-Source BFS)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Minimum minutes to spread contagion on grid.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 19. Optimal Account Balancing (Multi-Party Ride Split)
- **College/Drive:** Advanced SWE Slot 2023
- **Problem Summary:** Minimum transactions to settle all debts between riders.
- **LeetCode Equivalent:** [465. Optimal Account Balancing](https://leetcode.com/problems/optimal-account-balancing/)
- **Complexity:** $O(2^N)$ for $N \le 12$.

#### 20. Longest Substring with at Most K Distinct Characters
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Find length of longest substring containing at most $K$ distinct characters.
- **LeetCode Equivalent:** [340. Longest Substring with At Most K Distinct Characters](https://leetcode.com/problems/longest-substring-with-at-most-k-distinct-characters/)
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

---

## 💡 CodeSignal GCA Strategy for Uber
1. **Pacing Across 4 Tasks:** Aim to complete Task 1 & Task 2 in under 18 minutes.
2. **Beware of Task 3 Simulation Traps:** Task 3 often has long specifications (e.g. text editors, memory maps). Read carefully to handle edge cases before testing.
3. **Task 4 Algorithmic Rigor:** Task 4 almost always requires an $O(N)$ or $O(N \log N)$ algorithm (Monotonic Deque, Prefix Hash, Segment Trees). $O(N^2)$ solutions will fail hidden scale test cases and drop your score below 820.
