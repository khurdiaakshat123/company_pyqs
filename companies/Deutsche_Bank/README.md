# Deutsche Bank Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerEarth**
- **Test Duration:** 90 to 105 minutes
- **Structure Breakdown:**
  1. **Technical MCQs Section (30 mins):** 20 MCQs covering SQL/DBMS, Java fundamentals, Operating Systems, and Financial/Quantitative Aptitude.
  2. **Coding Section (60 mins, 2 to 3 Questions):** Algorithmic problem-solving (Medium difficulty).
- **Passing Cutoff:** Full clearance on at least 1.5 coding questions + high score in SQL/DBMS MCQs (>75%).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Dynamic Programming:** Stock profit series, 0/1 knapsack, coin change, grid paths with obstacles.
- **SQL Queries & Window Functions:** `DENSE_RANK()`, `LEAD()`, `LAG()`, consecutive transaction days, self-joins.
- **Arrays & Two Pointers:** Running balance, interval merging, maximum profit, jump game.
- **Graph Traversals:** Currency conversion cycles, BFS shortest path, connected networks, evaluate division.
- **HashMaps & Frequency Counters:** Anagram pairs, subarray sums, longest consecutive sequence.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Best Time to Buy and Sell Stock with Transaction Fee
- **College/Drive:** BITS Pilani / Pune University 2024
- **Problem Summary:** You are given an array `prices` where `prices[i]` is the price of a given stock on the $i$-th day, and an integer `fee` representing a transaction fee. Find the maximum profit you can achieve.
- **LeetCode Equivalent:** [714. Best Time to Buy and Sell Stock with Transaction Fee](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-transaction-fee/)
- **Approach:** State DP with two variables: `cash` (max profit not holding stock) and `hold` (max profit holding stock).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Currency Conversion Arbitrage / Evaluate Division
- **College/Drive:** NIT Surat / DTU 2024
- **Problem Summary:** Given a list of currency exchange rates `(curr1, curr2, rate)`, compute the conversion rate from an arbitrary currency $A$ to $B$. Return $-1.0$ if no path exists.
- **LeetCode Equivalent:** [399. Evaluate Division](https://leetcode.com/problems/evaluate-division/)
- **Approach:** Graph construction where edge weight is `rate`, query solved via BFS/DFS or Disjoint Set Union with weights.
- **Complexity:** $O(Q \times (V + E))$ Time.

#### 3. Real SQL Challenge: Consecutive Transaction Days
- **College/Drive:** Deutsche Bank Graduate Scheme 2024
- **Problem Summary:** Write a query to find all users who made transactions on at least 3 consecutive calendar days.
- **Approach:** Window functions `LEAD()` or `DENSE_RANK()` grouped by `user_id, transaction_date - ROW_NUMBER()`.
- **SQL Solution:**
  ```sql
  SELECT DISTINCT user_id 
  FROM (
      SELECT user_id, 
             transaction_date, 
             LAG(transaction_date, 1) OVER (PARTITION BY user_id ORDER BY transaction_date) as prev1,
             LAG(transaction_date, 2) OVER (PARTITION BY user_id ORDER BY transaction_date) as prev2
      FROM transactions
  ) t
  WHERE DATEDIFF(transaction_date, prev1) = 1 AND DATEDIFF(prev1, prev2) = 1;
  ```

#### 4. Jump Game II (Minimum Steps to Reach Target)
- **College/Drive:** IIIT Bangalore / VIT 2024
- **Problem Summary:** Given a 0-indexed array of integers `nums` of length $n$, return the minimum number of jumps to reach $n - 1$.
- **LeetCode Equivalent:** [45. Jump Game II](https://leetcode.com/problems/jump-game-ii/)
- **Approach:** Greedy BFS level-by-level window tracking `farthest` reachable index.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Partition Equal Subset Sum (0/1 Knapsack)
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Determine if integer array can be partitioned into two subsets with equal sum.
- **LeetCode Equivalent:** [416. Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum/)
- **Approach:** 1D boolean DP array targeting `sum / 2`.
- **Complexity:** $O(N \times \text{target})$ Time, $O(\text{target})$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Minimum Path Sum in Grid
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Find path from top-left to bottom-right of matrix minimizing sum of numbers along path.
- **LeetCode Equivalent:** [64. Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/)
- **Approach:** 2D DP table: `dp[i][j] = grid[i][j] + min(dp[i-1][j], dp[i][j-1])`.
- **Complexity:** $O(M \times N)$ Time, $O(N)$ Space.

#### 7. Merge Intervals / Trade Blotter Reconciliation
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Merge all overlapping execution intervals.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 8. Valid Parenthesis String (With Asterisk Wildcards)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Verify validity of parentheses string where `'*'` can be treated as `'('`, `')'`, or empty.
- **LeetCode Equivalent:** [678. Valid Parenthesis String](https://leetcode.com/problems/valid-parenthesis-string/)
- **Approach:** Range of open parentheses `[low, high]` tracking.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Lowest Common Ancestor in Binary Tree
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Find lowest common ancestor node in binary tree.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 10. Longest Consecutive Sequence
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Find length of longest sequence of consecutive integers in unsorted array.
- **LeetCode Equivalent:** [128. Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/)
- **Approach:** Hash Set lookup; only build streak if `val - 1` is absent.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

## 🧠 Frequent SQL & Core CS MCQs in Deutsche Bank OA
1. **Window Function `DENSE_RANK()` vs `RANK()`:**
   - How does `DENSE_RANK()` differ from `RANK()` when ties occur?
   - *Answer:* `RANK()` leaves gaps in rank numbering after ties (e.g. 1, 2, 2, 4), while `DENSE_RANK()` produces continuous rank numbering without gaps (e.g. 1, 2, 2, 3).
2. **Transaction Isolation & Dirty Reads:**
   - Which SQL isolation level allows dirty reads?
   - *Answer:* `READ UNCOMMITTED`. Under `READ COMMITTED` and higher levels, dirty reads are strictly prevented.
