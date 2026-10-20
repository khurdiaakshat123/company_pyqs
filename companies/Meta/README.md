# Meta (Facebook) Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) ♾️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **CodeSignal** / **HackerRank** / Meta Internal Assessment Portal
- **Test Duration:** 45 to 70 minutes
- **Structure Breakdown:**
  - 2 to 4 Algorithmic Coding Problems (LeetCode Medium to Hard).
  - In technical phone screening / automated OAs, candidates typically have **45 minutes to solve 2 distinct problems completely**.
- **The "Meta Speed Benchmark":**
  - Meta evaluates speed and immediate optimal execution. You are expected to produce clean, bug-free code with optimal time/space complexity within 15–20 minutes per problem.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Two Pointers & Binary Search:** Dot product of sparse vectors, subarray sums, rotated array searches, palindrome extensions.
- **HashMaps & Frequency Counters:** Subarray sum equals K, group anagrams, continuous subarray sum.
- **Trees & Lowest Common Ancestor:** LCA with parent pointers, vertical order traversal, diameter of binary tree, binary tree right side view.
- **Monotonic Stack & Heaps:** Minimum remove to make valid parentheses, next greater element, K closest points to origin.
- **Graph & Matrix Traversals:** Word ladder, number of islands, shortest path in binary matrix.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Dot Product of Two Sparse Vectors
- **College/Drive:** Meta University / Global Internship & New Grad 2024
- **Problem Summary:** Given two sparse vectors, compute their dot product efficiently without iterating over large runs of zeroes.
- **LeetCode Equivalent:** [1570. Dot Product of Two Sparse Vectors](https://leetcode.com/problems/dot-product-of-two-sparse-vectors/)
- **Approach:** Store non-zero elements as pairs of `(index, value)`. Use Two Pointers to compute product where indices match.
- **Complexity:** $O(L_1 + L_2)$ Time where $L_1, L_2$ are counts of non-zero elements.

#### 2. Minimum Remove to Make Valid Parentheses
- **College/Drive:** Meta Rotational Engineer / Campus Drive 2024
- **Problem Summary:** Given a string $s$ of `'('` , `')'` and lowercase English characters. Remove the minimum number of parentheses in any positions so that the resulting parentheses string is valid.
- **LeetCode Equivalent:** [1249. Minimum Remove to Make Valid Parentheses](https://leetcode.com/problems/minimum-remove-to-make-valid-parentheses/)
- **Approach:** Stack tracking unmatched `'('` indices, plus tracking invalid `')'` indices. Rebuild string skipping flagged indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 3. Subarray Sum Equals K
- **College/Drive:** Meta SWE New Grad 2024
- **Problem Summary:** Given an array of integers `nums` and an integer `k`, return the total number of subarrays whose sum equals to `k`.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Hash Map storing prefix sum frequencies: `map[prefix_sum - k]`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 4. Lowest Common Ancestor of a Binary Tree III (With Parent Pointer)
- **College/Drive:** Meta London / US / India Campus 2024
- **Problem Summary:** Given two nodes $p$ and $q$ in a binary tree where each node has a reference to its parent, find their lowest common ancestor.
- **LeetCode Equivalent:** [1650. Lowest Common Ancestor of a Binary Tree III](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree-iii/)
- **Approach:** Two-pointer linked list cycle detection technique: pointer $a$ starts at $p$, pointer $b$ starts at $q$. When reaching root/null, redirect to the other node's start. They meet at the LCA.
- **Complexity:** $O(H)$ Time, $O(1)$ Space.

#### 5. Valid Word Abbreviation
- **College/Drive:** Meta University Screening 2024
- **Problem Summary:** Given a non-empty string `word` and an abbreviation `abbr`, return whether the string matches the given abbreviation (handling multi-digit counts without leading zeroes).
- **LeetCode Equivalent:** [408. Valid Word Abbreviation](https://leetcode.com/problems/valid-word-abbreviation/)
- **Approach:** Two pointers: iterate through both strings, parse numeric digit runs, verify no leading `'0'`, advance the word pointer by the parsed number.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. K Closest Points to Origin
- **College/Drive:** Meta Campus Slot 1 (2023)
- **Problem Summary:** Find $K$ points closest to origin $(0, 0)$ on Euclidean plane.
- **LeetCode Equivalent:** [973. K Closest Points to Origin](https://leetcode.com/problems/k-closest-points-to-origin/)
- **Approach:** Max-Heap of size $K$ or Quickselect in $O(N)$ average time.
- **Complexity:** $O(N \log K)$ Time with Heap, $O(K)$ Space.

#### 7. Vertical Order Traversal of Binary Tree
- **College/Drive:** Meta Campus Slot 2 (2023)
- **Problem Summary:** Group binary tree nodes by vertical columns, ordered from top to bottom, breaking ties by node values.
- **LeetCode Equivalent:** [987. Vertical Order Traversal of a Binary Tree](https://leetcode.com/problems/vertical-order-traversal-of-a-binary-tree/)
- **Complexity:** $O(N \log N)$ Time.

#### 8. Word Ladder (Shortest Mutation Sequence)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Find shortest transformation sequence length from `beginWord` to `endWord` using word dictionary.
- **LeetCode Equivalent:** [127. Word Ladder](https://leetcode.com/problems/word-ladder/)
- **Approach:** Bidirectional BFS checking 1-letter substitutions against hash set.
- **Complexity:** $O(M^2 \times N)$ Time where $M$ is word length, $N$ is dictionary size.

#### 9. Range Sum of BST
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Return sum of values of all nodes with a value in the inclusive range $[low, high]$.
- **LeetCode Equivalent:** [938. Range Sum of BST](https://leetcode.com/problems/range-sum-of-bst/)
- **Approach:** Pruned DFS leveraging BST properties.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 10. Binary Tree Maximum Path Sum
- **College/Drive:** Advanced SWE Screening 2023
- **Problem Summary:** Find maximum path sum of any non-empty path in binary tree.
- **LeetCode Equivalent:** [124. Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/)
- **Approach:** Post-order DFS computing maximum contribution of each subtree.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

---

## 💡 Meta Interview & OA Best Practices
1. **Never jump straight to code:** In technical interviews / interactive screenings, state the brute force, then optimize to optimal time/space before typing.
2. **Handle Edge Cases Early:** Mention empty inputs, single element arrays, negative values, and integer overflows ($2^{31}-1$).
3. **Write Idiomatic Code:** Use standard library containers (`unordered_map`, `std::priority_queue` in C++, or `collections.defaultdict` in Python) without boilerplate overhead.
