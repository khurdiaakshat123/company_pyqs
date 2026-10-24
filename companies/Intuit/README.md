# Intuit Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💰

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Glider AI** / **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  - 4 Algorithmic Coding Questions (ranging from Medium to Hard).
  - (In select campus drives) 2 DSA Coding Questions + 1 Advanced SQL Query + 1 Linux/Bash Scripting Question.
- **Evaluation Criteria:**
  - Glider uses strict behavioral proctoring (screen tracking, audio monitoring, typing cadence).
  - Passing 3.5 to 4 questions is usually required for SDE-1 / Summer Intern interviews.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Grid Pathfinding & Dungeon Games:** Minimum initial health, obstacle navigation, multi-source BFS.
- **Topological Sorting & Dependency Ordering:** Alien dictionary, package build systems, course schedule.
- **Binary Search on Answer:** Allocation of resources, capacity thresholds, shipment days.
- **Financial Stream & Sliding Windows:** Fraud detection windows, minimum window substring, subarray sum equals K.
- **SQL & Shell Scripting:** Monthly recurring revenue (MRR), window ranks, bash text filtering (`awk`, `sed`, `grep`).
- **Core CS MCQs:** Financial transaction idempotency, ACID vs BASE, distributed database sharding, double-entry bookkeeping ledger integrity.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Dungeon Game / Minimum Initial Health (Intuit Classic)
- **College/Drive:** IIT Roorkee / IIT BHU 2024
- **Problem Statement:** The demons had captured the princess and imprisoned her in the bottom-right corner of a dungeon of size $M \times N$. The knight starts at top-left. Each room contains magic or demons ($grid[i][j]$ integer). Knight dies if health $\le 0$. Find knight's minimum initial health to rescue the princess.
- **LeetCode Equivalent:** [174. Dungeon Game](https://leetcode.com/problems/dungeon-game/)
- **Approach:** Bottom-up Dynamic Programming starting from destination $(M-1, N-1)$ back to $(0, 0)$:
  $$dp[i][j] = \max(1, \min(dp[i+1][j], dp[i][j+1]) - grid[i][j])$$
- **Complexity:** $O(M \times N)$ Time, $O(N)$ Space.

#### 2. Alien Dictionary / Character Lexicographical Order
- **College/Drive:** BITS Pilani 2024
- **Problem Statement:** Given a list of strings `words` from an alien language's dictionary where the strings are sorted lexicographically by the rules of this new language. Derive the order of letters in this language.
- **LeetCode Equivalent:** [269. Alien Dictionary](https://leetcode.com/problems/alien-dictionary/)
- **Approach:** Graph construction: compare adjacent words to find first differing character, creating a directed edge. Use Kahn's Algorithm (Topological Sort). If cycle detected, return `""`.
- **Complexity:** $O(C)$ where $C$ is total length of all words.

#### 3. Capacity to Ship Packages Within D Days (Binary Search on Answer)
- **College/Drive:** NIT Trichy / Warangal 2024
- **Problem Statement:** A conveyor belt has packages that must be shipped within `days` days. Return the least weight capacity of the ship that will result in all packages being shipped within `days` days.
- **LeetCode Equivalent:** [1011. Capacity To Ship Packages Within D Days](https://leetcode.com/problems/capacity-to-ship-packages-within-d-days/)
- **Approach:** Binary Search in range $[\max(weights), \sum weights]$. Greedy verification check.
- **Complexity:** $O(N \log(\sum weights))$ Time.

#### 4. Intuit SQL Query: High Value Invoices per Customer
- **College/Drive:** VIT / Manipal 2024
- **Problem Statement:** Write a query to find customers whose average invoice amount exceeds $\$5,000$ and who have paid more than 3 invoices in the last financial year.
- **SQL Implementation:**
  ```sql
  SELECT customer_id, COUNT(invoice_id) as total_invoices, AVG(amount) as avg_spent
  FROM Invoices
  WHERE invoice_date BETWEEN '2023-04-01' AND '2024-03-31'
  GROUP BY customer_id
  HAVING COUNT(invoice_id) > 3 AND AVG(amount) > 5000;
  ```

#### 5. Merge Overlapping Tax Deduction Brackets (Merge Intervals)
- **College/Drive:** IIT Delhi 2024
- **Problem Statement:** Given income intervals for tiered tax deductions, merge overlapping and contiguous intervals.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start value; iterate and merge if current interval overlaps with previous.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 6. Subarray Sum Equals K (Transaction Anomaly Detection)
- **College/Drive:** IIT Bombay 2024
- **Problem Statement:** Given an array of integers `nums` representing net daily balances and target $K$, find total contiguous subsegments summing to $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency tracking.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Trapping Rain Water
- **College/Drive:** IIT Kanpur 2024
- **Problem Statement:** Compute total water trapped by elevation bars after rainfall.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers inward from left and right maintaining running maxima.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Minimum Window Substring / Token Matching
- **College/Drive:** BITS Pilani 2024
- **Problem Statement:** Find smallest substring in `s` containing all characters of pattern `t`.
- **LeetCode Equivalent:** [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- **Approach:** Sliding window with dual frequency maps.
- **Complexity:** $O(|S| + |T|)$ Time.

#### 9. Search in Rotated Sorted Array
- **College/Drive:** DTU Delhi 2024
- **Problem Statement:** Search for a target key in a circularly shifted sorted array.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking which half is sorted.
- **Complexity:** $O(\log N)$ Time.

#### 10. Real SQL: Monthly Recurring Revenue (MRR) Growth Rate
- **College/Drive:** Intuit Campus Hiring 2024
- **Problem Statement:** Calculate monthly recurring revenue (MRR) and month-over-month growth percentage for subscription services in 2024.
- **SQL Implementation:**
  ```sql
  WITH MonthlyRev AS (
      SELECT DATE_TRUNC('month', payment_date) AS rev_month,
             SUM(amount) AS total_mrr
      FROM Subscriptions
      WHERE payment_date >= '2024-01-01'
      GROUP BY DATE_TRUNC('month', payment_date)
  )
  SELECT rev_month, total_mrr,
         ROUND(((total_mrr - LAG(total_mrr) OVER (ORDER BY rev_month)) / 
                LAG(total_mrr) OVER (ORDER BY rev_month)) * 100.0, 2) AS mom_growth_pct
  FROM MonthlyRev;
  ```

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Non-Overlapping Intervals / Meeting Optimizer
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Given an array of intervals `intervals` where `intervals[i] = [start_i, end_i]`, return the minimum number of intervals you need to remove to make the rest of the intervals non-overlapping.
- **LeetCode Equivalent:** [435. Non-overlapping Intervals](https://leetcode.com/problems/non-overlapping-intervals/)
- **Approach:** Greedy: Sort intervals by end time; keep non-overlapping intervals ending earliest.
- **Complexity:** $O(N \log N)$ Time, $O(1)$ Space.

#### 12. Course Schedule II (Order of Completion)
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Return the ordering of courses you should take to finish all courses given prerequisite pairs.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm with in-degree tracking and queue.
- **Complexity:** $O(V + E)$ Time.

#### 13. Bash Scripting: Parse Log Error Count
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Write a bash one-liner to parse a log file `server.log`, find lines containing `"ERROR"`, extract the IP address (column 2), count occurrences, and print the top 5 offending IPs sorted descending.
- **Solution:** `grep "ERROR" server.log | awk '{print $2}' | sort | uniq -c | sort -nr | head -n 5`

#### 14. Maximum Subarray with Bounded Element Deletions
- **College/Drive:** Campus Intern Hiring 2023
- **Problem Statement:** Return the maximum sum of a non-empty subarray after deleting at most one negative element.
- **Approach:** 2-state DP: `dp_no_del[i]` and `dp_one_del[i]`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 15. Cascading Service Outage (Rotting Oranges)
- **College/Drive:** NSUT Delhi 2023
- **Problem Statement:** Multi-source BFS to calculate minutes required for an outage to spread across a server grid.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time and Space.

#### 16. Word Break (Invoice Header Validator)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Determine if invoice header string can be segmented into space-separated dictionary keywords.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Complexity:** $O(N^2)$ Time, $O(N)$ Space.

#### 17. Longest Increasing Subsequence
- **College/Drive:** IIIT Delhi 2023
- **Problem Statement:** Find length of longest strictly increasing subsequence in transaction amounts.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Approach:** Patience sorting with binary search.
- **Complexity:** $O(N \log N)$ Time.

#### 18. LRU Cache / Session Cache Implementation
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Implement an LRU cache with $O(1)$ operations.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Complexity:** $O(1)$ Time per operation.

#### 19. Load Balancing Server Tasks (Reorganize String)
- **College/Drive:** Campus Placement 2023
- **Problem Statement:** Rearrange characters so that no two identical characters are adjacent.
- **LeetCode Equivalent:** [767. Reorganize String](https://leetcode.com/problems/reorganize-string/)
- **Complexity:** $O(N \log \Sigma)$ Time.

#### 20. QuickBooks Expression Parser (Decode String)
- **College/Drive:** University Hiring 2023
- **Problem Statement:** Decode nested string encoding format `k[string]`.
- **LeetCode Equivalent:** [394. Decode String](https://leetcode.com/problems/decode-string/)
- **Approach:** Dual stack for counts and strings.
- **Complexity:** $O(\text{Output Length})$ Time.

---

## 🧠 Frequent FinTech & Architecture MCQs Asked in Intuit OA
1. **Idempotency in Payment Gateways:**
   - Why must payment transaction processing endpoints be strictly idempotent, and how is it implemented?
   - *Answer:* Network timeouts or retries may cause a client to submit the same charge request multiple times. Idempotency ensures that submitting identical requests produces the exact same outcome without duplicate charges. It is implemented by generating a unique Idempotency Key (UUID) on the client side, storing it in Redis/database with an atomic lock, and returning the cached response if the key was already processed.
2. **Double-Entry Bookkeeping Ledger Invariants:**
   - What invariant must hold true across every single transaction in a double-entry ledger?
   - *Answer:* For every transaction, the sum of all debits must exactly equal the sum of all credits ($\sum \text{Debits} = \sum \text{Credits}$), and total assets must always equal total liabilities plus equity ($\text{Assets} = \text{Liabilities} + \text{Equity}$).
