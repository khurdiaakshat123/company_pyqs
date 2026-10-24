# SAP Labs Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏢

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **SHL** / **HackerRank**
- **Eligibility Benchmark:** Often enforces a strict 7.0+ CGPA academic cutoff for campus hiring drives.
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Core CS & Technical MCQs (30 mins):** 20 to 25 MCQs covering Object-Oriented Programming (Java/C++), Operating Systems (Paging, Semaphores, Deadlocks), DBMS (SQL Indexing, ACID, B+ Trees), and In-Memory Data Processing concepts.
  2. **Coding Assessment (60 mins, 2 Questions):** Medium to Hard difficulty problems in DSA + occasionally 1 complex SQL scenario.
- **Evaluation Criteria:** Passing both coding questions + high accuracy on the core CS fundamentals MCQs is necessary for interview shortlisting.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Trees & Binary Search Trees:** Lowest common ancestor, boundary traversals, diameter, level-order processing.
- **Arrays & Bucket Sorting:** Maximum gap, subsegment balance, sorting variations, two pointers.
- **Dynamic Programming & Strings:** Longest common subsequence, knapsack variations, coin change, word break.
- **Graphs & BFS:** Supply chain network routing, warehouse grid spread (rotting oranges), topological build dependencies.
- **Enterprise SQL Queries:** Window functions (`DENSE_RANK`, `ROW_NUMBER`), aggregations, group-by partitions, recency analysis.
- **Core CS MCQs:** Java Garbage Collection (G1GC vs ZGC), In-memory column stores (SAP HANA architecture), ACID transactions.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Maximum Gap in Linear Time (Bucket Sort / Pigeonhole)
- **College/Drive:** NIT Trichy / NIT Warangal 2024
- **Problem Statement:** Given an integer array `nums`, return the maximum difference between two successive elements in its sorted form. You must write an algorithm that runs in linear time $O(N)$ and uses linear extra space.
- **LeetCode Equivalent:** [164. Maximum Gap](https://leetcode.com/problems/maximum-gap/)
- **Approach:** Pigeonhole Principle / Bucket Sort: Compute $\min$ and $\max$. Divide range into $N-1$ buckets of size $B = \max(1, \lfloor \frac{\max - \min}{N - 1} \rfloor)$. Track only the minimum and maximum of each bucket. Maximum gap will always occur between adjacent non-empty buckets.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 2. Lowest Common Ancestor of Deepest Leaves (Tree Traversal)
- **College/Drive:** BITS Pilani 2024
- **Problem Statement:** Given the root of a binary tree, return the lowest common ancestor of its deepest leaves.
- **LeetCode Equivalent:** [1123. Lowest Common Ancestor of Deepest Leaves](https://leetcode.com/problems/lowest-common-ancestor-of-deepest-leaves/)
- **Approach:** Post-order DFS returning pair `(max_depth, lca_node)`. If left depth == right depth, current node is LCA; else return result of deeper subtree.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 3. Enterprise Supply Chain Routing / Minimum Cost Grid Path
- **College/Drive:** DTU / NSUT 2024
- **Problem Statement:** An ERP warehouse routes raw materials across an $M \times N$ factory grid where each cell has a transportation fee. Moving right or down is free, moving left or up costs an extra surcharge $K$. Find the minimum total cost from top-left to bottom-right.
- **Approach:** 0-1 BFS or Dijkstra's Algorithm on 2D grid.
- **Complexity:** $O(M \times N \log(M \times N))$ Time.

#### 4. Real SQL Question: Top Performing Sales Regions
- **College/Drive:** VIT / Manipal 2024
- **Problem Statement:** Write a query to find the top 2 sales executives with the highest revenue in each sales region during Q3 2024.
- **SQL Implementation:**
  ```sql
  WITH RankedSales AS (
      SELECT region_id, employee_id, SUM(order_amount) as total_revenue,
             DENSE_RANK() OVER (PARTITION BY region_id ORDER BY SUM(order_amount) DESC) as rnk
      FROM Sales
      WHERE order_date BETWEEN '2024-07-01' AND '2024-09-30'
      GROUP BY region_id, employee_id
  )
  SELECT region_id, employee_id, total_revenue
  FROM RankedSales
  WHERE rnk <= 2;
  ```

#### 5. Merge Intervals (ERP Scheduling Conflicts)
- **College/Drive:** IIT Roorkee 2024
- **Problem Statement:** Given an array of intervals `intervals` where `intervals[i] = [start_i, end_i]`, merge all overlapping intervals representing production runs.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time. Merge greedily if current interval overlaps with previous.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 6. Subarray Sum Equals K (Order Value Analysis)
- **College/Drive:** BITS Pilani 2024
- **Problem Statement:** Given an array of integer transaction amounts `nums` and target `k`, return the total number of continuous subarrays whose sum equals `k`.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Running prefix sum with hash map storing cumulative frequency counts.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Warehouse Spoilage Spread (Rotting Oranges)
- **College/Drive:** NIT Surathkal 2024
- **Problem Statement:** You are given an $M \times N$ grid of perishable stock items where $0$ is empty, $1$ is fresh, and $2$ is spoiled. Each minute, fresh items adjacent to spoiled ones spoil. Calculate minimum minutes until no fresh stock remains, or $-1$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS initializing queue with all spoiled item coordinates.
- **Complexity:** $O(M \times N)$ Time and Space.

#### 8. Trapping Rain Water (Reservoir Simulation)
- **College/Drive:** Thapar University 2024
- **Problem Statement:** Compute total water trapped by elevation bars after rain.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers inward from left and right maintaining running maxima.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Search in Rotated Sorted Array
- **College/Drive:** Manipal Institute of Technology 2024
- **Problem Statement:** Search for a target integer in an array sorted in ascending order and rotated at an unknown pivot.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Modified binary search identifying which half is strictly sorted.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 10. Real SQL Question: Customer Lifetime Value & Churn Recency
- **College/Drive:** SAP Labs Campus Drive 2024
- **Problem Statement:** Find customers who have made at least 3 orders, have total lifetime spending $> \$5,000$, and whose most recent order was placed within the last 60 days.
- **SQL Implementation:**
  ```sql
  SELECT customer_id, COUNT(order_id) AS total_orders, SUM(order_total) AS lifetime_spend
  FROM Orders
  GROUP BY customer_id
  HAVING COUNT(order_id) >= 3 
     AND SUM(order_total) > 5000 
     AND MAX(order_date) >= CURRENT_DATE - INTERVAL '60' DAY;
  ```

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Coin Change (Fewest Coins)
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Return fewest coins to make target amount.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 12. Binary Tree Level Order Traversal
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Output nodes level-by-level from left to right.
- **LeetCode Equivalent:** [102. Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/)
- **Complexity:** $O(N)$ Time.

#### 13. Valid Parentheses
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Check if brackets in ERP expression string are valid.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Complexity:** $O(N)$ Time.

#### 14. Longest Common Subsequence (ERP Product Diff)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Find longest common configuration between two software builds.
- **LeetCode Equivalent:** [1143. Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/)
- **Complexity:** $O(M \times N)$ Time.

#### 15. Word Break (Enterprise Token Parser)
- **College/Drive:** RVCE Bengaluru 2023
- **Problem Statement:** Given a string `s` and a dictionary `wordDict`, determine if `s` can be segmented into a sequence of dictionary words.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Approach:** 1D DP boolean array: `dp[i]` is true if prefix `s[0...i-1]` is valid.
- **Complexity:** $O(N^2)$ Time, $O(N)$ Space.

#### 16. Supply Chain Prerequisite Order (Course Schedule II)
- **College/Drive:** PES University 2023
- **Problem Statement:** Find valid assembly step sequence given dependency graph.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Topological Sort with Kahn's Algorithm.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 17. Longest Increasing Subsequence
- **College/Drive:** DTU Delhi 2023
- **Problem Statement:** Find length of longest strictly increasing subsequence in an array.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Approach:** Binary search patience sorting in $O(N \log N)$.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 18. LRU Query Cache Implementation
- **College/Drive:** Campus Placement 2023
- **Problem Statement:** Implement an LRU cache with $O(1)$ operations.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Hash Map pointing to Doubly Linked List nodes.
- **Complexity:** $O(1)$ Time per operation.

#### 19. Kth Largest Element in an Array
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Find the $k$-th largest element in an unsorted array.
- **LeetCode Equivalent:** [215. Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/)
- **Approach:** Min-Heap of size $K$ or Quickselect partition.
- **Complexity:** $O(N \log K)$ Time, $O(K)$ Space.

#### 20. Decode Ways (ERP Transaction Codes)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Number of ways to decode numeric message using '1'->'A' ... '26'->'Z'.
- **LeetCode Equivalent:** [91. Decode Ways](https://leetcode.com/problems/decode-ways/)
- **Approach:** 1D DP: $dp[i] = dp[i-1] + dp[i-2]$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent DBMS & Architecture MCQs Asked in SAP Labs OA
1. **Row-Store vs Column-Store (SAP HANA Architecture):**
   - Why do in-memory column-oriented databases perform analytical aggregation queries orders of magnitude faster than traditional row-oriented databases?
   - *Answer:* Column stores only read and load the specific columns referenced in the `SELECT` and `WHERE` clauses into CPU cache lines, completely skipping irrelevant column attributes. Furthermore, contiguous column data of identical types allows superior SIMD vectorization and compression (run-length encoding, dictionary encoding).
2. **B+ Tree Indexing Properties:**
   - Why are B+ trees preferred over B trees for disk-based relational database indexes?
   - *Answer:* In a B+ tree, internal nodes store only search keys (allowing higher fan-out and shallower tree height), and all data pointers are stored exclusively at the leaf level. Furthermore, leaf nodes are linked sequentially in a doubly linked list, enabling highly efficient range scan queries.
