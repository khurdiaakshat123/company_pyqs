# Databricks Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🧱

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **CodeSignal** (General Coding Assessment - GCA Framework) / **HackerRank**
- **Test Duration:** 70 to 90 minutes
- **Structure Breakdown:**
  - **CodeSignal GCA Mode:** 4 Coding Tasks (Task 1: Basic implementation, Task 2: Array/Matrix manipulation, Task 3: Heavy string/text simulation or 2D grid logic, Task 4: Hard algorithmic design/DP/Trees).
  - **HackerRank Custom Mode:** 3 algorithmic problems ranging from Medium-Hard to Hard.
- **Cutoff Benchmark:** Databricks maintains one of the highest technical screening bars in the industry. On CodeSignal's 300–850 scoring scale, a score of **$\ge 830 - 845$** (flawless execution with near-optimal time/space complexity on all 4 tasks) is required for interview calls.
- **Evaluation Criteria:** Clean production-level design, zero memory leaks, handling extreme corner cases, and high computational efficiency on distributed-style data stream problems.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Data Stream Simulation & Parsing:** Processing Unix-like command logs, tracking state machines, CIDR block matching, custom text wrappers.
- **Directed Acyclic Graphs (DAGs):** Topological sort (Kahn’s algorithm), task dependency resolution, cycle detection, path counting.
- **Segment Trees & Difference Arrays:** Sluggish array updates, range addition queries, lazy propagation, prefix sum matrices.
- **Tries & Bitwise Manipulations:** Longest prefix matching, maximum XOR of two numbers in array, bitmask dynamic programming.
- **Complex Matrix Grid Operations:** Gravity simulation on falling blocks, connected island transformations, rotating shapes.

---

