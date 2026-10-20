# Meta (Facebook) Online Assessment Guide & PYQs (2023 - 2025/2026) ♾️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **CodeSignal** / **HackerRank** / Meta Internal Assessment Portal
- **Test Duration:** 45 to 70 minutes
- **Structure Breakdown:**
  - 2 to 4 Algorithmic Coding Problems (LeetCode Medium to Hard).
  - In technical phone screening / automated OAs, candidates typically have **45 minutes to solve 2 distinct problems completely**.
- **The "Meta Speed Benchmark":**
  - Meta evaluates speed and immediate optimal execution. You are expected to produce clean, bug-free code with optimal time/space complexity within 15–20 minutes per problem.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

Meta's question bank heavily revolves around classic, well-defined algorithmic patterns:

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Extremely High** | Two Pointers & Binary Search | Medium | Subarray sums, rotated array searches, palindrome extensions |
| **Very High** | HashMaps & Frequency Counters | Easy - Medium | Subarray sum equals K, dot product of sparse vectors, custom sort |
| **Very High** | Trees & Lowest Common Ancestor | Medium | Post-order traversal, LCA with parent pointers, vertical order |
| **High** | Breadth-First & Depth-First Search | Medium - Hard | Shortest path on grid, word ladder, connected islands |
| **Medium** | Monotonic Stack & Heaps | Medium | Valid parentheses removal, K closest points to origin |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Dot Product of Two Sparse Vectors
- **Problem Summary:** Given two sparse vectors, compute their dot product efficiently without iterating over large runs of zeroes.
- **LeetCode Equivalent:** [1570. Dot Product of Two Sparse Vectors](https://leetcode.com/problems/dot-product-of-two-sparse-vectors/)
- **Approach:** Store non-zero elements as pairs of `(index, value)`. Use Two Pointers to compute product where indices match.
- **Complexity:** $O(L_1 + L_2)$ Time where $L_1, L_2$ are counts of non-zero elements.

### 2. Minimum Remove to Make Valid Parentheses
- **Problem Summary:** Given a string $s$ of `'('` , `')'` and lowercase English characters. Remove the minimum number of parentheses in any positions so that the resulting parentheses string is valid.
- **LeetCode Equivalent:** [1249. Minimum Remove to Make Valid Parentheses](https://leetcode.com/problems/minimum-remove-to-make-valid-parentheses/)
- **Approach:** Stack tracking unmatched `'('` indices, plus tracking invalid `')'` indices. Rebuild string skipping flagged indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 3. Subarray Sum Equals K
- **Problem Summary:** Given an array of integers `nums` and an integer `k`, return the total number of subarrays whose sum equals to `k`.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Hash Map storing prefix sum frequencies: `map[prefix_sum - k]`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 4. Vertical Order Traversal of Binary Tree
- **Problem Summary:** Given the root of a binary tree, calculate the vertical order traversal of the binary tree.
- **LeetCode Equivalent:** [987. Vertical Order Traversal of a Binary Tree](https://leetcode.com/problems/vertical-order-traversal-of-a-binary-tree/)
- **Approach:** BFS tracking `(node, row, col)`. Group by `col`, sort by `row`, then value.
- **Complexity:** $O(N \log N)$ Time.
