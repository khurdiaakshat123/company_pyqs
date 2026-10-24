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
- **Arrays & Prefix Sums:** Running sum, subarray target sum, equilibrium index, divisibility by K.
- **Strings & HashMaps:** Group anagrams, frequency counting, valid parenthesis strings, longest substring without repeats.
- **Sliding Window & Two Pointers:** Subarray product less than K, minimum window substring, container with most water.
- **Binary Trees & BFS:** Level order traversal, right side view, lowest common ancestor.
- **Dynamic Programming:** Minimum path sum in 2D grid, coin change, longest palindromic substring.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Count Subarrays with Sum Equal to K (JPMC Classic)
- **College/Drive:** JPMC Code for Good 2024–2025
- **Problem Summary:** Given an array of integers `nums` and an integer `k`, return the total number of continuous subarrays whose sum equals to `k`.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$, $-1000 \le nums[i] \le 1000$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Maintain `current_sum` and a Hash Map storing frequencies of prefix sums. For each element, add `map[current_sum - k]` to answer.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 2. Group Anagrams / Transaction Clustering
- **College/Drive:** IIT Roorkee / BITS Pilani 2024–2025
- **Problem Summary:** Given an array of strings `strs`, group the anagrams together in any order.
- **Constraints:** $1 \le strs.length \le 10^4$, $0 \le strs[i].length \le 100$.
- **LeetCode Equivalent:** [49. Group Anagrams](https://leetcode.com/problems/group-anagrams/)
- **Approach:** Use sorted string or 26-element character frequency array as HashMap key.
- **Complexity:** $O(N \times K \log K)$ Time.

#### 3. Binary Tree Level Order Traversal
- **College/Drive:** NIT Trichy / DTU 2024–2025
- **Problem Summary:** Given the root of a binary tree, return the level order traversal of its nodes' values (i.e., from left to right, level by level).
- **Constraints:** Nodes $\le 2000$.
- **LeetCode Equivalent:** [102. Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/)
- **Approach:** Standard queue-based BFS tracking level size.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 4. Minimum Path Sum in Grid (2D DP)
- **College/Drive:** IIIT Delhi 2024–2025
- **Problem Summary:** Given an $m \times n$ grid filled with non-negative numbers, find a path from top left to bottom right, which minimizes the sum of all numbers along its path (moving only down or right).
- **Constraints:** $1 \le m, n \le 200$.
- **LeetCode Equivalent:** [64. Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/)
- **Approach:** 2D DP: `dp[i][j] = grid[i][j] + min(dp[i-1][j], dp[i][j-1])`.
- **Complexity:** $O(M \times N)$ Time, $O(N)$ Space.

#### 5. Best Time to Buy and Sell Stock (Single Transaction)
- **College/Drive:** Campus Placement 2024–2025
- **Problem Summary:** Maximize profit choosing a single day to buy and a different day in future to sell.
- **Constraints:** $1 \le prices.length \le 10^5$.
- **LeetCode Equivalent:** [121. Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- **Approach:** One pass tracking `min_price_so_far`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 6. Subarray Sums Divisible by K
- **College/Drive:** JPMC Code for Good 2024
- **Problem Summary:** Given an integer array `nums` and an integer `k`, return the number of non-empty subarrays that have a sum divisible by `k`.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$, $2 \le k \le 10^4$.
- **LeetCode Equivalent:** [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- **Approach:** Prefix sum modulo $k$ frequency hash map: normalize remainder `((sum % k) + k) % k`.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 7. Rotten Oranges / Contagion Spread
- **College/Drive:** JPMC Off-Campus 2024
- **Problem Summary:** Minimum minutes to infect all oranges in grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 8. Longest Palindromic Substring
- **College/Drive:** IIT BHU / NIT Surathkal 2024
- **Problem Summary:** Given a string $s$, return the longest palindromic substring in $s$.
- **Constraints:** $1 \le s.length \le 1000$.
- **LeetCode Equivalent:** [5. Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/)
- **Approach:** Expand around center for all $2N - 1$ centers (odd and even length).
- **Complexity:** $O(N^2)$ Time, $O(1)$ Space.

#### 9. Daily Temperatures / Transaction Spikes
- **College/Drive:** Campus Slot 2024
- **Problem Summary:** Find days to wait for a warmer day.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Course Schedule (Cycle Detection)
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** Determine if candidate can finish all courses given prerequisites.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Kahn's Algorithm (BFS topological sort indegree count).
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Valid Parentheses
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Check if brackets in transaction string are balanced.
- **Constraints:** $1 \le s.length \le 10^4$.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Stack matching opening brackets.
- **Complexity:** $O(N)$ Time.

#### 12. Merge Intervals
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Merge overlapping transaction settlement intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time; merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 13. Container With Most Water
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Two pointers inward maximizing area between vertical lines.
- **Constraints:** $2 \le heights.length \le 10^5$.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Approach:** Two pointers moving shorter bar inwards.
- **Complexity:** $O(N)$ Time.

#### 14. Coin Change (Fewest Denominations)
- **College/Drive:** Code for Good 2023
- **Problem Summary:** Minimum coins to make exact payment amount.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 15. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Sliding window with hash map of character indices.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Two-pointer sliding window with last seen map.
- **Complexity:** $O(N)$ Time.

#### 16. Product of Array Except Self
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Compute array product except self without division in $O(N)$ time.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Prefix product pass from left, running suffix product from right.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 17. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** CFG Hackathon Screening 2023
- **Problem Summary:** Find maximum subarray sum.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Approach:** Kadane's algorithm.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 18. Two Sum
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Find two indices whose values add up to target.
- **Constraints:** $2 \le nums.length \le 10^4$.
- **LeetCode Equivalent:** [1. Two Sum](https://leetcode.com/problems/two-sum/)
- **Approach:** Hash Map storing `target - nums[i]`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 19. Search in Rotated Sorted Array
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Search target in rotated sorted array in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 5000$.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Modified Binary Search determining which half is sorted.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 20. Lowest Common Ancestor of Binary Tree
- **College/Drive:** Advanced SDE 2023
- **Problem Summary:** Find lowest common ancestor of two nodes in binary tree.
- **Constraints:** Nodes $\le 10^5$.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Approach:** Post-order DFS returning non-null branch when matching $p$ or $q$.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

---

## 💡 Cracking JPMorgan Code for Good (CFG) & HireVue
1. **Speed & 100% Test Cases:** JPMC OA has relatively accessible LeetCode Easy/Medium problems, meaning thousands of candidates get full marks. Solving them quickly with clean variable naming places you higher on the CFG shortlist.
2. **Behavioral HireVue / STAR Method:** For the video prompts, structure answers using the STAR method (Situation, Task, Action, Result) with explicit emphasis on collaboration, non-profit impact, and resolving team conflicts.
