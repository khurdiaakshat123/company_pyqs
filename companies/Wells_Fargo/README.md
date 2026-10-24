# Wells Fargo Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏦

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 75 to 90 minutes
- **Structure Breakdown:**
  1. **Coding Section:** 2 Coding Questions (LeetCode Easy to Medium difficulty, 45 mins).
  2. **SQL Query Challenge:** 1 Practical SQL Query (Intermediate to Advanced, 15 mins).
  3. **Core CS & Aptitude Section:** 10 to 15 MCQs covering Database Systems, Operating Systems, OOPs concepts, and Quantitative/Verbal Aptitude (20 mins).
- **Passing Cutoff:** Full score on the SQL query is often a hard requirement alongside at least 1.5 coding questions cleared.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **SQL Queries:** Window functions (`DENSE_RANK()`, `ROW_NUMBER()`), `GROUP BY`, `HAVING`, Self-joins, CTEs.
- **Arrays & Two Pointers:** Sliding window, subarray sums, element removal, running balance, prefix products.
- **Strings & HashMaps:** Frequency maps, isomorphic strings, longest substring without repeats, anagram grouping.
- **Grid Traversals (BFS / DFS):** Matrix paths, island count, shortest path in binary matrix, rotten oranges.
- **Dynamic Programming:** House robber, coin change, maximum subarray sum.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Longest Substring Without Repeating Characters
- **College/Drive:** IIT Roorkee / BITS Pilani 2024–2025
- **Problem Summary:** Given a string $s$, find the length of the longest substring without repeating characters.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with a hash map storing the last seen index of each character.
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

