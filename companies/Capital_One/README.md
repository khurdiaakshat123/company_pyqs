# Capital One Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💳

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **CodeSignal** (General Coding Assessment - GCA Framework)
- **Test Duration:** 70 minutes (4 Tasks)
- **Structure Breakdown:**
  - **Task 1 (Easy):** Basic string/array operations, counting, and simple formatting.
  - **Task 2 (Easy-Medium):** 2D Matrix traversal, bounded manipulation, or diagonal sorting.
  - **Task 3 (Medium-Hard):** Complex banking simulation / Transaction log processing with intricate rules, error states, and edge cases.
  - **Task 4 (Hard):** Algorithmic optimization (Two pointers, sliding window, prefix sums, or monotonic stack).
- **Scoring & Cutoff:** CodeSignal generates an automated score between **300 and 850**. Capital One typically requires a score of **$\ge 750 - 800+$** to advance to their Power Day / technical interviews.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Banking & Transaction Simulations (Task 3):** Processing ledger credits/debits, balance verification, fraud detection, rollback transactions.
- **2D Matrix & Grid Operations (Task 2):** Diagonal traversals, matrix rotations, spiral ordering, boundary checks.
- **Strings & Text Parsing:** Text editor with undo/redo, palindrome permutations, custom string alignment.
- **Sliding Window & Intervals (Task 4):** Overlapping transactions, maximum balances in time intervals, mutated array distance.
- **HashMaps & Frequency Counters:** Most frequent elements, balance lookups, prefix sum matching.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Banking System Transaction Ledger (CodeSignal Task 3 Classic)
- **College/Drive:** Capital One SWE TDP Drive 2024–2025
- **Problem Summary:** Design a simplified banking system that supports three operations:
  - `CREATE_ACCOUNT(timestamp, account_id)`
  - `DEPOSIT(timestamp, account_id, amount)`
  - `TRANSFER(timestamp, source_id, target_id, amount)`
  If source has insufficient balance or account does not exist, fail transaction. Track total successful transfers and final account balances.
- **Constraints:** Up to $10^5$ operations, amounts $\le 10^9$.
- **Approach:** Hash Map mapping `account_id -> balance` with timestamp and validation checks.
- **Complexity:** $O(1)$ per operation.

