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
- **College/Drive:** Capital One SWE TDP Drive 2024
- **Problem Summary:** Design a simplified banking system that supports three operations:
  - `CREATE_ACCOUNT(timestamp, account_id)`
  - `DEPOSIT(timestamp, account_id, amount)`
  - `TRANSFER(timestamp, source_id, target_id, amount)`
  If source has insufficient balance or account does not exist, fail transaction. Track total successful transfers and final account balances.
- **Approach:** Hash Map mapping `account_id -> balance` with timestamp and validation checks.
- **Complexity:** $O(1)$ per operation.

#### 2. Matrix Diagonal Sort / Zigzag Traversal (Task 2)
- **College/Drive:** CodeSignal GCA Assessment 2024
- **Problem Summary:** Given an $M \times N$ matrix of integers, sort the elements in each matrix diagonal (from top-left to bottom-right) in ascending order and return the resulting matrix.
- **LeetCode Equivalent:** [1329. Sort the Matrix Diagonally](https://leetcode.com/problems/sort-the-matrix-diagonally/)
- **Approach:** Group elements by diagonal index `(r - c)` in a HashMap, sort each list, and write back to the matrix.
- **Complexity:** $O(M \times N \log(\min(M, N)))$ Time.

#### 3. Maximum Continuous Days with Positive Balance (Task 4)
- **College/Drive:** Capital One Power Day Screen 2024
- **Problem Summary:** Given an array of daily changes in bank account balance, find the maximum length of a contiguous period where the account balance remained strictly greater than its initial value.
- **Approach:** Prefix sums combined with Monotonic Stack or Binary Search.
- **Complexity:** $O(N)$ or $O(N \log N)$ Time.

#### 4. Mutated Array Distance / Number Replacement
- **College/Drive:** CodeSignal GCA Slot 2024
- **Problem Summary:** Given an array `arr` and a target integer `target`, return the value of the integer such that the sum of the array is closest to `target` when every element greater than this value is replaced by it.
- **LeetCode Equivalent:** [1300. Sum of Mutated Array Closest to Target](https://leetcode.com/problems/sum-of-mutated-array-closest-to-target/)
- **Approach:** Binary Search on the replacement value in range $[0, \max(arr)]$.
- **Complexity:** $O(N \log(\max(arr)))$ Time.

#### 5. Text Editor with Undo / Redo Commands (Task 3 Simulation)
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Implement text editor supporting commands `INSERT(text)`, `DELETE()`, `COPY(index)`, `PASTE()`, and `UNDO()`.
- **Approach:** Maintain text as `std::string` or double-ended buffer with a Stack of previous states for `UNDO`.
- **Complexity:** $O(1)$ per operation amortized, $O(K \times L)$ space for history snapshots.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Spiral Matrix Traversal and Fill (Task 2)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Return all elements of $M \times N$ matrix in spiral clockwise order.
- **LeetCode Equivalent:** [54. Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
- **Complexity:** $O(M \times N)$ Time, $O(1)$ Extra Space.

#### 7. Subarray Sum Equals K (Transaction Matching)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Count contiguous subarrays that sum up to target $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sum with hash map of seen prefix counts.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 8. Longest Substring Without Repeating Characters
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Length of longest substring without duplicate characters.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 9. Top K Frequent Elements in Transaction Stream
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Return $K$ most frequent account transactions.
- **LeetCode Equivalent:** [347. Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/)
- **Approach:** Hash Map frequency count + Min-Heap of size $K$.
- **Complexity:** $O(N \log K)$ Time.

#### 10. Valid Palindrome II (At Most One Deletion)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Determine if string is palindrome allowing removal of at most one character.
- **LeetCode Equivalent:** [680. Valid Palindrome II](https://leetcode.com/problems/valid-palindrome-ii/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 💡 CodeSignal GCA Strategy for Capital One
1. **Solve in Order: Task 1 -> Task 2 -> Task 4 -> Task 3:**
   - Tasks 1 and 2 are easy points (aim to finish both within 15–18 minutes).
   - Task 4 usually tests clean algorithms (two pointers, binary search, prefix sums) and takes less code than Task 3.
   - Leave Task 3 for the remaining 30–35 minutes because it involves 50+ lines of simulation logic with tricky edge cases.
2. **Watch for Hidden Penalties:** CodeSignal factors speed and submission count into the final 300–850 score. Test locally before submitting.
