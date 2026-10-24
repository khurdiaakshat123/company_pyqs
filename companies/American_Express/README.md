# American Express (Amex) Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) 💳

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerEarth** / **Aon CoCubes**
- **Test Duration:** 90 to 105 minutes
- **Structure Breakdown:**
  1. **Technical MCQs:** 15 to 20 Questions covering Data Structures, SQL/DBMS, OS, and Probability/Aptitude (30 mins).
  2. **Coding Section:** 2 to 3 Coding Questions (Medium difficulty, 60–75 mins).
- **Passing Cutoff:** Full score on at least 1.5 coding questions + high accuracy on SQL and DBMS MCQs is required for interview calls.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Dynamic Programming:** Subset sum, maximum points from cards, knapsack variants, bounded transfers, 2D minimum path sum.
- **Arrays & Prefix Sums:** Subarray sum divisible by K, running balance tracking, interval scheduling, prefix products.
- **SQL Queries & Database MCQs:** Joins, group by with having, window functions (`RANK()`, `DENSE_RANK()`), ACID, transaction rollback.
- **Strings & HashMaps:** Substring matching, frequency maps, group anagrams, sliding window.
- **Graph Reachability:** Connected components, BFS path checking, course schedule cycle check.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Maximum Score from Card Points (Amex Classic)
- **College/Drive:** IIT Roorkee / BITS Pilani 2024–2025
- **Problem Summary:** In one step, you can take one card from the beginning or from the end of the row. You have to take exactly $k$ cards. Return the maximum score you can obtain.
- **Constraints:** $1 \le cardPoints.length \le 10^5$, $1 \le k \le cardPoints.length$.
- **LeetCode Equivalent:** [1423. Maximum Points You Can Obtain from Cards](https://leetcode.com/problems/maximum-points-you-can-obtain-from-cards/)
- **Approach:** Sliding window of size $N - k$. Find the contiguous subarray of size $N - k$ with the minimum sum, then subtract it from total points.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Subarray Sums Divisible by K
- **College/Drive:** NIT Trichy / DTU 2024–2025
- **Problem Summary:** Given an integer array `nums` and an integer $k$, return the number of non-empty subarrays that have a sum divisible by $k$.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$, $2 \le k \le 10^4$.
- **LeetCode Equivalent:** [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- **Approach:** Prefix sums with modulo arithmetic: `rem = ((sum % k) + k) % k`. Count frequency of each remainder using a HashMap.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 3. Credit Card Fraud Detection / Anomaly Detection
- **College/Drive:** IIIT Allahabad 2024–2025
- **Problem Summary:** Given a stream of transactions `[amount, timestamp, city]`, flag any transaction where an amount $\ge 1000$ occurs or where two transactions in different cities occur within 60 minutes.
- **Constraints:** $1 \le transactions.length \le 10^4$.
- **Approach:** Sort by timestamp, maintain a sliding window of transactions for each cardholder ID using Hash Maps.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 4. Coin Change II / Transaction Combinations
- **College/Drive:** Off-Campus Drive 2024–2025
- **Problem Summary:** Return the number of combinations that make up that amount with given coins.
- **Constraints:** $1 \le amount \le 5000$, $1 \le coins.length \le 300$.
- **LeetCode Equivalent:** [518. Coin Change II](https://leetcode.com/problems/coin-change-ii/)
- **Approach:** Unbounded Knapsack DP: iterate coins on outer loop, amount on inner loop: `dp[w] += dp[w - coin]`.
- **Complexity:** $O(N \times \text{amount})$ Time, $O(\text{amount})$ Space.

#### 5. Real SQL Question: Third Highest Transaction per User
- **College/Drive:** Amex Campus 2024–2025
- **SQL Implementation:**
  ```sql
  WITH RankedTransactions AS (
      SELECT user_id, amount,
             DENSE_RANK() OVER (PARTITION BY user_id ORDER BY amount DESC) as rnk
      FROM Transactions
  )
  SELECT user_id, amount FROM RankedTransactions WHERE rnk = 3;
  ```

#### 6. Subarray Sum Equals K
- **College/Drive:** Amex Gurgaon Drive 2024
- **Problem Summary:** Total contiguous periods where net transactions sum to $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sum frequencies stored in Hash Map.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Minimum Path Sum in Grid (2D DP)
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Find minimum cost path from top-left to bottom-right in $M \times N$ matrix.
- **Constraints:** $M, N \le 200$.
- **LeetCode Equivalent:** [64. Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/)
- **Approach:** 2D DP: `dp[i][j] = grid[i][j] + min(dp[i-1][j], dp[i][j-1])`.
- **Complexity:** $O(M \times N)$ Time, $O(N)$ Space.

#### 8. Course Schedule (Topological Sort)
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** Determine if workflow tasks can be scheduled without cyclic deadlocks.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Kahn's Algorithm for Topological Sort using indegrees.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 9. Daily Temperatures / Transaction Spikes
- **College/Drive:** Campus Slot 2024
- **Problem Summary:** Find days to wait for a warmer transaction day.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Valid Parentheses
- **College/Drive:** Off-Campus Screening 2024
- **Problem Summary:** Check if string brackets are balanced.
- **Constraints:** $1 \le s.length \le 10^4$.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Stack matching opening with closing brackets.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Group Anagrams
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Group strings that are anagrams.
- **Constraints:** $1 \le strs.length \le 10^4$.
- **LeetCode Equivalent:** [49. Group Anagrams](https://leetcode.com/problems/group-anagrams/)
- **Approach:** Character frequency array or sorted string as hash key.
- **Complexity:** $O(N \cdot K \log K)$ Time.

#### 12. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Sliding window with hash map storing last seen indices.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

#### 13. Merge Intervals
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Merge overlapping transaction settlement times.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time; merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 14. Number of Islands
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** BFS/DFS on 2D grid matrix to count connected components.
- **Constraints:** $M, N \le 300$.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Complexity:** $O(M \times N)$ Time.

#### 15. Maximum Subarray Sum (Kadane's)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Maximum contiguous subarray sum.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. Product of Array Except Self
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Compute array product except self without division in $O(N)$ time.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 17. Container With Most Water
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Two pointers inward maximizing area between vertical lines.
- **Constraints:** $2 \le heights.length \le 10^5$.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 18. Best Time to Buy and Sell Stock
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Maximize profit with a single transaction.
- **Constraints:** $1 \le prices.length \le 10^5$.
- **LeetCode Equivalent:** [121. Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 19. Two Sum
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Return indices of two numbers that add up to target.
- **Constraints:** $2 \le nums.length \le 10^4$.
- **LeetCode Equivalent:** [1. Two Sum](https://leetcode.com/problems/two-sum/)
- **Approach:** Hash Map lookup for `target - num`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 20. Search in Rotated Sorted Array
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find target in rotated sorted array in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 5000$.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking sorted half.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent Database & Systems Questions in Amex OA
1. **Window Functions vs GROUP BY:**
   - What is the fundamental difference between `GROUP BY` and a Window Function (`OVER (PARTITION BY ...)` )?
   - *Answer:* `GROUP BY` collapses multiple rows into a single summary row for each group, while a window function calculates an aggregate over a subset of rows without collapsing the underlying individual rows.
2. **Transaction Isolation Levels:**
   - Which anomaly does `READ COMMITTED` prevent, and which anomaly can still occur?
   - *Answer:* `READ COMMITTED` prevents Dirty Reads (reading uncommitted data). However, Non-Repeatable Reads (reading different values of the same row during the same transaction) and Phantom Reads can still occur.
3. **Database Sharding vs Partitioning:**
   - What is the difference between horizontal partitioning and database sharding?
   - *Answer:* Horizontal partitioning divides a large table into smaller physical partitions on the same database instance/server. Sharding distributes partitions across multiple independent database servers/nodes across a network.
