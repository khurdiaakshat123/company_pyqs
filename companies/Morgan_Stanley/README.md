# Morgan Stanley Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **Aspiring Minds (AMCAT)**
- **Test Duration:** 75 to 90 minutes
- **Structure Breakdown (Strict Sectional Timers):**
  1. **Section 1: Quantitative & Logical Aptitude** (~10 Questions, 20 mins) – Financial arithmetic, percentages, probability, and analytical puzzles.
  2. **Section 2: Code Debugging** (~7 to 10 Questions, 20 mins) – Identify and fix syntax errors, off-by-one errors, or improper pointer/loop logic in pre-written snippets (C++, Java, or Python).
  3. **Section 3: Algorithmic Coding** (2 to 3 Coding Problems, 45–50 mins) – Medium difficulty problems.
- **Sectional Movement:** Strict timers per section; once a section's timer expires, candidates cannot return to make modifications.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Code Debugging | Easy - Medium | Off-by-one errors, null pointer checks, integer overflow, incorrect condition checks |
| **Very High** | Array & String Two Pointers | Medium | Sliding window, interval merging, prefix sums, container with most water |
| **High** | Stack & Queue Applications | Medium | Longest valid parentheses, daily temperatures, stock span problem |
| **High** | Dynamic Programming | Medium | Longest common subsequence, coin change, partition equal subset sum |
| **Medium** | Math & Financial Logic | Medium | Stock profit with cooldown, transaction fee optimizations |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Merge Intervals / Portfolio Trade Reconciliation
- **Problem Summary:** Given an array of `intervals` where `intervals[i] = [start_i, end_i]`, merge all overlapping intervals, and return an array of the non-overlapping intervals that cover all the intervals in the input.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort intervals by start time; iterate through and merge overlapping intervals with running end time tracker.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

### 2. Stock Span Problem / Monotonic Stack
- **Problem Summary:** The stock span problem is a financial problem where we have a series of $n$ daily price quotes for a stock and we need to calculate the span of stock’s price for all $n$ days (maximum consecutive days for which price was $\le$ current day's price).
- **LeetCode Equivalent:** [901. Online Stock Span](https://leetcode.com/problems/online-stock-span/)
- **Approach:** Monotonic Decreasing Stack storing pairs of `(price, span)`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 3. Longest Valid Parentheses
- **Problem Summary:** Given a string containing just the characters `'('` and `')'`, return the length of the longest valid (well-formed) parentheses substring.
- **LeetCode Equivalent:** [32. Longest Valid Parentheses](https://leetcode.com/problems/longest-valid-parentheses/)
- **Approach:** Stack initialized with `-1` storing indices or two-pass left-to-right & right-to-left counter.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 4. Minimum Operations to Reduce Array to Zero
- **Problem Summary:** In each step, choose the smallest positive non-zero number $x$ in the array and subtract $x$ from all positive elements. Return the total number of operations required.
- **LeetCode Equivalent:** [2357. Make Array Zero by Subtracting Equal Amounts](https://leetcode.com/problems/make-array-zero-by-subtracting-equal-amounts/)
- **Approach:** Count the number of distinct positive integers in the array using a Hash Set.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

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
