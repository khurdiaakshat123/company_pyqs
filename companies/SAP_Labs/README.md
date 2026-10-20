# SAP Labs Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏢

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **SHL** / **HackerRank**
- **Eligibility Benchmark:** Often enforces a strict 7.0+ CGPA academic cutoff for campus hiring drives.
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Core CS & Technical MCQs (30 mins):** 20 to 25 MCQs covering Object-Oriented Programming (Java/C++), Operating Systems (Paging, Semaphores), DBMS (SQL Indexing, ACID), and Software Architecture.
  2. **Coding Assessment (60 mins, 2 Questions):** Medium to Hard difficulty problems.
- **Evaluation Criteria:** Passing both coding questions + high accuracy on the core CS fundamentals MCQs is necessary.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Trees & Binary Search Trees:** Lowest common ancestor, boundary traversals, diameter.
- **Arrays & Bucket Sorting:** Maximum gap, subsegment balance, sorting variations.
- **Dynamic Programming:** Knapsack variations, minimum path matrix costs.
- **Enterprise SQL Queries:** Aggregations, window ranks, nested queries.

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

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Coin Change (Fewest Coins)
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Return fewest coins to make target amount.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 6. Binary Tree Level Order Traversal
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Output nodes level-by-level from left to right.
- **LeetCode Equivalent:** [102. Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/)
- **Complexity:** $O(N)$ Time.

#### 7. Valid Parentheses
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Check if brackets in ERP expression string are valid.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Complexity:** $O(N)$ Time.

#### 8. Longest Common Subsequence (ERP Product Diff)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Find longest common configuration between two software builds.
- **LeetCode Equivalent:** [1143. Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/)
- **Complexity:** $O(M \times N)$ Time.
