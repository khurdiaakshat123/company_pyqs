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
- **SQL Queries:** Window functions (`DENSE_RANK()`, `ROW_NUMBER()`), `GROUP BY`, `HAVING`, Self-joins.
- **Arrays & Two Pointers:** Sliding window, subarray sums, element removal, running balance.
- **Strings & HashMaps:** Frequency maps, isomorphic strings, longest substring without repeats.
- **Grid Traversals (BFS / DFS):** Matrix paths, island count, shortest path in binary matrix.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Longest Substring Without Repeating Characters
- **College/Drive:** IIT Roorkee / BITS Pilani 2024
- **Problem Summary:** Given a string $s$, find the length of the longest substring without repeating characters.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with a hash map storing the last seen index of each character.
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

#### 2. Minimum Operations to Make Array Equal
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Summary:** You have an array `arr` of length `n` where `arr[i] = (2 * i) + 1` for all valid `i`. In one operation, subtract 1 from `arr[x]` and add 1 to `arr[y]`. Return minimum operations to make all elements equal.
- **LeetCode Equivalent:** [1551. Minimum Operations to Make Array Equal](https://leetcode.com/problems/minimum-operations-to-make-array-equal/)
- **Approach:** Math formula: $\lfloor \frac{n^2}{4} \rfloor$.
- **Complexity:** $O(1)$ Time.

#### 3. Shortest Path in Binary Matrix (8-Directional BFS)
- **College/Drive:** IIIT Allahabad 2024
- **Problem Summary:** Given an $n \times n$ binary matrix `grid`, return the length of the shortest clear path in the matrix. If there is no clear path, return -1 (8-directional movement permitted).
- **LeetCode Equivalent:** [1091. Shortest Path in Binary Matrix](https://leetcode.com/problems/shortest-path-in-binary-matrix/)
- **Approach:** Breadth-First Search (BFS) level traversal.
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

#### 4. Real SQL Question: Department Top 3 Salaries
- **College/Drive:** Wells Fargo Campus 2024
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
- **College/Drive:** Off-Campus Drive 2024
- **Problem Statement:** Find contiguous subarray with maximum sum.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Number of Islands (2D Grid BFS)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Count connected components of 1s in binary matrix.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Complexity:** $O(M \times N)$ Time.

#### 7. Isomorphic Strings
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Determine if two strings are isomorphic.
- **LeetCode Equivalent:** [205. Isomorphic Strings](https://leetcode.com/problems/isomorphic-strings/)
- **Complexity:** $O(N)$ Time.

#### 8. Merge Intervals
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Merge overlapping transaction intervals.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time.

#### 9. Valid Parentheses
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Stack balanced brackets check.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Complexity:** $O(N)$ Time.

#### 10. Coin Change (Fewest Coins)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Minimum coins to make change.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time.