#### 2. Minimum Operations to Make Array Equal
- **College/Drive:** NIT Trichy / DTU 2024–2025
- **Problem Summary:** You have an array `arr` of length `n` where `arr[i] = (2 * i) + 1` for all valid `i`. In one operation, subtract 1 from `arr[x]` and add 1 to `arr[y]`. Return minimum operations to make all elements equal.
- **Constraints:** $1 \le n \le 10^4$.
- **LeetCode Equivalent:** [1551. Minimum Operations to Make Array Equal](https://leetcode.com/problems/minimum-operations-to-make-array-equal/)
- **Approach:** Math formula: $\lfloor \frac{n^2}{4} \rfloor$.
- **Complexity:** $O(1)$ Time.

#### 3. Shortest Path in Binary Matrix (8-Directional BFS)
- **College/Drive:** IIIT Allahabad 2024–2025
- **Problem Summary:** Given an $n \times n$ binary matrix `grid`, return the length of the shortest clear path in the matrix. If there is no clear path, return -1 (8-directional movement permitted).
- **Constraints:** $1 \le n \le 100$.
- **LeetCode Equivalent:** [1091. Shortest Path in Binary Matrix](https://leetcode.com/problems/shortest-path-in-binary-matrix/)
- **Approach:** Breadth-First Search (BFS) level traversal.
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

#### 4. Real SQL Question: Department Top 3 Salaries
- **College/Drive:** Wells Fargo Campus 2024–2025
- **LeetCode Equivalent:** [185. Department Top Three Salaries](https://leetcode.com/problems/department-top-three-salaries/)
- **SQL Implementation:**
  ```sql
  WITH RankedSalaries AS (
      SELECT d.name AS Department, e.name AS Employee, e.salary AS Salary,
             DENSE_RANK() OVER (PARTITION BY e.departmentId ORDER BY e.salary DESC) AS rnk
      FROM Employee e JOIN Department d ON e.departmentId = d.id
  )
  SELECT Department, Employee, Salary FROM RankedSalaries WHERE rnk <= 3;
  ```

#### 5. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Off-Campus Drive 2024–2025
- **Problem Summary:** Find contiguous subarray with maximum sum.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Approach:** Kadane's algorithm tracking running sum: `curr = max(x, curr + x)`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 6. Subarray Sum Equals K / Cash Balance
- **College/Drive:** Wells Fargo Bangalore Drive 2024
- **Problem Summary:** Return the total number of continuous subarrays whose sum equals to $k$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Hash Map tracking prefix sum frequencies.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Rotten Oranges / Multi-Source BFS
- **College/Drive:** Wells Fargo Campus Slot 2024
- **Problem Summary:** Minimum minutes to infect all oranges in grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 8. Course Schedule (Topological Sort)
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** Determine if candidate can finish all courses given prerequisite pairs.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Kahn's Algorithm using indegrees and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 9. Daily Temperatures (Monotonic Stack)
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Find days to wait for a warmer temperature.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Real SQL Question: Second Highest Salary & Consecutive Seats
- **College/Drive:** Wells Fargo Technical Screen 2024
- **LeetCode Equivalent:** [176. Second Highest Salary](https://leetcode.com/problems/second-highest-salary/)
- **SQL Implementation:**
  ```sql
  SELECT MAX(salary) AS SecondHighestSalary
  FROM Employee
  WHERE salary < (SELECT MAX(salary) FROM Employee);
  ```

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Number of Islands (2D Grid BFS)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Count connected components of 1s in binary matrix.
- **Constraints:** $M, N \le 300$.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Approach:** BFS or DFS marking visited land cells.
- **Complexity:** $O(M \times N)$ Time.

#### 12. Isomorphic Strings
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Determine if two strings are isomorphic.
- **Constraints:** $1 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [205. Isomorphic Strings](https://leetcode.com/problems/isomorphic-strings/)
- **Approach:** Two Hash Maps mapping character-to-character bijectively.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 13. Merge Intervals
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Merge overlapping transaction intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time and merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 14. Valid Parentheses
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Stack balanced brackets check.
- **Constraints:** $1 \le s.length \le 10^4$.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Stack matching opening with closing brackets.
- **Complexity:** $O(N)$ Time.

#### 15. Coin Change (Fewest Coins)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Minimum coins to make change.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 16. Product of Array Except Self
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Return array where `output[i]` is product of all elements except `nums[i]` without division.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Prefix product from left, suffix product from right.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 17. Two Sum
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Return indices of the two numbers such that they add up to target.
- **Constraints:** $2 \le nums.length \le 10^4$.
- **LeetCode Equivalent:** [1. Two Sum](https://leetcode.com/problems/two-sum/)
- **Approach:** Hash Map lookup for `target - num`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 18. House Robber (1D Dynamic Programming)
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Maximize stolen value without robbing two adjacent houses.
- **Constraints:** $1 \le nums.length \le 100$.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** DP: `dp[i] = max(dp[i-1], dp[i-2] + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 19. Search in Rotated Sorted Array
- **College/Drive:** Technical Assessment 2023
- **Problem Summary:** Find target in rotated sorted array in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 5000$.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking sorted half.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 20. Best Time to Buy and Sell Stock
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Maximize profit with a single buy and sell transaction.
- **Constraints:** $1 \le prices.length \le 10^5$.
- **LeetCode Equivalent:** [121. Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- **Approach:** One pass tracking minimum price so far.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent Database & Systems MCQs in Wells Fargo OA
1. **ACID Properties in Banking:**
   - How does the database guarantee Atomicity and Durability during system failure?
   - *Answer:* Via Write-Ahead Logging (WAL) and Undo/Redo transaction logs. Undo logs rollback uncommitted transactions; redo logs reapply committed transactions that were not yet flushed to data pages.
2. **Clustered vs Non-Clustered Indexes:**
   - Why can a database table have only one clustered index?
   - *Answer:* Because the clustered index defines the physical storage order of the actual rows on disk pages. Data can only be physically sorted one way.
3. **Deadlock Resolution in Relational Databases:**
   - How does the DBMS detect and resolve deadlocks between concurrent financial transactions?
   - *Answer:* The database maintains a Wait-For Graph (WFG) where vertices are transactions and directed edges represent lock waits. If a cycle is detected, the DBMS aborts and rolls back the "victim" transaction (usually the one with lowest cost to rollback).
