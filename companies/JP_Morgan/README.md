# JPMorgan Chase (JPMC) Online Assessment Guide & PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Flagship Hiring Channels:**
  - **Code for Good (CFG) Hackathon:** Premier hiring pipeline for summer internships & full-time roles (14–19 LPA).
  - **JPMorgan Tech Connect / Campus Drives**
- **Test Duration:** 60 minutes
- **Structure Breakdown:**
  - **Coding Section:** 2 Algorithmic Coding Problems (LeetCode Easy to Medium difficulty, 60 mins).
  - **Behavioral Screening (HireVue / Pymetrics):** 2 video response questions explaining personal teamwork and problem resolution, or 12 gamified cognitive mini-games measuring risk tolerance and memory.
- **Passing Cutoff:** Full score on both coding questions (all public and hidden test cases passed) is essential to advance to the CFG hackathon stage or final interview round.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Arrays & Prefix Sums | Easy - Medium | Running sum, subarray target sum, equilibrium index |
| **Very High** | Strings & HashMaps | Easy - Medium | Group anagrams, frequency counting, valid parenthesis strings |
| **High** | Sliding Window & Two Pointers | Medium | Subarray product less than K, minimum window substring |
| **High** | Binary Trees & BFS | Medium | Level order traversal, right side view, symmetric tree |
| **Medium** | Dynamic Programming | Medium | Stock buy & sell variations, minimum path sum in grid |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Count Subarrays with Sum Equal to K
- **Problem Summary:** Given an array of integers `nums` and an integer `k`, return the total number of continuous subarrays whose sum equals to `k`.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Maintain `current_sum` and a Hash Map storing frequencies of prefix sums. For each element, add `map[current_sum - k]` to answer.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 2. Group Anagrams / Transaction Clustering
- **Problem Summary:** Given an array of strings `strs`, group the anagrams together in any order.
- **LeetCode Equivalent:** [49. Group Anagrams](https://leetcode.com/problems/group-anagrams/)
- **Approach:** Use sorted string or 26-element character frequency array as HashMap key.
- **Complexity:** $O(N \times K \log K)$ Time.

### 3. Binary Tree Level Order Traversal
- **Problem Summary:** Given the root of a binary tree, return the level order traversal of its nodes' values (i.e., from left to right, level by level).
- **LeetCode Equivalent:** [102. Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/)
- **Approach:** Standard queue-based BFS tracking level size.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 4. Minimum Path Sum in Grid
- **Problem Summary:** Given an $m \times n$ grid filled with non-negative numbers, find a path from top left to bottom right, which minimizes the sum of all numbers along its path (moving only down or right).
- **LeetCode Equivalent:** [64. Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/)
- **Approach:** 2D DP: `dp[i][j] = grid[i][j] + min(dp[i-1][j], dp[i][j-1])`.
- **Complexity:** $O(M \times N)$ Time, $O(N)$ Space.
