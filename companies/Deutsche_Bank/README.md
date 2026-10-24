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
- **Arrays & Two Pointers:** Running balance, interval merging, maximum profit, jump game, prefix products.
- **Graph Traversals:** Currency conversion cycles, BFS shortest path, connected networks, evaluate division.
- **HashMaps & Frequency Counters:** Anagram pairs, subarray sums, longest consecutive sequence.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Best Time to Buy and Sell Stock with Transaction Fee
- **College/Drive:** BITS Pilani / Pune University 2024–2025
- **Problem Summary:** You are given an array `prices` where `prices[i]` is the price of a given stock on the $i$-th day, and an integer `fee` representing a transaction fee. Find the maximum profit you can achieve.
- **Constraints:** $1 \le prices.length \le 5 \times 10^4$, $1 \le prices[i] \le 5 \times 10^4$, $0 \le fee \le 10^4$.
- **LeetCode Equivalent:** [714. Best Time to Buy and Sell Stock with Transaction Fee](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-transaction-fee/)
- **Approach:** State DP with two variables: `cash` (max profit not holding stock) and `hold` (max profit holding stock).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Currency Conversion Arbitrage / Evaluate Division
- **College/Drive:** NIT Surat / DTU 2024–2025
- **Problem Summary:** Given a list of currency exchange rates `(curr1, curr2, rate)`, compute the conversion rate from an arbitrary currency $A$ to $B$. Return $-1.0$ if no path exists.
- **Constraints:** Equations $\le 20$, queries $\le 20$.
- **LeetCode Equivalent:** [399. Evaluate Division](https://leetcode.com/problems/evaluate-division/)
- **Approach:** Graph construction where edge weight is `rate`, query solved via BFS/DFS or Disjoint Set Union with weights.
- **Complexity:** $O(Q \times (V + E))$ Time.

#### 3. Real SQL Challenge: Consecutive Transaction Days
- **College/Drive:** Deutsche Bank Graduate Scheme 2024–2025
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
- **College/Drive:** IIIT Bangalore / VIT 2024–2025
- **Problem Summary:** Given a 0-indexed array of integers `nums` of length $n$, return the minimum number of jumps to reach $n - 1$.
- **Constraints:** $1 \le nums.length \le 10^4$.
- **LeetCode Equivalent:** [45. Jump Game II](https://leetcode.com/problems/jump-game-ii/)
- **Approach:** Greedy BFS level-by-level window tracking `farthest` reachable index.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Partition Equal Subset Sum (0/1 Knapsack)
- **College/Drive:** Campus Drive 2024–2025
- **Problem Summary:** Determine if integer array can be partitioned into two subsets with equal sum.
- **Constraints:** $1 \le nums.length \le 200$.
- **LeetCode Equivalent:** [416. Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum/)
- **Approach:** 1D boolean DP array targeting `sum / 2`.
- **Complexity:** $O(N \times \text{target})$ Time, $O(\text{target})$ Space.

#### 6. Subarray Sum Equals K
- **College/Drive:** Deutsche Bank Pune Slot 2024
- **Problem Summary:** Find total continuous periods where net transactions sum to $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sum frequencies stored in Hash Map.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Course Schedule (Cycle Detection)
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** Determine if candidate can finish all courses given prerequisite pairs.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Kahn's Algorithm (BFS topological sort indegrees).
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 8. Daily Temperatures / Transaction Spikes
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Find days to wait for a warmer transaction day.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 9. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Compute minimum time for contagion to spread across entire 2D matrix.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 10. Coin Change (Fewest Coins)
- **College/Drive:** Off-Campus Screening 2024
- **Problem Summary:** Find minimum number of coins to make up given amount.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Minimum Path Sum in Grid
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Find path from top-left to bottom-right of matrix minimizing sum of numbers along path.
- **Constraints:** $1 \le M, N \le 200$.
- **LeetCode Equivalent:** [64. Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/)
- **Approach:** 2D DP table: `dp[i][j] = grid[i][j] + min(dp[i-1][j], dp[i][j-1])`.
- **Complexity:** $O(M \times N)$ Time, $O(N)$ Space.

#### 12. Merge Intervals / Trade Blotter Reconciliation
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Merge all overlapping execution intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 13. Valid Parenthesis String (With Asterisk Wildcards)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Verify validity of parentheses string where `'*'` can be treated as `'('`, `')'`, or empty.
- **Constraints:** $1 \le s.length \le 100$.
- **LeetCode Equivalent:** [678. Valid Parenthesis String](https://leetcode.com/problems/valid-parenthesis-string/)
- **Approach:** Range of open parentheses `[low, high]` tracking.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 14. Lowest Common Ancestor in Binary Tree
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Find lowest common ancestor node in binary tree.
- **Constraints:** Nodes $\le 10^5$.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 15. Longest Consecutive Sequence
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Find length of longest sequence of consecutive integers in unsorted array.
- **Constraints:** $0 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [128. Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/)
- **Approach:** Hash Set lookup; only build streak if `val - 1` is absent.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 16. Product of Array Except Self without Division
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Return array where `output[i]` is product of all elements except `nums[i]`.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 17. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Sliding window with hash map storing last seen indices.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

#### 18. House Robber (1D Dynamic Programming)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Maximize stolen value without robbing two adjacent houses.
- **Constraints:** $1 \le nums.length \le 100$.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** DP: `dp[i] = max(dp[i-1], dp[i-2] + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 19. Search in Rotated Sorted Array
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Find target in rotated sorted array in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 5000$.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking sorted half.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 20. Container With Most Water
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Two pointers inward maximizing area between vertical lines.
- **Constraints:** $2 \le heights.length \le 10^5$.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent SQL & Core CS MCQs in Deutsche Bank OA
1. **Window Function `DENSE_RANK()` vs `RANK()`:**
   - How does `DENSE_RANK()` differ from `RANK()` when ties occur?
   - *Answer:* `RANK()` leaves gaps in rank numbering after ties (e.g. 1, 2, 2, 4), while `DENSE_RANK()` produces continuous rank numbering without gaps (e.g. 1, 2, 2, 3).
2. **Transaction Isolation & Dirty Reads:**
   - Which SQL isolation level allows dirty reads?
   - *Answer:* `READ UNCOMMITTED`. Under `READ COMMITTED` and higher levels, dirty reads are strictly prevented.
3. **Database Normalization (3NF vs BCNF):**
   - What makes BCNF stricter than 3NF?
   - *Answer:* In BCNF (Boyce-Codd Normal Form), for every non-trivial functional dependency $X \to Y$, $X$ must be a superkey. 3NF allows $Y$ to be a prime attribute (part of candidate key) even if $X$ is not a superkey.
