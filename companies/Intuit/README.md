# Intuit Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💰

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Glider AI** / **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  - 4 Algorithmic Coding Questions (ranging from Easy to Hard).
  - (In select campus drives) 2 DSA Coding Questions + 1 Advanced SQL Query + 1 Linux/Bash Scripting Question.
- **Evaluation Criteria:**
  - Glider uses strict behavioral proctoring (screen tracking, audio monitoring).
  - Passing 3.5 to 4 questions is usually required for SDE-1 / Summer Intern interviews.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Grid Pathfinding & Dungeon Games:** Minimum initial health, obstacle navigation.
- **Topological Sorting & Dependency Ordering:** Alien dictionary, package build systems.
- **Binary Search on Answer:** Allocation of resources, capacity thresholds.
- **SQL & Shell:** Joins, aggregations, bash text filtering (`awk`, `sed`, `grep`).

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

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Non-Overlapping Intervals / Meeting Optimizer
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Given an array of intervals `intervals` where `intervals[i] = [start_i, end_i]`, return the minimum number of intervals you need to remove to make the rest of the intervals non-overlapping.
- **LeetCode Equivalent:** [435. Non-overlapping Intervals](https://leetcode.com/problems/non-overlapping-intervals/)
- **Approach:** Greedy: Sort intervals by end time; keep non-overlapping intervals ending earliest.
- **Complexity:** $O(N \log N)$ Time, $O(1)$ Space.

#### 6. Course Schedule II (Order of Completion)
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Return the ordering of courses you should take to finish all courses given prerequisite pairs.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm with in-degree tracking and queue.
- **Complexity:** $O(V + E)$ Time.

#### 7. Bash Scripting: Parse Log Error Count
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Write a bash one-liner to parse a log file `server.log`, find lines containing `"ERROR"`, extract the IP address (column 2), count occurrences, and print the top 5 offending IPs sorted descending.
- **Solution:** `grep "ERROR" server.log | awk '{print $2}' | sort | uniq -c | sort -nr | head -n 5`

#### 8. Maximum Subarray with Bounded Element Deletions
- **College/Drive:** Campus Intern Hiring 2023
- **Problem Statement:** Return the maximum sum of a non-empty subarray after deleting at most one negative element.
- **Approach:** 2-state DP: `dp_no_del[i]` and `dp_one_del[i]`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.
