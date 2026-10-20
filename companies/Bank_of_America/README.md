# Bank of America (BofA) Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **Codility**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  1. **Coding Section:** 2 Coding Problems (LeetCode Easy to Medium difficulty, 45–60 mins).
  2. **Core CS & SQL Section:** 10 to 15 MCQs covering SQL Queries, DBMS Normalization, Operating Systems, OOPs principles, and Quantitative Aptitude (20–30 mins).
- **Passing Cutoff:** 100% test cases cleared on both coding questions + solid performance on SQL/DBMS MCQs.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Strings & Frequency Counting | Easy - Medium | Anagrams, unique characters, palindrome checks, word frequencies |
| **Very High** | Arrays & Two Pointers | Easy - Medium | Running sum, balance index, pair target sum, move zeros |
| **High** | SQL Queries & DBMS MCQs | Medium | Aggregate functions, joins, subqueries, group by with having |
| **High** | Sliding Window & Intervals | Easy - Medium | Maximum sum subarray of size K, merging time slots |
| **Medium** | Trees & Binary Search Trees | Easy - Medium | Invert binary tree, path sum, level order traversal |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Invert Binary Tree
- **Problem Summary:** Given the root of a binary tree, invert the tree, and return its root.
- **LeetCode Equivalent:** [226. Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/)
- **Approach:** Recursive DFS swapping left and right child pointers at each node.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

### 2. First Unique Character in a String (Financial Transaction ID)
- **Problem Summary:** Given a string $s$, find the first non-repeating character in it and return its index. If it does not exist, return -1.
- **LeetCode Equivalent:** [387. First Unique Character in a String](https://leetcode.com/problems/first-unique-character-in-a-string/)
- **Approach:** 26-element character frequency array; two-pass scan.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

### 3. Maximum Average Subarray I
- **Problem Summary:** You are given an integer array `nums` consisting of $n$ elements, and an integer $k$. Find a contiguous subarray whose length is equal to $k$ that has the maximum average value and return this value.
- **LeetCode Equivalent:** [643. Maximum Average Subarray I](https://leetcode.com/problems/maximum-average-subarray-i/)
- **Approach:** Fixed-size sliding window of length $k$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 4. Real SQL Question: Account Holder Running Total
- **Problem Summary:** Write a query to calculate the cumulative running total of deposits for each account holder over time.
- **SQL Implementation:**
  ```sql
  SELECT account_id, transaction_date, amount,
         SUM(amount) OVER (PARTITION BY account_id ORDER BY transaction_date ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW) as running_balance
  FROM Transactions;
  ```
