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
- **Dynamic Programming:** State transitions, unbounded knapsack, coin change variants, grid paths.
- **Graphs & BFS/DFS:** Shortest path, connected components, bipartite graphs, multi-source BFS.
- **Trees & Binary Search Trees:** Lowest Common Ancestor (LCA), tree diameter, serialize/deserialize.
- **Monotonic Stack / Queue:** Next greater element, largest rectangle in histogram, trapping rain water.

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

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Course Schedule (Topological Sort)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Check for cycles in task prerequisites.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Complexity:** $O(V + E)$ Time.

#### 7. Merge Intervals
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Merge overlapping delivery time slots.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time.

#### 8. Trapping Rain Water
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Compute water trapped between elevation bars.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time.

#### 9. Word Break (Dynamic Programming)
- **College/Drive:** Walmart CodeHers 2023
- **Problem Statement:** Segment string into dictionary words.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Complexity:** $O(N^2)$ Time.

#### 10. Maximum Subarray Sum (Kadane's)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Largest contiguous subarray sum.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time.
