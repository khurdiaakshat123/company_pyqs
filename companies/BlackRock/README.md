# BlackRock Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Financial & Technical MCQs (30 mins):** 15 MCQs covering Data Structures, SQL, OOPs, and Financial/Quantitative calculations (portfolio returns, Sharpe ratio intuition, interest formulas).
  2. **Coding Section (60 mins, 2 Questions):** Medium difficulty algorithmic questions themed around asset allocation, transactions, and portfolio management (BlackRock Aladdin platform style).
- **Passing Cutoff:** Full score on both coding problems + high accuracy on SQL and financial/CS MCQs (>75%).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Portfolio & Transaction Simulations:** Rebalancing portfolios, rounding allocation differences, transaction matching, trade reconciliation.
- **Arrays & Sliding Window:** Subarray max/min differences, running cash flow tracking, bond maturity intervals, prefix products.
- **SQL Queries & Data Aggregation:** Aggregate portfolio value, top holdings by asset class, `DENSE_RANK()`, joins.
- **Stacks & Queues:** Next greater price, stock span, sliding window maximum.
- **Graph Reachability:** Counterparty credit risk graphs, circular debt settlement netting.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Portfolio Asset Weight Rebalancing (Aladdin Engine Core)
- **College/Drive:** BITS Pilani / IIT Roorkee 2024–2025
- **Problem Summary:** An investment portfolio holds $N$ assets with current market values $V_i$. Target percentage allocations are given as $T_i$ (where $\sum T_i = 100\%$). Calculate the exact buy/sell transaction amounts required for each asset to achieve target allocation while minimizing total transaction turnover.
- **Constraints:** $1 \le N \le 10^5$, asset values $\le 10^9$.
- **Approach:** Calculate $\text{total\_value} = \sum V_i$. For each asset, target value is $\text{total\_value} \times \frac{T_i}{100}$. Trade order is $\text{target\_value} - V_i$.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 2. Currency Rounding & Decimal Precision Balancing
- **College/Drive:** IIT BHU / NIT Surathkal 2024–2025
- **Problem Summary:** Round an array of decimal asset weights such that each rounded weight is an integer, and the sum of rounded weights strictly equals 100, while minimizing the total rounding discrepancy.
- **Constraints:** $N \le 100$, sum of weights $= 100.0$.
- **Approach:** Floor all elements, calculate remainder deficit $D = 100 - \sum \lfloor w_i \rfloor$, sort elements by fractional part descending, and increment top $D$ elements by 1.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 3. Daily Stock Prices / Next Greater Element
- **College/Drive:** DTU / NSUT 2024–2025
- **Problem Summary:** Given an array of daily stock prices, find the next day with a strictly higher price for every day in the array, or return -1 if none exists.
- **Constraints:** $1 \le n \le 10^5$.
- **LeetCode Equivalent:** [496. Next Greater Element I](https://leetcode.com/problems/next-greater-element-i/) / [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 4. Counterparty Circular Debt Settlement (Graph Debt Netting)
- **College/Drive:** BlackRock Summer Internship Drive 2024–2025
- **Problem Summary:** Given a list of transactions where person $A$ owes person $B$ an amount $X$, settle all debts using the minimum number of transactions.
- **Constraints:** Transactions $\le 1000$, distinct people $\le 12$.
- **LeetCode Equivalent:** [465. Optimal Account Balancing](https://leetcode.com/problems/optimal-account-balancing/)
- **Approach:** Compute net balance for each person. Filter non-zero balances and apply Backtracking with DFS or Bitmask DP.
- **Complexity:** $O(2^N)$ or $O(N!)$ worst case for $N \le 12$.

#### 5. Real SQL Challenge: Top 3 Asset Classes by Total Portfolio Weight
- **College/Drive:** Campus Placement Drive 2024–2025
- **Problem Summary:** Write an SQL query to retrieve the top 3 asset classes based on total held portfolio market value, showing rank and percentage contribution.
- **SQL Solution:**
  ```sql
  WITH AssetTotals AS (
      SELECT asset_class, 
             SUM(market_value) AS total_val,
             DENSE_RANK() OVER (ORDER BY SUM(market_value) DESC) as rank_pos
      FROM portfolio_holdings
      GROUP BY asset_class
  )
  SELECT asset_class, total_val, rank_pos
  FROM AssetTotals
  WHERE rank_pos <= 3;
  ```

#### 6. Stock Span Problem (Monotonic Stack)
- **College/Drive:** Campus Slot 1 (2024)
- **Problem Summary:** Compute number of consecutive days before current day where price was less than or equal to current day.
- **Constraints:** $1 \le n \le 10^5$.
- **LeetCode Equivalent:** [901. Online Stock Span](https://leetcode.com/problems/online-stock-span/)
- **Approach:** Monotonic Decreasing Stack storing pairs `(price, span)`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Merge Intervals / Bond Maturity Schedule
- **College/Drive:** Campus Slot 2 (2024)
- **Problem Summary:** Given bond holding lock-in intervals, merge overlapping intervals into unified maturity windows.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time; merge overlapping intervals.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 8. Top K Frequent Securities in Trade Log
- **College/Drive:** Off-Campus Hiring 2024
- **Problem Summary:** Return $K$ most frequent traded securities from streaming log.
- **Constraints:** $1 \le k \le \text{unique securities} \le 10^5$.
- **LeetCode Equivalent:** [347. Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/)
- **Approach:** Hash Map for counting + Min-Heap of size $K$.
- **Complexity:** $O(N \log K)$ Time, $O(N)$ Space.

#### 9. Best Time to Buy and Sell Stock with Cooldown
- **College/Drive:** Campus Hiring 2024
- **Problem Summary:** Maximize profit with 1-day cooldown after selling.
- **Constraints:** $1 \le prices.length \le 5000$.
- **LeetCode Equivalent:** [309. Best Time to Buy and Sell Stock with Cooldown](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-cooldown/)
- **Approach:** State machine DP with 3 states: `held`, `sold`, `rest`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 10. Maximum Subarray Sum with Fixed Window Size K
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Find contiguous subsegment of size $K$ with maximum cash flow sum.
- **Constraints:** $1 \le k \le n \le 10^5$.
- **Approach:** Sliding window keeping running sum.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Subarray Sum Equals K
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Count total continuous subarrays whose sum equals $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency counter.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 12. Trapping Rain Water
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 13. Course Schedule (Topological Sort)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Cycle detection in directed graph of security processing dependencies.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Kahn's Algorithm / BFS indegree count.
- **Complexity:** $O(V + E)$ Time.

#### 14. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Compute minimum time for contagion to spread across entire 2D matrix.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS starting with all initially rotten cells.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 15. Coin Change (Fewest Coins)
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Fewest coins needed to make up target amount.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

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

## 🧠 Frequent Technical & SQL MCQs in BlackRock OA
1. **Database Indexing & Range Queries:**
   - Why are B+ trees preferred over B trees for database indexing?
   - *Answer:* All leaf nodes are linked in a singly/doubly linked list, enabling extremely efficient range scans without traversing up and down intermediate nodes.
2. **Sharpe Ratio Intuition:**
   - What does a high Sharpe ratio indicate in portfolio performance?
   - *Answer:* It indicates high excess return generated per unit of total risk (volatility); higher is better ($\frac{R_p - R_f}{\sigma_p}$).
3. **BlackRock Aladdin Platform Principles:**
   - What is the primary role of Aladdin in enterprise asset management?
   - *Answer:* It provides an integrated investment management platform uniting risk analytics, portfolio construction, trading execution, compliance, and post-trade operations under a unified single database model.
