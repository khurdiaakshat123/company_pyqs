# Capital One Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 💳

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **CodeSignal** (General Coding Assessment - GCA Framework)
- **Test Duration:** 70 minutes (4 Tasks)
- **Structure Breakdown:**
  - **Task 1 (Easy):** Basic string/array operations, counting, and simple formatting.
  - **Task 2 (Easy-Medium):** 2D Matrix traversal, bounded manipulation, or grid rotation.
  - **Task 3 (Medium-Hard):** Complex banking simulation / Transaction log processing with intricate rules and edge cases.
  - **Task 4 (Hard):** Algorithmic optimization (Two pointers, sliding window, prefix sums, or monotonic stack).
- **Scoring & Cutoff:** CodeSignal generates an automated score between **300 and 850**. Capital One typically requires a score of **$\ge 750 - 800+$** to advance to their Power Day / technical interviews.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Banking & Transaction Simulations | Medium - Hard | Processing ledger credits/debits, balance verification, fraud detection |
| **Very High** | 2D Matrix & Grid Operations | Easy - Medium | Diagonal traversals, matrix rotations, boundary boundary checks |
| **High** | Strings & Text Parsing | Easy - Medium | Palindrome permutations, anagrams, custom string alignment |
| **High** | Sliding Window & Intervals | Medium | Overlapping transactions, maximum balances in time intervals |
| **Medium** | HashMaps & Frequency Counters | Easy - Medium | Most frequent elements, balance lookups |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Banking System Transaction Ledger (Task 3 Simulation)
- **Problem Summary:** Design a simplified banking system that supports three operations:
  - `CREATE_ACCOUNT(timestamp, account_id)`
  - `DEPOSIT(timestamp, account_id, amount)`
  - `TRANSFER(timestamp, source_id, target_id, amount)`
  If source has insufficient balance or account does not exist, fail transaction. Track total successful transfers and final account balances.
- **Approach:** Hash Map mapping `account_id -> balance` with timestamp and validation checks.
- **Complexity:** $O(1)$ per operation.

### 2. Matrix Diagonal Sort / Zigzag Traversal (Task 2)
- **Problem Summary:** Given an $M \times N$ matrix of integers, sort the elements in each matrix diagonal (from top-left to bottom-right) in ascending order and return the resulting matrix.
- **LeetCode Equivalent:** [1329. Sort the Matrix Diagonally](https://leetcode.com/problems/sort-the-matrix-diagonally/)
- **Approach:** Group elements by diagonal index `(r - c)` in a HashMap, sort each list, and write back to the matrix.
- **Complexity:** $O(M \times N \log(\min(M, N)))$ Time.

### 3. Maximum Continuous Days with Positive Balance (Task 4)
- **Problem Summary:** Given an array of daily changes in bank account balance, find the maximum length of a contiguous period where the account balance remained strictly greater than its initial value.
- **Approach:** Prefix sums combined with Monotonic Stack or Binary Search.
- **Complexity:** $O(N)$ or $O(N \log N)$ Time.

### 4. Mutated Array Distance / Number Replacement
- **Problem Summary:** Given an array `arr` and a target integer `target`, return the value of the integer such that the sum of the array is closest to `target` when every element greater than this value is replaced by it.
- **LeetCode Equivalent:** [1300. Sum of Mutated Array Closest to Target](https://leetcode.com/problems/sum-of-mutated-array-closest-to-target/)
- **Approach:** Binary Search on the replacement value in range $[0, \max(arr)]$.
- **Complexity:** $O(N \log(\max(arr)))$ Time.
