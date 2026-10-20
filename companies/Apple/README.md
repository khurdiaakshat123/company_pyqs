# Apple Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🍎

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **CodeSignal**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  - **Coding Section:** 2 to 3 Coding Problems (Easy-Medium to Medium-Hard).
  - **Core CS Section:** 10 to 15 MCQs covering Operating Systems (Processes, Threads, Semaphores), Computer Networks (TCP/UDP, DNS), and C++ / Swift memory management.
- **Evaluation Criteria:** Apple places extreme emphasis on clean, idiomatic code, handling edge cases, and algorithmic efficiency. On CodeSignal, strict test-case coverage determines the candidate's invitation to team interviews.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Strings & Text Parsing:** Substring matching, custom compression, balanced delimiters.
- **Arrays & Sliding Window:** Minimum operations, maximum subarray sum, monotonic properties.
- **Trees & Graph Traversal:** BFS / DFS, Tree level-order variations, connected components.
- **Dynamic Programming:** Knapsack variants, word break, matrix minimum path sums.
- **System & Low-Level Concepts:** Memory layouts, reference counting / ARC (Automatic Reference Counting), concurrency.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Minimum Operations to Reduce Array / Longest Subarray
- **College/Drive:** IIT Roorkee / IIT Madras 2024
- **Problem Summary:** Given an array of integers `nums` and an integer `x`. In one operation, you can remove either the leftmost or the rightmost element from the array and subtract its value from `x`. Return the minimum number of operations to reduce `x` to exactly `0`, or `-1` if impossible.
- **LeetCode Equivalent:** [1658. Minimum Operations to Reduce X to Zero](https://leetcode.com/problems/minimum-operations-to-reduce-x-to-zero/)
- **Approach:** Invert the problem: Find the longest contiguous subarray whose sum equals $\sum nums - x$ using a sliding window.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Word Break & Dictionary Segment Matching
- **College/Drive:** BITS Pilani / NIT Trichy 2024
- **Problem Summary:** Given a string $s$ and a dictionary of strings `wordDict`, return `true` if $s$ can be segmented into a space-separated sequence of one or more dictionary words.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Approach:** 1D Dynamic Programming: `dp[i]` is true if a valid prefix exists such that `dp[j]` is true and $s[j \dots i]$ is in the dictionary (or using a Trie).
- **Complexity:** $O(N^2)$ Time, $O(N)$ Space.

#### 3. Maximum Number of Events That Can Be Attended (Min-Heap)
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** You are given an array of `events` where `events[i] = [startDay, endDay]`. You can attend at most one event on any given day. Return the maximum number of events you can attend.
- **LeetCode Equivalent:** [1353. Maximum Number of Events That Can Be Attended](https://leetcode.com/problems/maximum-number-of-events-that-can-be-attended/)
- **Approach:** Sort events by start day, maintain a Min-Heap of end days for active events, and greedily attend the event ending earliest each day.
- **Complexity:** $O(D + N \log N)$ where $D$ is max days.

#### 4. Tree Vertical Level Sum
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Summary:** Given a binary tree, return the vertical sum of all nodes lying on the same vertical line (assigning root coordinate 0, left child -1, right child +1).
- **Complexity:** $O(N \log N)$ or $O(N)$ with HashMap + BFS.

#### 5. Longest Palindromic Subsequence
- **College/Drive:** Apple Hardware/Software Campus 2024
- **Problem Summary:** Given a string $s$, find the longest palindromic subsequence's length in $s$.
- **LeetCode Equivalent:** [516. Longest Palindromic Subsequence](https://leetcode.com/problems/longest-palindromic-subsequence/)
- **Approach:** 2D DP: If $s[i] == s[j]$, $dp[i][j] = 2 + dp[i+1][j-1]$; else $\max(dp[i+1][j], dp[i][j-1])$.
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Find contiguous subarray with largest sum.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time.

#### 7. Lowest Common Ancestor of Binary Tree
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** LCA of nodes $p$ and $q$ in binary tree.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Complexity:** $O(N)$ Time.

#### 8. Merge Two Sorted Lists
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Merge two sorted linked lists.
- **LeetCode Equivalent:** [21. Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
- **Complexity:** $O(N + M)$ Time.

#### 9. Valid Parentheses
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Check matching brackets using Stack.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Complexity:** $O(N)$ Time.

#### 10. Coin Change (Fewest Denominations)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Fewest coins to form amount.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time.
