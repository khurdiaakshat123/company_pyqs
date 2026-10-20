# Bank of America (BofA) Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **Codility**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  1. **Coding Section:** 2 Coding Problems (LeetCode Easy to Medium difficulty, 45–60 mins).
  2. **Core CS & SQL Section:** 10 to 15 MCQs covering SQL Queries, DBMS Normalization, Operating Systems, OOPs principles, and Quantitative Aptitude (20–30 mins).
- **Passing Cutoff:** 100% test cases cleared on both coding questions + solid performance on SQL/DBMS MCQs (>75%).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Strings & Frequency Counting:** Anagrams, unique characters, palindrome checks, transaction tokenization.
- **Arrays & Two Pointers:** Running sum, balance index, pair target sum, move zeros, maximum average subarray.
- **SQL Queries & Window Functions:** Cumulative running totals, `DENSE_RANK()`, `GROUP BY` with `HAVING`, inner/outer joins.
- **Sliding Window & Intervals:** Maximum sum subarray of size K, merging time slots.
- **Trees & Binary Search Trees:** Invert binary tree, path sum, level order traversal, symmetric tree.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Invert Binary Tree
- **College/Drive:** BITS Pilani / VIT Vellore 2024
- **Problem Summary:** Given the root of a binary tree, invert the tree, and return its root.
- **LeetCode Equivalent:** [226. Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/)
- **Approach:** Recursive DFS swapping left and right child pointers at each node.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 2. First Unique Character in a String (Financial Transaction ID)
- **College/Drive:** Thapar University / Manipal 2024
- **Problem Summary:** Given a transaction string $s$, find the first non-repeating character in it and return its index. If it does not exist, return -1.
- **LeetCode Equivalent:** [387. First Unique Character in a String](https://leetcode.com/problems/first-unique-character-in-a-string/)
- **Approach:** 26-element character frequency array; two-pass scan.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 3. Maximum Average Subarray I (Sliding Window)
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** You are given an integer array `nums` consisting of $n$ elements, and an integer $k$. Find a contiguous subarray whose length is equal to $k$ that has the maximum average value and return this value.
- **LeetCode Equivalent:** [643. Maximum Average Subarray I](https://leetcode.com/problems/maximum-average-subarray-i/)
- **Approach:** Fixed-size sliding window of length $k$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Real SQL Question: Account Holder Running Total
- **College/Drive:** Bank of America Global Tech Campus 2024
- **Problem Summary:** Write a query to calculate the cumulative running total of deposits for each account holder over time.
- **SQL Implementation:**
  ```sql
  SELECT account_id, transaction_date, amount,
         SUM(amount) OVER (
             PARTITION BY account_id 
             ORDER BY transaction_date 
             ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW
         ) as running_balance
  FROM Transactions;
  ```

#### 5. Two Sum II - Input Array Is Sorted
- **College/Drive:** Campus Placement Drive 2024
- **Problem Summary:** Given a 1-indexed array of integers `numbers` that is already sorted in non-decreasing order, find two numbers such that they add up to a specific `target`.
- **LeetCode Equivalent:** [167. Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)
- **Approach:** Two pointers (`left = 0`, `right = n-1`). Shrink inwards based on comparison with target.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Valid Parentheses (Transaction Validation)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Check if transaction bracket string `()[]{}` is balanced.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Merge Two Sorted Linked Lists
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Merge two sorted linked lists into one sorted list.
- **LeetCode Equivalent:** [21. Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
- **Complexity:** $O(M + N)$ Time, $O(1)$ Space.

#### 8. Path Sum in Binary Tree
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Check if tree has root-to-leaf path summing to target.
- **LeetCode Equivalent:** [112. Path Sum](https://leetcode.com/problems/path-sum/)
- **Approach:** Recursive DFS subtracting current node value from target sum.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 9. Subarray Sum Equals K
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Count subarrays summing to $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Best Time to Buy and Sell Stock
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Find maximum profit with single buy and sell transaction.
- **LeetCode Equivalent:** [121. Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent CS Fundamentals MCQs in Bank of America OA
1. **Database Triggers:**
   - What is a database trigger, and when is it executed?
   - *Answer:* A trigger is a stored procedure automatically invoked by the DBMS in response to specified database events (`INSERT`, `UPDATE`, `DELETE`) on a particular table or view.
2. **Deadlock Conditions (Coffman Conditions):**
   - What are the four simultaneous conditions required for a deadlock?
   - *Answer:* Mutual Exclusion, Hold and Wait, No Preemption, and Circular Wait.
