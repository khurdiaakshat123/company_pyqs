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
- **Arrays & Two Pointers:** Running sum, balance index, pair target sum, move zeros, maximum average subarray, prefix products.
- **SQL Queries & Window Functions:** Cumulative running totals, `DENSE_RANK()`, `GROUP BY` with `HAVING`, inner/outer joins.
- **Sliding Window & Intervals:** Maximum sum subarray of size K, merging time slots.
- **Trees & Binary Search Trees:** Invert binary tree, path sum, level order traversal, symmetric tree, lowest common ancestor.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Invert Binary Tree
- **College/Drive:** BITS Pilani / VIT Vellore 2024–2025
- **Problem Summary:** Given the root of a binary tree, invert the tree, and return its root.
- **Constraints:** Number of nodes $\le 100$.
- **LeetCode Equivalent:** [226. Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/)
- **Approach:** Recursive DFS swapping left and right child pointers at each node.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 2. First Unique Character in a String (Financial Transaction ID)
- **College/Drive:** Thapar University / Manipal 2024–2025
- **Problem Summary:** Given a transaction string $s$, find the first non-repeating character in it and return its index. If it does not exist, return -1.
- **Constraints:** $1 \le s.length \le 10^5$.
- **LeetCode Equivalent:** [387. First Unique Character in a String](https://leetcode.com/problems/first-unique-character-in-a-string/)
- **Approach:** 26-element character frequency array; two-pass scan.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 3. Maximum Average Subarray I (Sliding Window)
- **College/Drive:** DTU / NSUT 2024–2025
- **Problem Summary:** You are given an integer array `nums` consisting of $n$ elements, and an integer $k$. Find a contiguous subarray whose length is equal to $k$ that has the maximum average value and return this value.
- **Constraints:** $1 \le k \le n \le 10^5$.
- **LeetCode Equivalent:** [643. Maximum Average Subarray I](https://leetcode.com/problems/maximum-average-subarray-i/)
- **Approach:** Fixed-size sliding window of length $k$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Real SQL Question: Account Holder Running Total
- **College/Drive:** Bank of America Global Tech Campus 2024–2025
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
- **College/Drive:** Campus Placement Drive 2024–2025
- **Problem Summary:** Given a 1-indexed array of integers `numbers` that is already sorted in non-decreasing order, find two numbers such that they add up to a specific `target`.
- **Constraints:** $2 \le numbers.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [167. Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)
- **Approach:** Two pointers (`left = 0`, `right = n-1`). Shrink inwards based on comparison with target.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 6. Lowest Common Ancestor of Binary Tree
- **College/Drive:** BofA Hyderabad Slot 2024
- **Problem Summary:** Find lowest common ancestor node of two nodes $p$ and $q$ in binary tree.
- **Constraints:** Nodes $\le 10^5$.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Approach:** Post-order DFS returning non-null branch.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 7. Symmetric Tree Verification
- **College/Drive:** BofA Campus Slot 2024
- **Problem Summary:** Check if binary tree is symmetric around its center.
- **Constraints:** Nodes $\le 1000$.
- **LeetCode Equivalent:** [101. Symmetric Tree](https://leetcode.com/problems/symmetric-tree/)
- **Approach:** Recursive DFS comparing left and right branches mirror-wise.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 8. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Minimum minutes to infect all items in 2D grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 9. Daily Temperatures / Metric Spike Monotonic Stack
- **College/Drive:** BofA Technical Screen 2024
- **Problem Summary:** Find days to wait for a warmer day.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Coin Change (Fewest Coins)
- **College/Drive:** Off-Campus Screening 2024
- **Problem Summary:** Minimum coins needed to make up amount.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Valid Parentheses (Transaction Validation)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Check if transaction bracket string `()[]{}` is balanced.
- **Constraints:** $1 \le s.length \le 10^4$.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 12. Merge Two Sorted Linked Lists
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Merge two sorted linked lists into one sorted list.
- **Constraints:** Total nodes $\le 100$.
- **LeetCode Equivalent:** [21. Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
- **Complexity:** $O(M + N)$ Time, $O(1)$ Space.

#### 13. Path Sum in Binary Tree
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Check if tree has root-to-leaf path summing to target.
- **Constraints:** Nodes $\le 5000$.
- **LeetCode Equivalent:** [112. Path Sum](https://leetcode.com/problems/path-sum/)
- **Approach:** Recursive DFS subtracting current node value from target sum.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 14. Subarray Sum Equals K
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Count subarrays summing to $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 15. Best Time to Buy and Sell Stock
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Find maximum profit with single buy and sell transaction.
- **Constraints:** $1 \le prices.length \le 10^5$.
- **LeetCode Equivalent:** [121. Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. Product of Array Except Self without Division
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Prefix product pass from left, running suffix product from right.
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

## 🧠 Frequent CS Fundamentals MCQs in Bank of America OA
1. **Database Triggers:**
   - What is a database trigger, and when is it executed?
   - *Answer:* A trigger is a stored procedure automatically invoked by the DBMS in response to specified database events (`INSERT`, `UPDATE`, `DELETE`) on a particular table or view.
2. **Deadlock Conditions (Coffman Conditions):**
   - What are the four simultaneous conditions required for a deadlock?
   - *Answer:* Mutual Exclusion, Hold and Wait, No Preemption, and Circular Wait.
3. **Database Normalization (2NF Requirement):**
   - What is required for a relational table to satisfy Second Normal Form (2NF)?
   - *Answer:* The table must already be in 1NF, and all non-key attributes must be fully functionally dependent on the entire primary key (no partial dependencies on a composite candidate key).
