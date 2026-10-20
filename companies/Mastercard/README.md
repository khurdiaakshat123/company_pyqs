# Mastercard Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💳

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Core CS & Aptitude MCQs (30 mins)** – 15 to 20 MCQs covering Operating Systems, DBMS/SQL, OOPs (Java focus), Computer Networks, and Quantitative Aptitude.
  2. **Section 2: Hands-On Coding (60 mins, 2 Questions)** – LeetCode Easy to Medium difficulty.
- **Passing Cutoff:** Full test-case clearance on both coding problems + solid performance on Core CS MCQs (>75%).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Arrays & Two Pointers:** Sliding window, subarray sums, running transactions, Kadane's maximum sum.
- **Strings & HashMaps:** Character frequency balancing, anagram verification, Luhn algorithm validation, valid parentheses.
- **SQL Queries & DBMS MCQs:** Joins, `GROUP BY`, indexing, ACID properties, transaction rollback, isolation levels.
- **Trees & Binary Search Trees:** Tree traversals, lowest common ancestor, symmetric tree, BST search.
- **Basic Dynamic Programming:** House robber, coin change, climbing stairs, maximum profit.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Credit Card Luhn Algorithm Validation
- **College/Drive:** BITS Pilani / VIT Vellore 2024
- **Problem Summary:** Implement the Luhn algorithm to check whether a given 16-digit credit card number string is valid.
- **Approach:** Process digits from right to left. Double every second digit; if doubled value $> 9$, subtract 9. Sum all digits and verify if total sum $\pmod{10} == 0$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Subarray Sum Equals K (Transaction Matching)
- **College/Drive:** Thapar University / Manipal 2024
- **Problem Summary:** Given an array of transaction amounts and integer $K$, return total number of continuous subarrays whose sum equals $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix Sum combined with a Hash Map storing frequency of prefix sums.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 3. Symmetric Binary Tree Verification
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** Given the root of a binary tree, check whether it is a mirror of itself (symmetric around center).
- **LeetCode Equivalent:** [101. Symmetric Tree](https://leetcode.com/problems/symmetric-tree/)
- **Approach:** Recursive DFS comparing left subtree with right subtree (`left->val == right->val && isMirror(left->left, right->right) && isMirror(left->right, right->left)`).
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 4. Minimum Steps to Make Two Strings Anagram
- **College/Drive:** SRM University / PES 2024
- **Problem Summary:** Given two strings $s$ and $t$ of equal length, return the minimum character replacements in $t$ to make it an anagram of $s$.
- **LeetCode Equivalent:** [1347. Minimum Number of Steps to Make Two Strings Anagram](https://leetcode.com/problems/minimum-number-of-steps-to-make-two-strings-anagram/)
- **Approach:** Frequency count array of 26 letters; sum differences where `count_s > count_t`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Longest Substring Without Repeating Characters
- **College/Drive:** Mastercard Accelerate Campus 2024
- **Problem Summary:** Given a transaction string, find length of longest substring without repeating characters.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with a hash map / 128-element array tracking the last seen index of each character.
- **Complexity:** $O(N)$ Time, $O(1)$ Auxiliary Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Find contiguous subarray with largest sum.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. House Robber (Maximum Cash Optimization)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Maximize cash robbed without alerting security on adjacent houses.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** Dynamic Programming: `dp = max(prev1, prev2 + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Merge Two Sorted Linked Lists
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Merge two sorted linked lists into one sorted linked list in-place.
- **LeetCode Equivalent:** [21. Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
- **Complexity:** $O(M + N)$ Time, $O(1)$ Space.

#### 9. Lowest Common Ancestor in a Binary Search Tree
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Find lowest common ancestor in BST.
- **LeetCode Equivalent:** [235. Lowest Common Ancestor of a Binary Search Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/)
- **Approach:** Compare node value with $p$ and $q$. If both greater, go right; if both smaller, go left; else current node is LCA.
- **Complexity:** $O(H)$ Time, $O(1)$ Space.

#### 10. Coin Change (Fewest Coins)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find minimum number of coins to make up given amount.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time, $O(\text{amount})$ Space.

---

## 🧠 Frequent CS Fundamentals & SQL MCQs in Mastercard OA
1. **Database ACID Properties:**
   - What does Atomicity guarantee in banking transactions?
   - *Answer:* All operations within a transaction either execute completely or roll back entirely with no intermediate or partial updates left behind.
2. **REST API Idempotency:**
   - Which HTTP methods are inherently idempotent according to RFC specifications?
   - *Answer:* `GET`, `PUT`, `DELETE`, and `HEAD` are idempotent. `POST` is NOT idempotent.
3. **Java Strings & Garbage Collection:**
   - Why are Strings immutable in Java?
   - *Answer:* Security (network connections, file paths), caching in the String Pool, thread safety without synchronization, and hash code caching for collections.
