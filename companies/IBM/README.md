# IBM Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🔵

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  1. **Coding Assessment:** 1 to 2 Coding Challenges (Easy to Medium difficulty, 45 mins).
  2. **Core CS & Technical MCQs:** 15 to 20 MCQs covering SQL Queries, DBMS Normalization, Operating Systems, Computer Networks, and OOPs (30 mins).
  3. **Code Debugging / Bug-Fixing Track:** (In some drives) 3 to 5 short code snippets where candidates find and fix syntax/logical bugs.
- **Passing Cutoff:** High passing benchmark for coding (100% test cases) combined with $\ge 70\%$ on technical MCQs.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Arrays & Contiguous Subarrays | Easy - Medium | Binary arrays (0s and 1s), prefix sums, balance points |
| **Very High** | SQL Queries & DBMS | Medium | Aggregate functions, joins, subqueries, group by with having |
| **High** | Strings & Character Counting | Easy - Medium | Substring frequencies, anagrams, compression |
| **High** | Interval Scheduling & Server Logs | Medium | Peak server load, event simulation, start/end timestamps |
| **Medium** | Coordinate / Slope Monotonicity | Medium | Strictly increasing slopes, coordinate sorting |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Maximum Contiguous Subarray of Equal 0s and 1s
- **Problem Summary:** Given a binary array `nums`, return the maximum length of a contiguous subarray with an equal number of 0 and 1.
- **LeetCode Equivalent:** [525. Contiguous Array](https://leetcode.com/problems/contiguous-array/)
- **Approach:** Transform all `0`s to `-1`. The problem reduces to finding the longest subarray with sum equal to 0. Maintain a HashMap of `prefix_sum -> first_occurrence_index`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 2. Peak Active Server Logs (Interval Overlap)
- **Problem Summary:** You are given server startup logs consisting of pairs `[start_time, end_time]`. Find the maximum number of servers actively running at any single point in time.
- **Approach:** Separate start and end times into two arrays, sort both, use two pointers to count concurrent active servers.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

### 3. Slope-Finding in Coordinate Trajectory
- **Problem Summary:** Given an array of 2D coordinates representing sensor measurements, find the length of the longest contiguous subsegment where the slope between successive points is strictly positive.
- **Approach:** Linear scan calculating $\frac{y_i - y_{i-1}}{x_i - x_{i-1}} > 0$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 4. Minimum Replacements to Make String Alternating
- **Problem Summary:** Given a string $s$ of `0`s and `1`s, find the minimum number of character flips needed to make the string alternating (e.g. `"010101..."` or `"101010..."`).
- **LeetCode Equivalent:** [1758. Minimum Changes To Make Alternating Binary String](https://leetcode.com/problems/minimum-changes-to-make-alternating-binary-string/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent SQL Queries Asked in IBM OA
1. **Find Departments with More than 5 Employees:**
   ```sql
   SELECT department_name, COUNT(emp_id) AS total_employees
   FROM Employees
   GROUP BY department_name
   HAVING COUNT(emp_id) > 5;
   ```
2. **Find Duplicate Emails in Table:**
   ```sql
   SELECT email FROM Users 
   GROUP BY email 
   HAVING COUNT(email) > 1;
   ```
3. **Primary Key vs Unique Key:** A primary key automatically enforces NOT NULL and uniquely identifies a record (only 1 per table); a unique key allows NULL values and multiple unique constraints can exist per table.
