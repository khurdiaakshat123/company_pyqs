# Citi (Citigroup) Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **HackerEarth**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Technical & SQL Quiz (30 mins)** – 15 to 20 MCQs covering SQL Queries, Database Normalization, Java/C++ OOP Concepts (Polymorphism, Inheritance, Exception handling), and Computer Networks.
  2. **Section 2: Coding Assessment (60 mins, 2 Questions):**
     - Question 1: Easy to Medium (Strings, Arrays, Two Pointers)
     - Question 2: Medium (Graph traversals, Dynamic Programming, or 2D Matrix paths)
- **Passing Cutoff:** Full clearance on at least 1 coding question + substantial test cases on the 2nd + high accuracy on the SQL/OOP section.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | SQL Queries & Database MCQs | Medium | Complex joins, window functions (`RANK()`, `ROW_NUMBER()`), subqueries, ACID |
| **Very High** | Arrays & Two Pointers | Easy - Medium | Subarray sums, palindrome verification, interval scheduling |
| **High** | Java & OOP Fundamentals | Medium | Abstract classes vs interfaces, Java Collections, thread states, immutability |
| **High** | Graph & Matrix Traversals | Medium | Number of islands, grid path counting, cycle detection |
| **Medium** | Dynamic Programming | Medium | Coin change, minimum path sum, house robber |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Count Number of Islands (Citi Classic)
- **Problem Summary:** Given an $m \times n$ 2D binary grid `grid` which represents a map of `'1'`s (land) and `'0'`s (water), return the number of islands. An island is surrounded by water and is formed by connecting adjacent lands horizontally or vertically.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Approach:** Standard BFS or DFS marking visited land cells in-place with `'0'`.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

### 2. Valid Palindrome with at most One Deletion
- **Problem Summary:** Given a string $s$, return true if the $s$ can be palindrome after deleting at most one character from it.
- **LeetCode Equivalent:** [680. Valid Palindrome II](https://leetcode.com/problems/valid-palindrome-ii/)
- **Approach:** Two pointers from left and right. When mismatch occurs at $(i, j)$, check if $s[i+1 \dots j]$ or $s[i \dots j-1]$ is a palindrome.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 3. Real SQL Question: Customers with Zero Recent Orders
- **Problem Summary:** Write a query to find the names of all customers who have not placed an order in the last 180 days.
- **SQL Implementation:**
  ```sql
  SELECT c.customer_name
  FROM Customers c
  LEFT JOIN Orders o ON c.customer_id = o.customer_id
                     AND o.order_date >= CURRENT_DATE - INTERVAL '180 days'
  WHERE o.order_id IS NULL;
  ```

### 4. Coin Change / Currency Payment Combination
- **Problem Summary:** Return the fewest number of coins that you need to make up a payment amount.
- **Complexity:** $O(N \times \text{amount})$ Time, $O(\text{amount})$ Space.
