# IBM Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🔵

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  1. **Coding Assessment:** 1 to 2 Coding Challenges (Easy to Medium difficulty, 45 mins).
  2. **Core CS & Technical MCQs:** 15 to 20 MCQs covering SQL Queries, DBMS Normalization, Operating Systems, Computer Networks, and OOPs (30 mins).
  3. **Code Debugging / Bug-Fixing Track:** (In select drives) 3 to 5 short code snippets where candidates find and fix syntax/logical bugs.
- **Passing Cutoff:** High passing benchmark for coding (100% test cases) combined with $\ge 75\%$ on technical MCQs.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Arrays & Contiguous Subarrays:** Binary arrays (0s and 1s), prefix sums, balance points, Kadane's algorithm.
- **SQL Queries & DBMS:** Aggregate functions, joins, subqueries, group by with having, window functions (`LAG`, `LEAD`).
- **Strings & Character Counting:** Substring frequencies, anagrams, compression, alternating binary strings.
- **Interval Scheduling & Server Logs:** Peak server load, event simulation, start/end timestamps.
- **Trees & Linked Lists:** Level-order traversal, tree inversion, cycle detection, reverse linked list.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Maximum Contiguous Subarray of Equal 0s and 1s (IBM Classic)
- **College/Drive:** Pan-India Campus Drive 2024
- **Problem Summary:** Given a binary array `nums`, return the maximum length of a contiguous subarray with an equal number of 0 and 1.
- **LeetCode Equivalent:** [525. Contiguous Array](https://leetcode.com/problems/contiguous-array/)
- **Approach:** Transform all `0`s to `-1`. The problem reduces to finding the longest subarray with sum equal to 0. Maintain a HashMap of `prefix_sum -> first_occurrence_index`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 2. Peak Active Server Logs (Interval Overlap)
- **College/Drive:** IBM ASE On-Campus 2024
- **Problem Summary:** You are given server startup logs consisting of pairs `[start_time, end_time]`. Find the maximum number of servers actively running at any single point in time.
- **Approach:** Separate start and end times into two arrays, sort both, use two pointers to count concurrent active servers.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 3. Slope-Finding in Coordinate Trajectory
- **College/Drive:** National Pool Campus 2024
- **Problem Summary:** Given an array of 2D coordinates representing sensor measurements, find the length of the longest contiguous subsegment where the slope between successive points is strictly positive.
- **Approach:** Linear scan calculating $\frac{y_i - y_{i-1}}{x_i - x_{i-1}} > 0$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Minimum Replacements to Make String Alternating
- **College/Drive:** Off-Campus Drive 2024
- **Problem Summary:** Given a string $s$ of `0`s and `1`s, find the minimum number of character flips needed to make the string alternating (e.g. `"010101..."` or `"101010..."`).
- **LeetCode Equivalent:** [1758. Minimum Changes To Make Alternating Binary String](https://leetcode.com/problems/minimum-changes-to-make-alternating-binary-string/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Real SQL Question: Department Headcount and High Salary Ratio
- **College/Drive:** Campus Placement 2024
- **Problem Statement:** Write a query to find department names with more than 10 employees where at least 20% of the employees earn above $\$100,000$.
- **SQL Implementation:**
  ```sql
  SELECT department_name, COUNT(emp_id) as total_emp,
         ROUND(100.0 * SUM(CASE WHEN salary > 100000 THEN 1 ELSE 0 END) / COUNT(emp_id), 2) as high_earner_pct
  FROM Employees
  GROUP BY department_name
  HAVING COUNT(emp_id) > 10 AND (1.0 * SUM(CASE WHEN salary > 100000 THEN 1 ELSE 0 END) / COUNT(emp_id)) >= 0.20;
  ```

#### 6. Longest Substring Without Repeating Characters
- **College/Drive:** VIT Vellore / SRM 2024
- **Problem Summary:** Given a string `s`, find the length of the longest substring without duplicate characters.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with hash map storing character positions.
- **Complexity:** $O(N)$ Time.

#### 7. Trapping Rain Water (Tech Expert Track)
- **College/Drive:** Manipal Institute of Technology 2024
- **Problem Summary:** Compute total water trapped by elevation profile after rain.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers from left and right inward.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Subarray Sum Equals K
- **College/Drive:** Pan-India Hiring 2024
- **Problem Summary:** Find total continuous subarrays whose sum equals $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency tracking.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 9. Search in Rotated Sorted Array
- **College/Drive:** IBM Off-Campus 2024
- **Problem Summary:** Find target in circularly rotated sorted array.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking sorted half.
- **Complexity:** $O(\log N)$ Time.

#### 10. Valid Parentheses Expression
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Verify that brackets in expression are properly closed.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Stack data structure.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Missing Number in Sequence
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Find missing number from 0 to $N$.
- **LeetCode Equivalent:** [268. Missing Number](https://leetcode.com/problems/missing-number/)
- **Complexity:** $O(N)$ Time.

#### 12. Valid Anagram String Check
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Character frequency equality test.
- **LeetCode Equivalent:** [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- **Complexity:** $O(N)$ Time.

#### 13. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Contiguous subarray with highest sum.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time.

#### 14. Reverse Linked List
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Reverse singly linked list in-place.
- **LeetCode Equivalent:** [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 15. Merge Two Sorted Arrays in Place
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Merge `nums2` into `nums1` in sorted order.
- **LeetCode Equivalent:** [88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)
- **Complexity:** $O(M + N)$ Time.

#### 16. Real SQL Question: Consecutive Days Active Logins
- **College/Drive:** IBM Off-Campus 2023
- **Problem Statement:** Find user IDs who logged into the system for at least 3 consecutive days.
- **SQL Implementation:**
  ```sql
  WITH DistinctLogins AS (
      SELECT DISTINCT user_id, login_date FROM UserLogins
  ),
  GroupedLogins AS (
      SELECT user_id, login_date,
             login_date - (ROW_NUMBER() OVER (PARTITION BY user_id ORDER BY login_date)) * INTERVAL '1 day' AS grp
      FROM DistinctLogins
  )
  SELECT DISTINCT user_id
  FROM GroupedLogins
  GROUP BY user_id, grp
  HAVING COUNT(*) >= 3;
  ```

#### 17. Cycle Detection in Linked List
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Determine if linked list has a cycle.
- **LeetCode Equivalent:** [141. Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/)
- **Approach:** Floyd's slow and fast pointers.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 18. Two Sum (Target Pair)
- **College/Drive:** University Hiring 2023
- **Problem Statement:** Indices of two numbers adding to target.
- **LeetCode Equivalent:** [1. Two Sum](https://leetcode.com/problems/two-sum/)
- **Approach:** One-pass Hash Map.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 19. Binary Tree Level Order Traversal
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Return level-by-level traversal of binary tree nodes.
- **LeetCode Equivalent:** [102. Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/)
- **Approach:** BFS queue.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 20. Invert Binary Tree
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Mirror invert binary tree and return root.
- **LeetCode Equivalent:** [226. Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/)
- **Approach:** Recursive DFS swap `swap(root->left, root->right)`.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

---

## 🧠 Frequent CS & DBMS MCQs Asked in IBM OA
1. **Database Normalization (3NF vs BCNF):**
   - When does a relation in Third Normal Form (3NF) fail to satisfy Boyce-Codd Normal Form (BCNF)?
   - *Answer:* When there is a non-trivial functional dependency $X \to Y$ where $X$ is NOT a superkey, but $Y$ is a prime attribute (part of candidate key). 3NF permits this, but BCNF strictly requires that every determinant $X$ must be a superkey.
2. **ACID Properties (Isolation vs Consistency):**
   - Which component of a DBMS is responsible for guaranteeing Isolation, and which guarantees Atomicity and Durability?
   - *Answer:* The **Concurrency Control Manager** (using locks, 2PL, or MVCC) guarantees Isolation. The **Recovery Manager** (using write-ahead logging (WAL) and checkpoints) guarantees Atomicity and Durability.
