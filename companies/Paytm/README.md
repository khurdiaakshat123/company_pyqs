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
- **Dynamic Programming:** Edit distance, coin change, longest increasing subsequence.
- **Graphs & Shortest Path:** Dijkstra, BFS reachability in transaction networks.
- **Subarrays & Two Pointers:** Subarray sum divisible by K, sliding window maximum.
- **Advanced SQL:** Window functions (`DENSE_RANK()`, `ROW_NUMBER()`), recursive CTEs.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Transaction Reconciliation Edit Distance
- **College/Drive:** DTU / NSUT / NIT Delhi 2024
- **Problem Statement:** Given two transaction log strings `word1` and `word2`, return the minimum number of operations required to convert `word1` to `word2` (insert, delete, or replace character).
- **LeetCode Equivalent:** [72. Edit Distance](https://leetcode.com/problems/edit-distance/)
- **Approach:** 2D Dynamic Programming:
  $$dp[i][j] = \begin{cases} dp[i-1][j-1] & \text{if } word1[i-1] == word2[j-1] \\ 1 + \min(dp[i-1][j], dp[i][j-1], dp[i-1][j-1]) & \text{otherwise} \end{cases}$$
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 2. Payment Gateway Latency Optimization (Dijkstra)
- **College/Drive:** BITS Pilani 2024
- **Problem Statement:** A payments processing network has $N$ servers connected by weighted bidirectional links representing network ping times. A payment confirmation must reach all servers from origin $S$. Find the shortest time for all servers to confirm, or return -1 if any server is unreachable.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's Algorithm using Min-Heap (`std::priority_queue`).
- **Complexity:** $O(E \log V)$ Time.

#### 3. Subarray Sums Divisible by K
- **College/Drive:** NIT Allahabad 2024
- **Problem Statement:** Given an array of integers `nums` and an integer $k$, return the number of non-empty subarrays that have a sum divisible by $k$.
- **LeetCode Equivalent:** [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- **Approach:** Prefix Sum modulo $k$ stored in a Hash Map.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 4. Real SQL Question: Top 3 Spending Users per Merchant
- **College/Drive:** Off-Campus Drive 2024
- **Problem Statement:** Write a query to find the top 3 highest spending customers for each merchant category during Diwali sales 2024.
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

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Longest Increasing Subsequence
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Find length of longest strictly increasing subsequence.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Complexity:** $O(N \log N)$ Time.

#### 6. Coin Change (Fewest Denominations)
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Fewest coins to make payment amount.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 7. Sliding Window Maximum
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Maximum transaction in every sliding window of size $K$.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Complexity:** $O(N)$ Time.

#### 8. Container With Most Water
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Maximize water container between vertical lines.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.
