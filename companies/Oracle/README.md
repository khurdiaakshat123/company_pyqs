# Oracle Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🔴

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 to 105 minutes
- **Structure Breakdown:**
  - **Part 1: Coding Assessment** (1 to 2 Coding Questions, 45–60 mins) – Focuses on Arrays, Prefix Sums, Intervals, and Binary Search.
  - **Part 2: Core CS & Aptitude MCQs** (15 to 35 Questions, 30–45 mins) – OS, DBMS, Computer Networks, OOPs (Java focus), and Quantitative Aptitude.
- **Scoring & Cutoff:** Oracle strictly evaluates the MCQ section alongside coding. Candidates passing all coding test cases but scoring poorly on OS/DBMS MCQs are frequently screened out.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Core CS MCQs (DBMS / OS):** SQL joins, normalization (3NF/BCNF), ACID, Semaphores, Paging, Page Faults.
- **Arrays & Prefix Sums:** Partition index, balanced even/odd sums, subarray equals K.
- **Binary Search on Answer:** Aggressive cows variation, allocation/capacity limits.
- **Java / OOP Fundamentals:** Immutability, String pool, Garbage collection, Exception hierarchy.
- **Matrix Traversals & BFS:** Grid reachability, boundary island tracking.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Fair Indices / Even-Odd Balance Index (Oracle Classic)
- **College/Drive:** IIT BHU / NIT Surathkal 2024
- **Problem Summary:** Given an array $A$ of size $N$, find the number of indices $i$ such that removing $A[i]$ makes the sum of elements at even positions equal to the sum of elements at odd positions.
- **Approach:** Maintain `even_prefix`, `odd_prefix`, `even_suffix`, `odd_suffix`. When removing index $i$, suffix elements flip their parity. Check in $O(1)$ per index.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 2. Minimum Reduction Cost (Greedy Array Reduction)
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** Repeatedly pick the two minimum elements in an array, remove them, and insert their sum back into the array until one element remains. Calculate the minimum total cost of all operations.
- **LeetCode Equivalent:** [1167. Minimum Cost to Connect Sticks](https://leetcode.com/problems/minimum-cost-to-connect-sticks/)
- **Approach:** Min-Heap (`priority_queue`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 3. Database Server Cluster Capacity Optimization
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** Allocate $M$ database query requests across $N$ servers such that the maximum load on any single server is minimized.
- **Approach:** Binary Search on maximum capacity (`low = max(requests)`, `high = sum(requests)`).
- **Complexity:** $O(N \log(\text{sum}))$.

#### 4. Matrix Path with Turn Restrictions (3D DP)
- **College/Drive:** IIIT Allahabad 2024
- **Problem Summary:** Given an $M \times N$ grid, find the number of paths from $(0, 0)$ to $(M-1, N-1)$ where moving right or down is permitted, but consecutive turns in the same direction are bounded by $K$.
- **Approach:** 3D Dynamic Programming: `dp[r][c][consecutive_turns]`.
- **Complexity:** $O(M \times N \times K)$ Time.

#### 5. Real SQL Question: Employee Hierarchy Depth
- **College/Drive:** Campus Placement Drive 2024
- **Problem Statement:** Write a recursive SQL query using CTE to compute the management hierarchy level for every employee in an enterprise organization.
- **SQL Implementation:**
  ```sql
  WITH RECURSIVE EmpHierarchy AS (
      SELECT emp_id, emp_name, manager_id, 1 as level
      FROM Employees WHERE manager_id IS NULL
      UNION ALL
      SELECT e.emp_id, e.emp_name, e.manager_id, eh.level + 1
      FROM Employees e JOIN EmpHierarchy eh ON e.manager_id = eh.emp_id
  )
  SELECT * FROM EmpHierarchy ORDER BY level, emp_id;
  ```

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Subarray Sum Equals K
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Count continuous subarrays with sum $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Lowest Common Ancestor in Binary Search Tree
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Find LCA in BST using value comparisons.
- **LeetCode Equivalent:** [235. Lowest Common Ancestor of a Binary Search Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/)
- **Complexity:** $O(H)$ Time.

#### 8. Merge Two Sorted Lists (In-Place Pointers)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Splice together nodes of two sorted lists.
- **LeetCode Equivalent:** [21. Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
- **Complexity:** $O(N + M)$ Time.

#### 9. Valid Anagram Verification
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Verify string anagram matching.
- **LeetCode Equivalent:** [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- **Complexity:** $O(N)$ Time.

#### 10. Coin Change (Minimum Coins)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Unbounded knapsack minimum coins.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time.
