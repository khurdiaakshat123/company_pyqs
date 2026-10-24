# Walmart Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🛒

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerEarth**
- **Hiring Tracks:**
  - **Walmart Global Tech SDE-1 (Campus & Off-Campus):** 14–22 LPA
  - **Walmart CodeHers (Flagship Women Hiring Challenge):** 20+ LPA
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Coding Section:** 2 Coding Questions (Medium to Hard difficulty, 60 mins).
  2. **Technical MCQs:** 15 to 20 MCQs covering Data Structures, OS, DBMS, OOPs, and Algorithm Analysis (30 mins).
- **Passing Cutoff:** Full score on both coding problems (100% test cases) or 1 full + 1 near-complete passes are generally required for shortlisting.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Dynamic Programming:** 2D Knapsack, coin change variants, grid paths, word break.
- **Graphs & BFS/DFS:** Shortest path, connected components, bipartite graphs, multi-source BFS (rotting oranges), topological sort.
- **Trees & Binary Search Trees:** Lowest Common Ancestor (LCA), binary tree maximum path sum, serialize/deserialize.
- **Monotonic Stack / Queue:** Largest rectangle in histogram, sliding window maximum, trapping rain water.
- **Intervals & Sliding Window:** Merge intervals, longest substring without repeating characters, subarray sum equals K.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Optimal Warehouse Stock Distribution (2D Knapsack)
- **College/Drive:** IIT Roorkee / IIT BHU 2024
- **Problem Summary:** A retail distribution center has $N$ item types, each with weight $W_i$, volume $V_i$, and profit $P_i$. A truck has maximum weight capacity $C_W$ and volume capacity $C_V$. Find the maximum total profit that can be loaded into the truck.
- **Approach:** 2D Dynamic Programming (Knapsack with two independent budget constraints).
- **Complexity:** $O(N \times C_W \times C_V)$ Time.

#### 2. Rotting Fruit / Warehouse Spoilage Time (Multi-Source BFS)
- **College/Drive:** BITS Pilani / NIT Trichy 2024
- **Problem Summary:** Calculate minimum hours until no fresh items remain, or return -1 if impossible.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-Source Breadth-First Search (BFS).
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 3. Lowest Common Ancestor in Binary Tree
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** Given a binary tree, find the lowest common ancestor (LCA) of two given nodes $p$ and $q$.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Approach:** Post-order DFS recursion: If root matches $p$ or $q$, return root. If both left and right recursive calls return non-null, root is the LCA.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 4. Coin Change / Minimal Denomination Transfers
- **College/Drive:** Walmart CodeHers 2024
- **Problem Summary:** Return the fewest number of coins that you need to make up that amount.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP array initialized to infinity. `dp[i] = min(dp[i], 1 + dp[i - c])`.
- **Complexity:** $O(N \times \text{amount})$ Time, $O(\text{amount})$ Space.

#### 5. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Drive 2024
- **Problem Statement:** Sliding window with hash map storing character positions.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time.

#### 6. Subarray Sum Equals K (Cart Value Target)
- **College/Drive:** IIT Delhi 2024
- **Problem Summary:** Given customer item prices and cart target $K$, find total contiguous subsegments summing to $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Running prefix sum with hash map frequency tracking.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Search in Rotated Sorted Array (Catalog Binary Search)
- **College/Drive:** IIT Bombay 2024
- **Problem Summary:** Search target item price in a rotated sorted catalog array in $O(\log N)$ time.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking sorted half.
- **Complexity:** $O(\log N)$ Time.

#### 8. Largest Rectangle in Histogram (Warehouse Pallet Stacking)
- **College/Drive:** Walmart CodeHers 2024
- **Problem Summary:** Given an array of integers `heights` representing the histogram's bar height where the width of each bar is 1, return the area of the largest rectangle in the histogram.
- **LeetCode Equivalent:** [84. Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/)
- **Approach:** Monotonic Increasing Stack storing bar indices. When encountering a shorter bar, pop stack top and calculate area with height of popped bar.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 9. LRU Product Catalog Cache Implementation
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** Implement an LRU Cache with $O(1)$ `get` and `put` operations.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Hash Map pointing to Doubly Linked List nodes.
- **Complexity:** $O(1)$ Time per operation.

#### 10. Order Fulfillment Pipeline (Course Schedule II)
- **College/Drive:** NIT Surathkal 2024
- **Problem Summary:** Given $N$ packing tasks and dependencies, return a valid linear completion order or empty array if deadlock exists.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm using in-degrees and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Course Schedule (Topological Sort)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Check for cycles in task prerequisites.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Complexity:** $O(V + E)$ Time.

#### 12. Merge Intervals
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Merge overlapping delivery time slots.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time.

#### 13. Trapping Rain Water
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Compute water trapped between elevation bars.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time.

#### 14. Word Break (Dynamic Programming)
- **College/Drive:** Walmart CodeHers 2023
- **Problem Statement:** Segment string into dictionary words.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Complexity:** $O(N^2)$ Time.

#### 15. Maximum Subarray Sum (Kadane's)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Largest contiguous subarray sum.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time.

#### 16. Binary Tree Maximum Path Sum
- **College/Drive:** IIT Kharagpur 2023
- **Problem Statement:** Find maximum path sum of any non-empty path in a binary tree.
- **LeetCode Equivalent:** [124. Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/)
- **Approach:** Post-order DFS returning max branch gain.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 17. Reorganize String / Shelf Arrangement
- **College/Drive:** Walmart CodeHers 2023
- **Problem Statement:** Rearrange characters so that no two adjacent characters are identical.
- **LeetCode Equivalent:** [767. Reorganize String](https://leetcode.com/problems/reorganize-string/)
- **Approach:** Max-Heap of character frequencies.
- **Complexity:** $O(N \log \Sigma)$ Time.

#### 18. Decode String (Dual Stack)
- **College/Drive:** Campus Placement 2023
- **Problem Statement:** Decode nested string encoding format `k[string]`.
- **LeetCode Equivalent:** [394. Decode String](https://leetcode.com/problems/decode-string/)
- **Approach:** Dual stack for multipliers and strings.
- **Complexity:** $O(\text{Output Length})$ Time.

#### 19. Sliding Window Maximum / Inventory Burst
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Maximum element in sliding window of size $K$.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Approach:** Monotonic Decreasing Deque.
- **Complexity:** $O(N)$ Time.

#### 20. Minimum Cost to Connect All Points (Delivery Network MST)
- **College/Drive:** Pan-India 2023
- **Problem Statement:** Connect $N$ delivery hubs with minimum total Manhattan distance.
- **LeetCode Equivalent:** [1584. Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)
- **Approach:** Prim's algorithm or Kruskal's with DSU.
- **Complexity:** $O(N^2)$ Time.
