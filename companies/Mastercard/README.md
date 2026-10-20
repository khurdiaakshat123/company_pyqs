# Mastercard Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 💳

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Core CS & Aptitude MCQs (30 mins)** – 15 to 20 MCQs covering Operating Systems, DBMS/SQL, OOPs (Java focus), Computer Networks, and Quantitative Aptitude.
  2. **Section 2: Hands-On Coding (60 mins, 2 Questions)** – LeetCode Easy to Medium difficulty.
- **Passing Cutoff:** Full test-case clearance on both coding problems + solid performance on Core CS MCQs.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Arrays & Two Pointers | Easy - Medium | Sliding window, subarray sums, running transactions |
| **Very High** | Strings & HashMaps | Easy - Medium | Character frequency balancing, anagram verification, valid parentheses |
| **High** | SQL Queries & DBMS MCQs | Medium | Joins, `GROUP BY`, indexing, ACID properties, transaction rollback |
| **High** | Trees & Binary Search Trees | Medium | Tree traversals, lowest common ancestor, symmetric tree |
| **Medium** | Basic Dynamic Programming | Medium | House robber, coin change, climbing stairs |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Credit Card Luhn Algorithm Validation
- **Problem Summary:** Implement the Luhn algorithm to check whether a given 16-digit credit card number string is valid.
- **Approach:** Process digits from right to left. Double every second digit; if the doubled value $> 9$, subtract 9. Sum all digits and verify if total sum $\pmod{10} == 0$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 2. Subarray Sum Equals K (Transaction Matching)
- **Problem Summary:** Given an array of integers `nums` and an integer `k`, return the total number of continuous subarrays whose sum equals to `k`.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix Sum combined with a Hash Map storing frequency of prefix sums.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 3. Check for Symmetric Binary Tree
- **Problem Summary:** Given the root of a binary tree, check whether it is a mirror of itself (i.e., symmetric around its center).
- **LeetCode Equivalent:** [101. Symmetric Tree](https://leetcode.com/problems/symmetric-tree/)
- **Approach:** Recursive DFS comparing left subtree with right subtree (`left->val == right->val && isMirror(left->left, right->right) && isMirror(left->right, right->left)`).
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

### 4. Minimum Steps to Make Two Strings Anagram
- **Problem Summary:** You are given two strings of the same length $s$ and $t$. In one step you can choose any character of $t$ and replace it with another character. Return the minimum number of steps to make $t$ an anagram of $s$.
- **LeetCode Equivalent:** [1347. Minimum Number of Steps to Make Two Strings Anagram](https://leetcode.com/problems/minimum-number-of-steps-to-make-two-strings-anagram/)
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.
