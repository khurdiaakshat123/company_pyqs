# Deutsche Bank Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerEarth**
- **Test Duration:** 90 to 105 minutes
- **Structure Breakdown:**
  1. **Technical MCQs Section (30 mins):** 20 MCQs covering SQL/DBMS, Java fundamentals, Operating Systems, and Financial/Quantitative Aptitude.
  2. **Coding Section (60 mins, 2 to 3 Questions):** Algorithmic problem-solving (Medium difficulty).
- **Passing Cutoff:** Full clearance on at least 1.5 coding questions + high score in SQL/DBMS MCQs.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Dynamic Programming | Medium | Stock profit series, knapsack, coin change, grid paths |
| **Very High** | SQL Queries & Window Functions | Medium | `DENSE_RANK()`, `LEAD()`, `LAG()`, subqueries, self-joins |
| **High** | Arrays & Two Pointers | Medium | Running balance, interval merging, maximum profit |
| **High** | Graph Traversals | Medium | Currency conversion cycles, BFS shortest path, connected networks |
| **Medium** | HashMaps & Frequency Counters | Easy - Medium | Anagram pairs, subarray sums, distinct elements |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Best Time to Buy and Sell Stock with Transaction Fee
- **Problem Summary:** You are given an array `prices` where `prices[i]` is the price of a given stock on the $i$-th day, and an integer `fee` representing a transaction fee. Find the maximum profit you can achieve.
- **LeetCode Equivalent:** [714. Best Time to Buy and Sell Stock with Transaction Fee](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-transaction-fee/)
- **Approach:** State DP with two variables: `cash` (max profit not holding stock) and `hold` (max profit holding stock).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 2. Currency Conversion Arbitrage
- **Problem Summary:** Given a list of currency exchange rates `(curr1, curr2, rate)`, compute the conversion rate from an arbitrary currency $A$ to $B$. Return $-1.0$ if no path exists.
- **LeetCode Equivalent:** [399. Evaluate Division](https://leetcode.com/problems/evaluate-division/)
- **Approach:** Graph construction where edge weight is `rate`, query solved via BFS/DFS or Disjoint Set Union with weights.
- **Complexity:** $O(Q \times (V + E))$ Time.

### 3. Real SQL Question: Consecutive Login / Transaction Days
- **Problem Summary:** Write a query to find all users who made transactions on at least 3 consecutive calendar days.
- **Approach:** Window functions `LEAD()` or `DENSE_RANK()` grouped by `user_id, transaction_date - ROW_NUMBER()`.

### 4. Jump Game II (Minimum Steps to Reach End)
- **Problem Summary:** You are given a 0-indexed array of integers `nums` of length $n$. Return the minimum number of jumps to reach $n - 1$.
- **LeetCode Equivalent:** [45. Jump Game II](https://leetcode.com/problems/jump-game-ii/)
- **Approach:** Greedy BFS level-by-level window tracking `farthest` reachable index.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.
