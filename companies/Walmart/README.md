# Walmart Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🛒

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

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Dynamic Programming | Medium - Hard | State transitions, unbounded knapsack, coin change variants, grid paths |
| **Very High** | Graphs & BFS/DFS | Medium - Hard | Shortest path, connected components, bipartite graphs, multi-source BFS |
| **High** | Trees & Binary Search Trees | Medium | Lowest Common Ancestor (LCA), tree diameter, serialize/deserialize |
| **High** | Monotonic Stack / Queue | Medium | Next greater element, largest rectangle in histogram, trapping rain water |
| **Medium** | Binary Search on Answer | Medium | Allocation problems, capacity thresholds, minimum maximums |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Optimal Warehouse Stock Distribution (Knapsack Variant)
- **Problem Summary:** A retail distribution center has $N$ item types, each with weight $W_i$, volume $V_i$, and profit $P_i$. A truck has maximum weight capacity $C_W$ and volume capacity $C_V$. Find the maximum total profit that can be loaded into the truck.
- **Approach:** 2D Dynamic Programming (Knapsack with two independent budget constraints).
- **Complexity:** $O(N \times C_W \times C_V)$ Time.

### 2. Rotting Fruit / Warehouse Spoilage Time
- **Problem Summary:** A warehouse layout is represented as an $M \times N$ grid with fresh items, spoiled items, and empty shelves. Every hour, any fresh item adjacent to a spoiled item spoils. Calculate minimum hours until no fresh items remain, or return -1 if impossible.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-Source Breadth-First Search (BFS).
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

### 3. Lowest Common Ancestor in Binary Tree
- **Problem Summary:** Given a binary tree, find the lowest common ancestor (LCA) of two given nodes $p$ and $q$.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Approach:** Post-order DFS recursion: If root matches $p$ or $q$, return root. If both left and right recursive calls return non-null, root is the LCA.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

### 4. Coin Change / Minimal Denomination Transfers
- **Problem Summary:** You are given an integer array `coins` representing coins of different denominations and an integer `amount`. Return the fewest number of coins that you need to make up that amount.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP array initialized to infinity. `dp[i] = min(dp[i], 1 + dp[i - c])`.
- **Complexity:** $O(N \times \text{amount})$ Time, $O(\text{amount})$ Space.

---

## 💡 Cracking Walmart OA
1. **Watch HackerEarth Memory Limits:** Pay close attention to spatial constraints; avoid unnecessarily large recursion depths that trigger StackOverflow.
2. **Handle Large Integers:** For DP sums and product queries, use 64-bit integer types (`long long` in C++) to prevent integer wrap-around.
