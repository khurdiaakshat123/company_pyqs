# Wells Fargo Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🏦

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 75 to 90 minutes
- **Structure Breakdown:**
  1. **Coding Section:** 2 Coding Questions (LeetCode Easy to Medium difficulty, 45 mins).
  2. **SQL Query Challenge:** 1 Practical SQL Query (Intermediate to Advanced, 15 mins).
  3. **Core CS & Aptitude Section:** 10 to 15 MCQs covering Database Systems, Operating Systems, OOPs concepts, and Quantitative/Verbal Aptitude (20 mins).
- **Passing Cutoff:** Full score on the SQL query is often a hard requirement alongside at least 1.5 coding questions cleared.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | SQL Queries | Medium | Window functions (`DENSE_RANK()`, `ROW_NUMBER()`), `GROUP BY`, `HAVING`, Self-joins |
| **Very High** | Arrays & Two Pointers | Easy - Medium | Sliding window, subarray sums, element removal, running balance |
| **High** | Strings & HashMaps | Easy - Medium | Frequency maps, isomorphic strings, longest substring without repeats |
| **High** | Grid Traversals (BFS / DFS) | Medium | Matrix paths, island count, shortest path in binary matrix |
| **Medium** | Stack / Queue Operations | Easy - Medium | Balanced brackets, next greater element |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Longest Substring Without Repeating Characters
- **Problem Summary:** Given a string $s$, find the length of the longest substring without repeating characters.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with a hash map storing the last seen index of each character.
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

### 2. Minimum Operations to Make Array Equal
- **Problem Summary:** You have an array `arr` of length `n` where `arr[i] = (2 * i) + 1` for all valid `i`. In one operation, you can select two indices `x` and `y` where `0 <= x, y < n` and subtract 1 from `arr[x]` and add 1 to `arr[y]`. Return the minimum number of operations needed to make all elements equal.
- **LeetCode Equivalent:** [1551. Minimum Operations to Make Array Equal](https://leetcode.com/problems/minimum-operations-to-make-array-equal/)
- **Approach:** Math formula: $\lfloor \frac{n^2}{4} \rfloor$.
- **Complexity:** $O(1)$ Time.

### 3. Shortest Path in Binary Matrix
- **Problem Summary:** Given an $n \times n$ binary matrix `grid`, return the length of the shortest clear path in the matrix. If there is no clear path, return -1 (8-directional movement permitted).
- **LeetCode Equivalent:** [1091. Shortest Path in Binary Matrix](https://leetcode.com/problems/shortest-path-in-binary-matrix/)
- **Approach:** Breadth-First Search (BFS) level traversal.
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

### 4. Real SQL Question: Department Top 3 Salaries
- **Problem Summary:** Write a solution to find the employees who are high earners in each of the departments. A high earner in a department is an employee who has a salary in the top three unique salaries for that department.
- **LeetCode Equivalent:** [185. Department Top Three Salaries](https://leetcode.com/problems/department-top-three-salaries/)
- **SQL Implementation:**
  ```sql
  WITH RankedSalaries AS (
      SELECT d.name AS Department, e.name AS Employee, e.salary AS Salary,
             DENSE_RANK() OVER (PARTITION BY e.departmentId ORDER BY e.salary DESC) AS rnk
      FROM Employee e
      JOIN Department d ON e.departmentId = d.id
  )
  SELECT Department, Employee, Salary
  FROM RankedSalaries
  WHERE rnk <= 3;
  ```
