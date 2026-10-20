# JPMorgan Chase (JPMC) Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) 🏛️

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

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Arrays & Prefix Sums:** Running sum, subarray target sum, equilibrium index.
- **Strings & HashMaps:** Group anagrams, frequency counting, valid parenthesis strings.
- **Sliding Window & Two Pointers:** Subarray product less than K, minimum window substring.
- **Binary Trees & BFS:** Level order traversal, right side view, symmetric tree.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Count Subarrays with Sum Equal to K (JPMC Classic)
- **College/Drive:** JPMC Code for Good 2024
- **Problem Summary:** Given an array of integers `nums` and an integer `k`, return the total number of continuous subarrays whose sum equals to `k`.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Maintain `current_sum` and a Hash Map storing frequencies of prefix sums. For each element, add `map[current_sum - k]` to answer.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 2. Group Anagrams / Transaction Clustering
- **College/Drive:** IIT Roorkee / BITS Pilani 2024
- **Problem Summary:** Given an array of strings `strs`, group the anagrams together in any order.
- **LeetCode Equivalent:** [49. Group Anagrams](https://leetcode.com/problems/group-anagrams/)
- **Approach:** Use sorted string or 26-element character frequency array as HashMap key.
- **Complexity:** $O(N \times K \log K)$ Time.

#### 3. Binary Tree Level Order Traversal
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Summary:** Given the root of a binary tree, return the level order traversal of its nodes' values (i.e., from left to right, level by level).
- **LeetCode Equivalent:** [102. Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/)
- **Approach:** Standard queue-based BFS tracking level size.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 4. Minimum Path Sum in Grid (2D DP)
- **College/Drive:** IIIT Delhi 2024
- **Problem Summary:** Given an $m \times n$ grid filled with non-negative numbers, find a path from top left to bottom right, which minimizes the sum of all numbers along its path (moving only down or right).
- **LeetCode Equivalent:** [64. Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/)
- **Approach:** 2D DP: `dp[i][j] = grid[i][j] + min(dp[i-1][j], dp[i][j-1])`.
- **Complexity:** $O(M \times N)$ Time, $O(N)$ Space.

#### 5. Best Time to Buy and Sell Stock (Single Transaction)
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Maximize profit choosing a single day to buy and a different day in future to sell.
- **LeetCode Equivalent:** [121. Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- **Approach:** One pass tracking `min_price_so_far`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Valid Parentheses
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Check if brackets in transaction string are balanced.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Complexity:** $O(N)$ Time.

#### 7. Merge Intervals
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Merge overlapping transaction settlement intervals.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time.

#### 8. Container With Most Water
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Two pointers inward maximizing area between vertical lines.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Complexity:** $O(N)$ Time.

#### 9. Coin Change (Fewest Denominations)
- **College/Drive:** Code for Good 2023
- **Problem Statement:** Minimum coins to make exact payment amount.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 10. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Sliding window with hash map of character indices.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time.
