# PayPal Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💳

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  - 2 Algorithmic Coding Questions (Medium to Hard).
  - 10 to 15 Core Computer Science MCQs (Operating Systems, DBMS/SQL, OOPs, Concurrency).
- **Evaluation Criteria:**
  - Full test-case clearance on both coding problems is standard for shortlisting.
  - High weightage placed on practical fintech simulation and transaction logic.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Heaps & Priority Queue Reductions:** Greedy reduction, merging transactions, connect sticks.
- **Wallet & Account Balances:** Ledger transactions, race conditions, overdraft checks, sliding window fraud detection.
- **String Substring Constraints:** Shortest window matching custom alphabets, vowel windows, longest unique substrings.
- **Interval Scheduling:** Maximum concurrent payments, job scheduling, server loads.
- **Prefix Sums & Modulo Arithmetic:** Contiguous equal 0/1 array, max subarray sum modulo M, subarray sum equals K.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Minimum Cost to Connect Transaction Pipes (Min-Heap)
- **College/Drive:** IIT Kharagpur / IIT Guwahati 2024–2025
- **Problem Summary:** You are given an array of integers representing transaction bundle sizes. In each step, combine the two smallest bundles. The cost to connect is their sum. Repeat until one bundle remains. Find minimum total cost.
- **Constraints:** $1 \le n \le 10^4$.
- **LeetCode Equivalent:** [1167. Minimum Cost to Connect Sticks](https://leetcode.com/problems/minimum-cost-to-connect-sticks/)
- **Approach:** Min-Heap (`std::priority_queue<int, vector<int>, greater<int>>`). Continuously extract two smallest elements and push their sum back.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 2. Digital Wallet Balance & Fraud Transaction Validator
- **College/Drive:** BITS Pilani / NIT Surathkal 2024–2025
- **Problem Summary:** Implement a digital wallet system that validates incoming payment streams `[user_id, amount, timestamp, location]`. Reject transactions if:
  1. Balance drops below zero (no overdraft).
  2. Two transactions from the same user occur within 5 minutes across locations $> 100 \text{ km}$ apart.
- **Constraints:** $1 \le transactions.length \le 10^5$.
- **Approach:** HashMap mapping `user_id -> balance` and `user_id -> deque<Transaction>` tracking timestamps and coordinates.
- **Complexity:** $O(1)$ amortized per transaction.

#### 3. Shortest Substring Containing All Target Characters
- **College/Drive:** DTU / NSUT 2024–2025
- **Problem Summary:** Given a string $S$ and an integer $K$, find the length of the shortest continuous substring in $S$ that contains at least $K$ distinct vowels.
- **Constraints:** $1 \le |S| \le 10^5$, $1 \le K \le 5$.
- **Approach:** Variable-size Sliding Window with two pointers and vowel frequency map.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 4. Maximum Profit from Scheduled Currency Orders
- **College/Drive:** VIT / Thapar 2024–2025
- **Problem Summary:** Given $N$ orders with start time, end time, and payout. No two orders can overlap in the execution queue. Find maximum total payout.
- **Constraints:** $1 \le N \le 5 \times 10^4$.
- **LeetCode Equivalent:** [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)
- **Approach:** Sort by end times; DP with Binary Search (`std::upper_bound`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 5. Longest Subarray of Equal 0s and 1s
- **College/Drive:** Campus Hiring Slot 1 (2024–2025)
- **Problem Summary:** Given a binary array representing approved (1) and declined (0) payments, find the maximum length of a contiguous subarray with equal approved and declined payments.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [525. Contiguous Array](https://leetcode.com/problems/contiguous-array/)
- **Approach:** Replace `0` with `-1`; find longest subarray with sum equal to 0 using prefix sum map.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 6. Task Scheduler / Payment Batching Processor
- **College/Drive:** Off-Campus Drive 2024
- **Problem Summary:** Given a characters array `tasks` and a cooling interval $n$, return the least number of units of times that the CPU will take to finish all the given tasks.
- **Constraints:** $1 \le tasks.length \le 10^4$, $0 \le n \le 100$.
- **LeetCode Equivalent:** [621. Task Scheduler](https://leetcode.com/problems/task-scheduler/)
- **Approach:** Math formula based on maximum frequency character: $\max(\text{len}(tasks), (\text{max\_freq} - 1) \times (n + 1) + \text{count\_max\_freq})$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Reverse Nodes in k-Group
- **College/Drive:** PayPal Tech Drive 2024
- **Problem Summary:** Given head of linked list, reverse nodes $k$ at a time and return modified list.
- **Constraints:** Nodes $\le 5000$.
- **LeetCode Equivalent:** [25. Reverse Nodes in k-Group](https://leetcode.com/problems/reverse-nodes-in-k-group/)
- **Approach:** Count $k$ nodes, reverse subsegment in-place, link recursively to subsequent groups.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Maximum Subarray Sum with Modulo M
- **College/Drive:** PayPal Advanced Slot 2024
- **Problem Summary:** Given an array of $N$ integers and integer $M$, find the maximum sum of any contiguous subarray modulo $M$.
- **Constraints:** $1 \le N \le 10^5$, $1 \le M \le 10^9$.
- **Approach:** Prefix sums modulo $M$ stored in a `std::set`. For each prefix sum $P$, query smallest prefix in set $> P$ via `lower_bound`. Maximum candidate is $(P - \text{prefix\_greater} + M) \pmod M$.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 9. Subarray Sum Equals K
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Count total continuous subarrays whose sum equals $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sum frequencies stored in Hash Map.
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

#### 12. Daily Temperatures / Metric Spike Monotonic Stack
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Find days to wait for a warmer day.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 13. Merge Intervals
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Merge all overlapping execution intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time; merge overlaps.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 14. Trapping Rain Water
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 15. Coin Change (Fewest Coins)
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Minimum coins needed to make up amount.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 16. Product of Array Except Self without Division
- **College/Drive:** Campus Slot 2023
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

## 🧠 Frequent Concurrency & Systems MCQs in PayPal OA
1. **Double-Checked Locking in Singleton:**
   - Why must the singleton instance variable be declared `volatile` in double-checked locking?
   - *Answer:* To prevent instruction reordering by the compiler/CPU. Without `volatile`, thread B could observe a non-null instance reference before the constructor has fully finished initializing fields in thread A.
2. **Distributed Transactions & 2-Phase Commit (2PC):**
   - What is the primary drawback of the Two-Phase Commit protocol in payment gateways?
   - *Answer:* It is a blocking protocol. If the transaction coordinator crashes during the prepare phase, participating cohort nodes remain blocked holding database locks indefinitely.
3. **Database Isolation: Phantom Read vs Non-Repeatable Read:**
   - How does a Phantom Read differ from a Non-Repeatable Read?
   - *Answer:* Non-Repeatable Read occurs when a row is re-read and its column values have been modified by another transaction. Phantom Read occurs when a range query (`WHERE age > 30`) is re-executed and *new rows* matching the predicate have been inserted by another committed transaction.
