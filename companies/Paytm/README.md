# Paytm Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 📱

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **CoCubes**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  - **Section 1: Algorithmic Coding (60 mins, 2 to 3 Questions)** – Medium to Hard difficulty problems.
  - **Section 2: Core CS & SQL MCQs (30 mins)** – 15 to 20 MCQs covering Operating Systems, DBMS (ACID, Normalization), Advanced Java/OOPs, and Practical SQL queries.
- **Passing Benchmark:** Solving 2 coding problems completely + high score on SQL and DBMS MCQs.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Dynamic Programming:** Edit distance, coin change, longest increasing subsequence, house robber.
- **Graphs & Shortest Path:** Dijkstra, BFS reachability in transaction networks, course schedule.
- **Subarrays & Two Pointers:** Subarray sum divisible by K, sliding window maximum, container with most water.
- **Advanced SQL:** Window functions (`DENSE_RANK()`, `ROW_NUMBER()`), recursive CTEs, grouping with having.
- **Stacks & Queues:** Daily temperatures, valid parentheses, monotonic deque.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Transaction Reconciliation Edit Distance
- **College/Drive:** DTU / NSUT / NIT Delhi 2024–2025
- **Problem Summary:** Given two transaction log strings `word1` and `word2`, return the minimum number of operations required to convert `word1` to `word2` (insert, delete, or replace character).
- **Constraints:** $0 \le |word1|, |word2| \le 500$.
- **LeetCode Equivalent:** [72. Edit Distance](https://leetcode.com/problems/edit-distance/)
- **Approach:** 2D Dynamic Programming:
  $$dp[i][j] = \begin{cases} dp[i-1][j-1] & \text{if } word1[i-1] == word2[j-1] \\ 1 + \min(dp[i-1][j], dp[i][j-1], dp[i-1][j-1]) & \text{otherwise} \end{cases}$$
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 2. Payment Gateway Latency Optimization (Dijkstra)
- **College/Drive:** BITS Pilani 2024–2025
- **Problem Summary:** A payments processing network has $N$ servers connected by weighted bidirectional links representing network ping times. A payment confirmation must reach all servers from origin $S$. Find the shortest time for all servers to confirm, or return -1 if any server is unreachable.
- **Constraints:** $1 \le N \le 100$, $1 \le edges \le 6000$.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's Algorithm using Min-Heap (`std::priority_queue`).
- **Complexity:** $O(E \log V)$ Time.

#### 3. Subarray Sums Divisible by K
- **College/Drive:** NIT Allahabad 2024–2025
- **Problem Summary:** Given an array of integers `nums` and an integer $k$, return the number of non-empty subarrays that have a sum divisible by $k$.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$, $2 \le k \le 10^4$.
- **LeetCode Equivalent:** [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- **Approach:** Prefix Sum modulo $k$ stored in a Hash Map.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 4. Real SQL Question: Top 3 Spending Users per Merchant
- **College/Drive:** Off-Campus Drive 2024–2025
- **Problem Summary:** Write a query to find the top 3 highest spending customers for each merchant category during Diwali sales 2024.
- **SQL Implementation:**
  ```sql
  WITH CustomerSpending AS (
      SELECT merchant_id, user_id, SUM(amount) as total_spent,
             DENSE_RANK() OVER (PARTITION BY merchant_id ORDER BY SUM(amount) DESC) as rnk
      FROM Transactions
      WHERE transaction_date BETWEEN '2024-10-20' AND '2024-11-05'
      GROUP BY merchant_id, user_id
  )
  SELECT merchant_id, user_id, total_spent
  FROM CustomerSpending
  WHERE rnk <= 3;
  ```

#### 5. Longest Increasing Subsequence
- **College/Drive:** Campus Drive Slot 1 (2024–2025)
- **Problem Summary:** Find length of longest strictly increasing subsequence.
- **Constraints:** $1 \le nums.length \le 2500$.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Approach:** Patience sorting with binary search (`std::lower_bound`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 6. Coin Change (Fewest Denominations)
- **College/Drive:** Campus Drive Slot 2 (2024)
- **Problem Summary:** Fewest coins to make payment amount.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 7. Sliding Window Maximum
- **College/Drive:** Off-Campus Drive 2024
- **Problem Summary:** Maximum transaction in every sliding window of size $K$.
- **Constraints:** $1 \le nums.length \le 10^5$, $1 \le k \le nums.length$.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Approach:** Monotonic Decreasing Deque storing indices.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 8. Container With Most Water
- **College/Drive:** Campus Hiring 2024
- **Problem Summary:** Maximize water container between vertical lines.
- **Constraints:** $2 \le heights.length \le 10^5$.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Approach:** Two pointers moving shorter bar inwards.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Subarray Sum Equals K
- **College/Drive:** Paytm Noida Screening 2024
- **Problem Summary:** Count total continuous subarrays whose sum equals $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency counter.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Campus Slot 2024
- **Problem Summary:** Minimum minutes to infect all items in 2D grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Course Schedule II (Topological Sort)
- **College/Drive:** Campus Drive 2023–2024
- **Problem Summary:** Order tasks given dependencies.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm using indegrees and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 12. Daily Temperatures / Transaction Spikes
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Find days to wait for a higher value.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 13. Merge Intervals / Settlement Batches
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Merge all overlapping settlement intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time; merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 14. Trapping Rain Water
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 15. Valid Parentheses
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Check if string brackets are balanced.
- **Constraints:** $1 \le s.length \le 10^4$.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Stack matching opening with closing brackets.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 16. Product of Array Except Self without Division
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
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

#### 20. Best Time to Buy and Sell Stock
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Maximize profit with a single transaction.
- **Constraints:** $1 \le prices.length \le 10^5$.
- **LeetCode Equivalent:** [121. Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent CS Fundamentals & SQL MCQs in Paytm OA
1. **Database Indexing & Range Lookups:**
   - Why are B+ Trees preferred over Hash Indexes in relational databases?
   - *Answer:* Hash Indexes only support point lookups ($=$) in $O(1)$ time, but cannot support range queries ($<$, $>$, `BETWEEN`). B+ Trees maintain sorted order at the leaf level, allowing efficient $O(\log N + K)$ range scans.
2. **ACID Durability vs In-Memory Caching:**
   - How does Redis achieve durability for financial state caching?
   - *Answer:* Via RDB snapshots (point-in-time point dumps) and AOF (Append Only File) logging which logs every write operation received by the server.
3. **Database Deadlocks in High-Concurrency Wallets:**
   - How can you design account transfer transactions between User A and User B to prevent deadlocks?
   - *Answer:* Always acquire locks on accounts in a globally deterministic order (e.g. `ORDER BY account_id`), ensuring no two concurrent transactions attempt to lock account A then B while another locks B then A.
