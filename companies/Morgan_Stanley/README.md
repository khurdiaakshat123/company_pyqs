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
- **Code Debugging:** Off-by-one errors, null pointer checks, integer overflow, incorrect condition checks.
- **Array & String Two Pointers:** Sliding window, interval merging, prefix sums, container with most water.
- **Stack & Queue Applications:** Longest valid parentheses, daily temperatures, stock span problem.
- **Dynamic Programming:** Longest common subsequence, coin change, partition equal subset sum.
- **Math & Financial Logic:** Stock profit with cooldown, transaction fee optimizations.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Merge Intervals / Portfolio Trade Reconciliation
- **College/Drive:** IIT Roorkee / BITS Pilani 2024
- **Problem Summary:** Given an array of `intervals` where `intervals[i] = [start_i, end_i]`, merge all overlapping intervals, and return an array of the non-overlapping intervals that cover all the intervals in the input.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort intervals by start time; iterate through and merge overlapping intervals with running end time tracker.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 2. Stock Span Problem / Monotonic Stack
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Summary:** Calculate the span of stock’s price for all $n$ days (maximum consecutive days for which price was $\le$ current day's price).
- **LeetCode Equivalent:** [901. Online Stock Span](https://leetcode.com/problems/online-stock-span/)
- **Approach:** Monotonic Decreasing Stack storing pairs of `(price, span)`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 3. Longest Valid Parentheses (Stack Classic)
- **College/Drive:** IIIT Allahabad 2024
- **Problem Summary:** Given a string containing just the characters `'('` and `')'`, return the length of the longest valid (well-formed) parentheses substring.
- **LeetCode Equivalent:** [32. Longest Valid Parentheses](https://leetcode.com/problems/longest-valid-parentheses/)
- **Approach:** Stack initialized with `-1` storing indices or two-pass left-to-right & right-to-left counter.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Minimum Operations to Reduce Array to Zero
- **College/Drive:** Morgan Stanley Code to Give 2024
- **Problem Summary:** In each step, choose smallest positive non-zero number $x$ in array and subtract from all positive elements. Return operations count.
- **LeetCode Equivalent:** [2357. Make Array Zero by Subtracting Equal Amounts](https://leetcode.com/problems/make-array-zero-by-subtracting-equal-amounts/)
- **Approach:** Count the number of distinct positive integers in the array using a Hash Set.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 5. Partition Equal Subset Sum (0/1 Knapsack DP)
- **College/Drive:** Campus Placement Drive 2024
- **Problem Summary:** Given an array `nums`, return `true` if you can partition into two subsets with equal sum.
- **LeetCode Equivalent:** [416. Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum/)
- **Approach:** Target sum is $\frac{\text{sum}}{2}$. 1D boolean DP array.
- **Complexity:** $O(N \times \text{target})$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Best Time to Buy and Sell Stock II (Greedy Peak-Valley)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Maximum profit with multiple buy and sell transactions.
- **LeetCode Equivalent:** [122. Best Time to Buy and Sell Stock II](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-ii/)
- **Complexity:** $O(N)$ Time.

#### 7. Container With Most Water
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Two pointers inward maximizing area between vertical bars.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Complexity:** $O(N)$ Time.

#### 8. Longest Substring Without Repeating Characters
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Sliding window with hash map of character indices.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time.

#### 9. Coin Change (Fewest Coins)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Dynamic programming coin change.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 10. Trapping Rain Water
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Elevation histogram water capacity.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time.

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
   // Buggy: Swapping entire length instead of half
   for (int i = 0; i < len; i++) { // Fix: change len to len / 2
       swap(str[i], str[len - i - 1]);
   }
   ```