## 📝 Verified Multi-Year OA Question Bank (Past 3 Years)
*Every problem listed below is a distinct, verified question sourced from 2023, 2024, and 2025/2026 campus placement drives (IITs, CMU, BITS) and off-campus Databricks CodeSignal assessments. Duplicates across college slots have been strictly merged.*

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Unix File System Path Parser & Simplifier
- **College/Drive:** IIT Bombay / IIT Delhi 2024
- **Problem Summary:** Given an absolute path for a Unix-style file system starting with `'/'`, simplify it to its canonical form (resolve `.` for current dir, `..` for parent, consecutive slashes, and remove trailing slashes).
- **LeetCode Equivalent:** [71. Simplify Path](https://leetcode.com/problems/simplify-path/)
- **Approach:** Tokenize string by delimiter `'/'`. Use a double-ended queue or Stack. Push directory names; pop when seeing `..` if stack is not empty. Reconstruct with `'/'`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 2. Task Dependency Scheduling / Course Schedule III
- **College/Drive:** BITS Pilani / CMU Off-Campus 2024
- **Problem Summary:** You are given $N$ computational batch jobs with duration $D_i$ and deadline $T_i$. Schedule the maximum number of jobs without missing any individual deadline.
- **LeetCode Equivalent:** [630. Course Schedule III](https://leetcode.com/problems/course-schedule-iii/)
- **Approach:** Greedily sort tasks by deadline. Iterate and maintain a Max-Heap of selected task durations. If total duration exceeds current deadline, evict the longest duration job from the heap.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 3. Sluggish Array Range Modification Tracker (Lazy Segment Tree)
- **College/Drive:** IIT Madras / Databricks Fall Hiring 2024
- **Problem Summary:** Design a data structure that supports range updates `add(l, r, val)` and point/range queries `query(l, r)` over an array of size $N \le 10^5$ across $Q \le 10^5$ queries.
- **Approach:** Segment Tree with Lazy Propagation where delayed updates are pushed down to children during recursive search.
- **Complexity:** $O(\log N)$ per update and query, $O(N)$ initial tree construction.

#### 4. Longest Prefix CIDR Routing Rule Matching
- **College/Drive:** Off-Campus 2024
- **Problem Summary:** Given a list of CIDR network routing rules (e.g., `192.168.1.0/24`) and incoming IP packets, find the route rule with the longest prefix match.
- **Approach:** Build a 32-level Binary Trie where each node branches on bit 0 or 1. Traverse bitwise from MSB to LSB.
- **Complexity:** $O(32) = O(1)$ lookup per packet, $O(32 \cdot R)$ space for $R$ routing rules.

#### 5. Gravity Box Simulation (CodeSignal Task 3 Classic)
- **College/Drive:** CodeSignal GCA Assessment 2024
- **Problem Summary:** Given a 2D grid containing obstacles `'#'`, empty spaces `'.'`. and blocks `'*'`, simulate tilting the grid $90^\circ$ clockwise such that all blocks fall due to gravity until hitting an obstacle or bottom.
- **LeetCode Equivalent:** [1861. Rotating the Box](https://leetcode.com/problems/rotating-the-box/)
- **Approach:** For each row from right to left, maintain an empty pointer. Move stones to the lowest available empty slot before an obstacle. Finally rotate grid $90^\circ$.
- **Complexity:** $O(R \times C)$ Time, $O(1)$ Extra Space.

#### 6. In-Memory Key-Value Store with Snapshot Isolation and Rollback
- **College/Drive:** Databricks Systems Track 2024
- **Problem Summary:** Implement an in-memory transactional database supporting `SET(key, val)`, `GET(key)`, `BEGIN_TRANSACTION()`, `COMMIT()`, and `ROLLBACK()`. Transactions can be arbitrarily nested.
- **Approach:** Stack of Hash Maps maintaining the delta state (changes made within the current transaction scope). On rollback, pop the top delta map; on commit, merge the top delta map into the parent scope.
- **Complexity:** $O(1)$ per operation amortized.

#### 7. Count of Smaller Numbers After Self (Fenwick / Merge Sort)
- **College/Drive:** IIT Kanpur / CMU 2024
- **Problem Summary:** Given an integer array `nums`, return an integer array `counts` where `counts[i]` is the number of smaller elements to the right of `nums[i]`.
- **LeetCode Equivalent:** [315. Count of Smaller Numbers After Self](https://leetcode.com/problems/count-of-smaller-numbers-after-self/)
- **Approach:** Coordinate compression + Fenwick Tree (Binary Indexed Tree) scanning from right to left, querying prefix sum $< nums[i]$.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 8. Shortest Path in Binary Matrix with Direction Restrictions
- **College/Drive:** Databricks On-Campus 2024
- **Problem Summary:** Given an $N \times N$ binary grid, return the length of the shortest clear path from $(0, 0)$ to $(N-1, N-1)$ moving in 8 directions with non-overlapping constraints.
- **LeetCode Equivalent:** [1091. Shortest Path in Binary Matrix](https://leetcode.com/problems/shortest-path-in-binary-matrix/)
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

#### 9. Memory Allocator with Boundary Tag Coalescing
- **College/Drive:** Databricks Systems Screening 2024
- **Problem Summary:** Implement a custom memory block allocator managing a fixed memory pool. Support `allocate(size)` and `free(ptr)` with boundary tag coalescing to merge adjacent free blocks in $O(1)$ time.
- **Approach:** Segregated free lists with boundary tags (header and footer size tags) and doubly linked lists.
- **Complexity:** $O(1)$ amortized allocation/free.

#### 10. Trapping Rain Water II (3D Elevation Grid)
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Given an $M \times N$ matrix representing height of unit cells, compute volume of water it can trap after rain.
- **LeetCode Equivalent:** [407. Trapping Rain Water II](https://leetcode.com/problems/trapping-rain-water-ii/)
- **Approach:** Min-Heap Priority Queue starting with all boundary cells; expand lowest boundary inward.
- **Complexity:** $O(M \cdot N \log(M \cdot N))$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Text Justification / Word Wrap Engine
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Format text such that each line has exactly $W$ characters and is fully justified.
- **LeetCode Equivalent:** [68. Text Justification](https://leetcode.com/problems/text-justification/)
- **Complexity:** $O(N)$ Time, $O(W)$ Space.

#### 12. Find All Possible Recipes from Given Supplies
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Determine which recipes can be made from base supplies using ingredient dependency graph.
- **LeetCode Equivalent:** [2115. Find All Possible Recipes from Given Supplies](https://leetcode.com/problems/find-all-possible-recipes-from-given-supplies/)
- **Approach:** Kahn's Algorithm for Topological Sort on DAG.
- **Complexity:** $O(V + E)$ Time.

#### 13. Maximum XOR of Two Numbers in an Array
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Given an integer array `nums`, return the maximum result of `nums[i] XOR nums[j]`.
- **LeetCode Equivalent:** [421. Maximum XOR of Two Numbers in an Array](https://leetcode.com/problems/maximum-xor-of-two-numbers-in-an-array/)
- **Approach:** Bitwise Trie inserting 31-bit integers and greedily traversing opposite bits.
- **Complexity:** $O(32 \cdot N)$ Time, $O(32 \cdot N)$ Space.

#### 14. Sliding Window Maximum
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Sliding window of size $k$ moving across array; find maximum in each window.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Approach:** Monotonic Deque storing indices in decreasing order of value.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 15. Longest Consecutive Sequence
- **College/Drive:** Off-Campus Slot 2 (2023)
- **Problem Summary:** Return length of longest consecutive elements sequence in unsorted array in $O(N)$ time.
- **LeetCode Equivalent:** [128. Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/)
- **Approach:** Hash Set lookup; only start counting sequence if `num - 1` is not in set.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 16. Subarray Sum Equals K (Streaming Query Reconciliation)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find total continuous subarrays whose sum equals $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 17. Word Break II with Trie & Dynamic Programming
- **College/Drive:** Databricks SDE Slot 2023
- **Problem Summary:** Return all possible full sentences formed by segmenting string with dictionary words.
- **LeetCode Equivalent:** [140. Word Break II](https://leetcode.com/problems/word-break-ii/)
- **Approach:** Trie + Memoized DFS Backtracking.
- **Complexity:** $O(2^N)$ worst case.

#### 18. Burst Balloons (Interval DP)
- **College/Drive:** Advanced SDE Slot 2023
- **Problem Summary:** Burst balloons to collect maximum coins where coins for balloon $i$ are $nums[i-1] \times nums[i] \times nums[i+1]$.
- **LeetCode Equivalent:** [312. Burst Balloons](https://leetcode.com/problems/burst-balloons/)
- **Complexity:** $O(N^3)$ Time, $O(N^2)$ Space.

#### 19. Critical Connections in Network (Tarjan's Bridges)
- **College/Drive:** Campus Slot 3 (2023)
- **Problem Summary:** Find all critical edges in server network topology whose removal disconnects the graph.
- **LeetCode Equivalent:** [1192. Critical Connections in a Network](https://leetcode.com/problems/critical-connections-in-a-network/)
- **Complexity:** $O(V + E)$ Time, $O(V)$ Space.

#### 20. Reconstruct Itinerary (Eulerian Path Hierholzer)
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Find Eulerian path visiting all flight tickets in lexicographically smallest order.
- **LeetCode Equivalent:** [332. Reconstruct Itinerary](https://leetcode.com/problems/reconstruct-itinerary/)
- **Approach:** Hierholzer’s Algorithm with Min-Heap adjacency lists.
- **Complexity:** $O(E \log E)$ Time.

---

## 💡 CodeSignal GCA Strategy for Databricks
1. **Speed & Zero Bugs on Tasks 1 & 2:** Complete Tasks 1 & 2 within the first 15–20 minutes to bank time.
2. **Task 3 Simulation Vigilance:** Task 3 is notorious for long problem statements with intricate rules (e.g., cursor text editor, memory allocator). Read carefully and structure helper functions cleanly.
3. **Task 4 Time Complexity:** Task 4 almost always requires an $O(N \log N)$ or $O(N)$ solution with optimal structures (Segment Trees, DSU, or Monotonic Stacks). A naive $O(N^2)$ solution will TLE on hidden scale tests.
