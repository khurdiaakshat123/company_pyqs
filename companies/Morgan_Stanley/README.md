# Morgan Stanley Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **Aspiring Minds (AMCAT)**
- **Test Duration:** 75 to 90 minutes
- **Structure Breakdown (Strict Sectional Timers):**
  1. **Section 1: Quantitative & Logical Aptitude** (~10 Questions, 20 mins) – Financial arithmetic, percentages, probability, and analytical puzzles.
  2. **Section 2: Code Debugging** (~7 to 10 Questions, 20 mins) – Identify and fix syntax errors, off-by-one errors, or improper pointer/loop logic in pre-written snippets (C++, Java, or Python).
  3. **Section 3: Algorithmic Coding** (2 to 3 Coding Problems, 45–50 mins) – Medium difficulty problems.
- **Sectional Movement:** Strict timers per section; once a section's timer expires, candidates cannot return to make modifications.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Code Debugging:** Off-by-one errors, null pointer checks, integer overflow, improper swap bounds.
- **Array & String Two Pointers:** Sliding window, interval merging, prefix sums, container with most water.
- **Stack & Queue Applications:** Longest valid parentheses, daily temperatures, stock span problem, circular next greater element.
- **Dynamic Programming:** Longest common subsequence, coin change, partition equal subset sum, house robber.
- **Math & Financial Logic:** Stock profit with cooldown, transaction fee optimizations, peak finding.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Merge Intervals / Portfolio Trade Reconciliation
- **College/Drive:** IIT Roorkee / BITS Pilani 2024–2025
- **Problem Summary:** Given an array of `intervals` where `intervals[i] = [start_i, end_i]`, merge all overlapping intervals, and return an array of the non-overlapping intervals that cover all the intervals in the input.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort intervals by start time; iterate through and merge overlapping intervals with running end time tracker.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 2. Stock Span Problem / Monotonic Stack
- **College/Drive:** NIT Trichy / DTU 2024–2025
- **Problem Summary:** Calculate the span of stock’s price for all $n$ days (maximum consecutive days for which price was $\le$ current day's price).
- **Constraints:** $1 \le n \le 10^5$.
- **LeetCode Equivalent:** [901. Online Stock Span](https://leetcode.com/problems/online-stock-span/)
- **Approach:** Monotonic Decreasing Stack storing pairs of `(price, span)`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 3. Longest Valid Parentheses (Stack Classic)
- **College/Drive:** IIIT Allahabad 2024–2025
- **Problem Summary:** Given a string containing just the characters `'('` and `')'`, return the length of the longest valid (well-formed) parentheses substring.
- **Constraints:** $1 \le s.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [32. Longest Valid Parentheses](https://leetcode.com/problems/longest-valid-parentheses/)
- **Approach:** Stack initialized with `-1` storing indices or two-pass left-to-right & right-to-left counter.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Minimum Operations to Reduce Array to Zero
- **College/Drive:** Morgan Stanley Code to Give 2024–2025
- **Problem Summary:** In each step, choose smallest positive non-zero number $x$ in array and subtract from all positive elements. Return operations count.
- **Constraints:** $1 \le nums.length \le 100$.
- **LeetCode Equivalent:** [2357. Make Array Zero by Subtracting Equal Amounts](https://leetcode.com/problems/make-array-zero-by-subtracting-equal-amounts/)
- **Approach:** Count the number of distinct positive integers in the array using a Hash Set.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 5. Partition Equal Subset Sum (0/1 Knapsack DP)
- **College/Drive:** Campus Placement Drive 2024–2025
- **Problem Summary:** Given an array `nums`, return `true` if you can partition into two subsets with equal sum.
- **Constraints:** $1 \le nums.length \le 200$, $1 \le nums[i] \le 100$.
- **LeetCode Equivalent:** [416. Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum/)
- **Approach:** Target sum is $\frac{\text{sum}}{2}$. 1D boolean DP array traversed right-to-left.
- **Complexity:** $O(N \times \text{target})$ Time.

#### 6. Subarray Sum Equals K / Cash Flow Balance
- **College/Drive:** Morgan Stanley Bangalore Drive 2024
- **Problem Summary:** Find total continuous periods where net cash transactions equal target $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Hash Map tracking prefix sum frequencies.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Next Greater Element II (Circular Monotonic Stack)
- **College/Drive:** NIT Warangal / IIT BHU 2024
- **Problem Summary:** Given a circular integer array `nums`, return the next greater number for every element. If it doesn't exist, return -1.
- **Constraints:** $1 \le nums.length \le 10^4$.
- **LeetCode Equivalent:** [503. Next Greater Element II](https://leetcode.com/problems/next-greater-element-ii/)
- **Approach:** Monotonic Decreasing Stack simulated over array of size $2N$ using modulo indexing `i % n`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 8. Course Schedule II (Workflow Dependency Ordering)
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Given dependencies, find an order of tasks to complete all, or empty array if impossible.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm for Topological Sort using indegree array and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 9. Rotten Oranges / Contagion Spread
- **College/Drive:** Mumbai Campus Drive 2024
- **Problem Summary:** Compute minimum time for all items to be infected in a 2D grid.
- **Constraints:** $M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \cdot N)$ Time and Space.

#### 10. Word Break (Dynamic Programming)
- **College/Drive:** Off-Campus Hiring 2024
- **Problem Summary:** Determine if string $s$ can be segmented into words in a dictionary.
- **Constraints:** $1 \le s.length \le 300$.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Approach:** 1D boolean DP array with hash set lookup.
- **Complexity:** $O(N^2 \cdot L)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Best Time to Buy and Sell Stock II (Greedy Peak-Valley)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Maximum profit with multiple buy and sell transactions.
- **Constraints:** $1 \le prices.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [122. Best Time to Buy and Sell Stock II](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-ii/)
- **Approach:** Greedy: accumulate `prices[i] - prices[i-1]` whenever price increases.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Container With Most Water
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Two pointers inward maximizing area between vertical bars.
- **Constraints:** $2 \le heights.length \le 10^5$.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Approach:** Two pointers moving whichever bar has smaller height.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 13. Longest Substring Without Repeating Characters
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Sliding window with hash map of character indices.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Two-pointer sliding window updating `left = max(left, last_seen[ch] + 1)`.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 14. Coin Change (Fewest Coins)
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Dynamic programming coin change for target amount.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 15. Trapping Rain Water
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. Find Peak Element
- **College/Drive:** Morgan Stanley Slot 2023
- **Problem Summary:** Find a peak element in an array where $nums[i] \ne nums[i+1]$ in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 1000$.
- **LeetCode Equivalent:** [162. Find Peak Element](https://leetcode.com/problems/find-peak-element/)
- **Approach:** Binary Search: if `nums[mid] < nums[mid + 1]`, search right half; else search left half.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 17. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Campus Technical Screen 2023
- **Problem Summary:** Find contiguous subarray with largest sum.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Approach:** Running sum: `curr = max(x, curr + x)`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 18. House Robber (1D Dynamic Programming)
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Maximize stolen value without robbing two adjacent houses.
- **Constraints:** $1 \le nums.length \le 100$.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** DP: `dp[i] = max(dp[i-1], dp[i-2] + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 19. Binary Tree Right Side View
- **College/Drive:** Off-Campus Drive 2023
- **Problem Summary:** Return list of values of nodes visible from right side of binary tree.
- **Constraints:** Nodes $\le 100$.
- **LeetCode Equivalent:** [199. Binary Tree Right Side View](https://leetcode.com/problems/binary-tree-right-side-view/)
- **Approach:** BFS level-order traversal saving the last node in each level.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 20. Kth Largest Element in an Array
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Return $K$-th largest element in unsorted array.
- **Constraints:** $1 \le k \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [215. Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/)
- **Approach:** Min-Heap of size $K$ or Quickselect in $O(N)$ average time.
- **Complexity:** $O(N \log K)$ Time, $O(K)$ Space.

---

## 🐞 Frequent Debugging Snippets in Morgan Stanley OA
1. **Loop Termination Bug:**
   ```cpp
   // Buggy: Infinite loop or off-by-one condition
   for (int i = 0; i <= n; i++) { // Fix: change <= to <
       arr[i] = arr[i] * 2;
   }
   ```
2. **String Reversal Swap:**
   ```cpp
   // Buggy: Swapping entire length instead of half (undoes itself)
   for (int i = 0; i < len; i++) { // Fix: change len to len / 2
       swap(str[i], str[len - i - 1]);
   }
   ```
3. **Integer Overflow in Multiplication:**
   ```cpp
   // Buggy: Integer multiplication overflow before assignment to long long
   long long product = a * b; // Fix: static_cast<long long>(a) * b
   ```
4. **Pointer Aliasing in Linked List Reversal:**
   ```cpp
   // Buggy: Lost next pointer reference
   curr->next = prev;
   curr = next; // Fix: cache next = curr->next before modifying curr->next
   ```