#### 2. Matrix Diagonal Sort / Zigzag Traversal (Task 2)
- **College/Drive:** CodeSignal GCA Assessment 2024–2025
- **Problem Summary:** Given an $M \times N$ matrix of integers, sort the elements in each matrix diagonal (from top-left to bottom-right) in ascending order and return the resulting matrix.
- **Constraints:** $1 \le M, N \le 100$.
- **LeetCode Equivalent:** [1329. Sort the Matrix Diagonally](https://leetcode.com/problems/sort-the-matrix-diagonally/)
- **Approach:** Group elements by diagonal index `(r - c)` in a HashMap, sort each list, and write back to the matrix.
- **Complexity:** $O(M \times N \log(\min(M, N)))$ Time.

#### 3. Maximum Continuous Days with Positive Balance (Task 4)
- **College/Drive:** Capital One Power Day Screen 2024–2025
- **Problem Summary:** Given an array of daily changes in bank account balance, find the maximum length of a contiguous period where the account balance remained strictly greater than its initial value.
- **Constraints:** $1 \le n \le 10^5$.
- **Approach:** Prefix sums combined with Monotonic Stack or Binary Search.
- **Complexity:** $O(N)$ or $O(N \log N)$ Time.

#### 4. Mutated Array Distance / Number Replacement
- **College/Drive:** CodeSignal GCA Slot 2024–2025
- **Problem Summary:** Given an array `arr` and a target integer `target`, return the value of the integer such that the sum of the array is closest to `target` when every element greater than this value is replaced by it.
- **Constraints:** $1 \le arr.length \le 10^4$, $1 \le target \le 10^5$.
- **LeetCode Equivalent:** [1300. Sum of Mutated Array Closest to Target](https://leetcode.com/problems/sum-of-mutated-array-closest-to-target/)
- **Approach:** Binary Search on the replacement value in range $[0, \max(arr)]$.
- **Complexity:** $O(N \log(\max(arr)))$ Time.

#### 5. Text Editor with Undo / Redo Commands (Task 3 Simulation)
- **College/Drive:** Campus Placement 2024–2025
- **Problem Summary:** Implement text editor supporting commands `INSERT(text)`, `DELETE()`, `COPY(index)`, `PASTE()`, and `UNDO()`.
- **Constraints:** Up to $1000$ operations.
- **Approach:** Maintain text as `std::string` or double-ended buffer with a Stack of previous states for `UNDO`.
- **Complexity:** $O(1)$ per operation amortized, $O(K \times L)$ space for history snapshots.

#### 6. Diagonal Traverse of Matrix (Task 2 Variant)
- **College/Drive:** CodeSignal GCA 2024
- **Problem Summary:** Return all elements of an $M \times N$ matrix in diagonal order.
- **Constraints:** $1 \le M, N \le 10^4$, $M \times N \le 10^5$.
- **LeetCode Equivalent:** [498. Diagonal Traverse](https://leetcode.com/problems/diagonal-traverse/)
- **Approach:** Group elements by sum of coordinates `r + c`. Reverse elements on odd diagonal levels.
- **Complexity:** $O(M \times N)$ Time and Space.

#### 7. Minimum Window Substring (Task 4 Algorithmic Optimization)
- **College/Drive:** Capital One Power Day 2024
- **Problem Summary:** Find minimum window in $s$ containing all characters of $t$.
- **Constraints:** $1 \le |s|, |t| \le 10^5$.
- **LeetCode Equivalent:** [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- **Approach:** Two-pointer sliding window with character frequency counter.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 8. Subarray Sums Divisible by K
- **College/Drive:** Capital One Richmond Screen 2024
- **Problem Summary:** Count non-empty continuous subarrays with sum divisible by $k$.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- **Approach:** Prefix sums modulo $k$ stored in Hash Map.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 9. Daily Temperatures / Metric Spike Monotonic Stack
- **College/Drive:** CodeSignal Assessment 2024
- **Problem Summary:** Find number of days to wait for a warmer day.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Course Schedule II (Dependency Topological Sort)
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Find valid course execution order given prerequisites.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm using indegrees and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Spiral Matrix Traversal and Fill (Task 2)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Return all elements of $M \times N$ matrix in spiral clockwise order.
- **Constraints:** $1 \le M, N \le 100$.
- **LeetCode Equivalent:** [54. Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
- **Approach:** Four boundary pointers (`top`, `bottom`, `left`, `right`) shifting inward.
- **Complexity:** $O(M \times N)$ Time, $O(1)$ Extra Space.

#### 12. Subarray Sum Equals K (Transaction Matching)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Count contiguous subarrays that sum up to target $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sum with hash map of seen prefix counts.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 13. Longest Substring Without Repeating Characters
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Length of longest substring without duplicate characters.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with hash map.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 14. Top K Frequent Elements in Transaction Stream
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Return $K$ most frequent account transactions.
- **Constraints:** $1 \le k \le \text{unique elements} \le 10^5$.
- **LeetCode Equivalent:** [347. Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/)
- **Approach:** Hash Map frequency count + Min-Heap of size $K$.
- **Complexity:** $O(N \log K)$ Time.

#### 15. Valid Palindrome II (At Most One Deletion)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Determine if string is palindrome allowing removal of at most one character.
- **Constraints:** $1 \le s.length \le 10^5$.
- **LeetCode Equivalent:** [680. Valid Palindrome II](https://leetcode.com/problems/valid-palindrome-ii/)
- **Approach:** Two pointers checking mismatch; branch check skipping left or right character once.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. Product of Array Except Self without Division
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 17. Merge Intervals
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Merge all overlapping intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time and merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 18. House Robber (1D Dynamic Programming)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Maximize stolen value without alerting alarms on adjacent houses.
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

## 💡 CodeSignal GCA Strategy for Capital One
1. **Solve in Order: Task 1 -> Task 2 -> Task 4 -> Task 3:**
   - Tasks 1 and 2 are easy points (aim to finish both within 15–18 minutes).
   - Task 4 usually tests clean algorithms (two pointers, binary search, prefix sums) and takes less code than Task 3.
   - Leave Task 3 for the remaining 30–35 minutes because it involves 50+ lines of simulation logic with tricky edge cases.
2. **Watch for Hidden Penalties:** CodeSignal factors speed and submission count into the final 300–850 score. Test locally before submitting.
3. **Handle Edge Cases Early:** Check for empty inputs, negative balances, and non-existent account IDs before executing state transitions.
