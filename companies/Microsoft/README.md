# Microsoft Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🪟

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Codility** (Primary) / Mettl (some off-campus drives)
- **Duration:** 75 to 90 minutes (3 Coding Questions)
- **Scoring Mechanism:** 
  - Codility separates score into **Correctness (50%)** and **Performance/Scalability (50%)**.
  - A solution passing all example and small tests will score ~50% if its time complexity is $O(N^2)$ when $O(N)$ or $O(N \log N)$ was expected.
  - Typical Cutoff: Total score $\ge 80\% - 90\%$ is generally required for shortlisting.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Strings & Frequency Maps | Medium | Unique character frequencies, palindrome transformations, anagram segments |
| **Very High** | Arrays & Prefix Sums | Medium | Subarray sums, balance points, maximum chunks to make sorted |
| **High** | Greedy & Sorting | Medium | Interval scheduling, minimum deletions, adjacent swap reductions |
| **High** | Trees & Graph Traversal | Medium | Directed graph cycle detection, tree path sums, disconnected networks |
| **Medium** | Bit Manipulation | Medium | Bitwise AND/OR subsegments, power of two reductions |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Minimum Deletions to Make Character Frequencies Unique
- **Problem Summary:** Given a string $s$, return the minimum number of characters you need to delete to make the frequency of each character in $s$ unique.
- **Constraints:** $1 \le |s| \le 10^5$, lowercase English letters.
- **Approach:** Count frequencies, sort descending or insert into a hash set. Decrement frequency until it is unused or reaches 0.
- **LeetCode Equivalent:** [1647. Minimum Deletions to Make Character Frequencies Unique](https://leetcode.com/problems/minimum-deletions-to-make-character-frequencies-unique/)
- **Complexity:** $O(N + K \log K)$ Time where $K \le 26$, $O(1)$ Space.

### 2. Max Chunks to Make Sorted II (Variations)
- **Problem Summary:** Given an array that may contain duplicates, split it into the maximum number of contiguous chunks such that sorting each chunk individually sorts the entire array.
- **Approach:** Maintain `prefix_max` from left and `suffix_min` from right. A partition is valid at index $i$ if $\max_{0 \dots i} \le \min_{i+1 \dots N-1}$.
- **LeetCode Equivalent:** [768. Max Chunks To Make Sorted II](https://leetcode.com/problems/max-chunks-to-make-sorted-ii/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 3. Min Steps to Make Piles Equal Height (Microsoft Classic)
- **Problem Summary:** You have $N$ boxes of different heights. In each step, you can reduce the tallest box to the height of the next tallest. Find the minimum steps to make all boxes the same height.
- **Approach:** Sort descending; for each distinct element, all previous taller elements require 1 step.
- **Complexity:** $O(N \log N)$ Time.

### 4. Largest K such that both K and -K exist
- **Problem Summary:** Given an array of positive and negative integers, return the largest positive integer $K$ such that both $K$ and $-K$ exist in the array. If no such integer exists, return 0.
- **Approach:** Store all numbers in an unordered set and track maximum positive match.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 5. Count Visible Nodes in Binary Tree (Good Nodes)
- **Problem Summary:** Given a binary tree root, return the number of nodes where the path from the root contains no node with a value greater than that node's value.
- **LeetCode Equivalent:** [1448. Count Good Nodes in Binary Tree](https://leetcode.com/problems/count-good-nodes-in-binary-tree/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

---

## 💡 Cracking Microsoft OA: Proven Tips
1. **Never use $O(N^2)$ nested loops** on arrays of size $N > 10^4$. Codility's automated performance evaluator specifically stresses test cases up to $N = 10^5$.
2. **Handle empty inputs, 1-element arrays, and negative bounds.** Codility tests boundary extremes vigorously.
