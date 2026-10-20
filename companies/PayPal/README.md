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
- **Heaps & Priority Queue Reductions:** Greedy reduction, merging transactions.
- **Wallet & Account Balances:** Ledger transactions, race conditions, overdraft checks.
- **String Substring Constraints:** Shortest window matching custom alphabets.
- **Interval Scheduling:** Maximum concurrent payments, server loads.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Minimum Cost to Connect Transaction Pipes (Min-Heap)
- **College/Drive:** IIT Kharagpur / IIT Guwahati 2024
- **Problem Statement:** You are given an array of integers representing transaction bundle sizes. In each step, combine the two smallest bundles. The cost to connect is their sum. Repeat until one bundle remains. Find minimum total cost.
- **LeetCode Equivalent:** [1167. Minimum Cost to Connect Sticks](https://leetcode.com/problems/minimum-cost-to-connect-sticks/)
- **Approach:** Min-Heap (`std::priority_queue<int, vector<int>, greater<int>>`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 2. Digital Wallet Balance & Fraud Transaction Validator
- **College/Drive:** BITS Pilani / NIT Surathkal 2024
- **Problem Statement:** Implement a digital wallet system that validates incoming payment streams `[user_id, amount, timestamp, location]`. Reject transactions if:
  1. Balance drops below zero (no overdraft).
  2. Two transactions from the same user occur within 5 minutes across locations $> 100 \text{ km}$ apart.
- **Approach:** HashMap mapping `user_id -> balance` and `user_id -> deque<Transaction>` tracking timestamps and coordinates.
- **Complexity:** $O(1)$ amortized per transaction.

#### 3. Shortest Substring Containing All Target Characters
- **College/Drive:** DTU / NSUT 2024
- **Problem Statement:** Given a string $S$ and an integer $K$, find the length of the shortest continuous substring in $S$ that contains at least $K$ distinct vowels.
- **Approach:** Variable-size Sliding Window with two pointers and vowel frequency map.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 4. Maximum Profit from Scheduled Currency Orders
- **College/Drive:** VIT / Thapar 2024
- **Problem Statement:** Given $N$ orders with start time, end time, and payout. No two orders can overlap in the execution queue. Find maximum total payout.
- **LeetCode Equivalent:** [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)
- **Approach:** Sort by end times; DP with Binary Search (`std::upper_bound`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Longest Subarray of Equal 0s and 1s
- **College/Drive:** Campus Hiring Slot 1 (2023)
- **Problem Statement:** Given a binary array representing approved (1) and declined (0) payments, find the maximum length of a contiguous subarray with equal approved and declined payments.
- **LeetCode Equivalent:** [525. Contiguous Array](https://leetcode.com/problems/contiguous-array/)
- **Approach:** Replace `0` with `-1`; find longest subarray with sum equal to 0 using prefix sum map.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 6. Task Scheduler / Payment Batching Processor
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Given a characters array `tasks` and a cooling interval $n$, return the least number of units of times that the CPU will take to finish all the given tasks.
- **LeetCode Equivalent:** [621. Task Scheduler](https://leetcode.com/problems/task-scheduler/)
- **Approach:** Math formula based on maximum frequency character: $\max(\text{len}(tasks), (\text{max\_freq} - 1) \times (n + 1) + \text{count\_max\_freq})$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Reverse Nodes in k-Group
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Given the head of a linked list, reverse the nodes of the list $k$ at a time, and return the modified list.
- **LeetCode Equivalent:** [25. Reverse Nodes in k-Group](https://leetcode.com/problems/reverse-nodes-in-k-group/)
- **Approach:** Count $k$ nodes, reverse subsegment in-place, link recursively to subsequent groups.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Maximum Subarray Sum with Modulo M
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Given an array of $N$ integers and integer $M$, find the maximum sum of any contiguous subarray modulo $M$.
- **Approach:** Prefix sums modulo $M$ stored in a `std::set`. For each prefix sum $P$, query smallest prefix in set $> P$ via `lower_bound`.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.
