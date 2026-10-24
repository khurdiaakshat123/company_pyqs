# Meta (Facebook) Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) ♾️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **CodeSignal** / **HackerRank** / Meta Internal Assessment Portal
- **Test Duration:** 45 to 70 minutes
- **Structure Breakdown:**
  - 2 to 4 Algorithmic Coding Problems (LeetCode Medium to Hard).
  - In technical phone screening / automated OAs, candidates typically have **45 minutes to solve 2 distinct problems completely**.
- **The "Meta Speed Benchmark":**
  - Meta evaluates speed, clarity, and bug-free optimal execution. You are expected to produce clean, optimal code with tight time/space complexity within 15–20 minutes per problem.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Two Pointers & Binary Search:** Dot product of sparse vectors, subarray sums, rotated array searches, palindrome extensions.
- **HashMaps & Prefix Sums:** Subarray sum equals K, continuous subarray sum, accounts merge, custom sort string.
- **Trees & Lowest Common Ancestor:** LCA with parent pointers, vertical order traversal, diameter of binary tree, binary tree right side view, string to binary tree parsing.
- **Monotonic Stack & Heaps:** Minimum remove to make valid parentheses, ocean view buildings, exclusive function time, K closest points to origin.
- **Graph & Matrix Traversals:** Word ladder, number of islands, shortest path in binary matrix, DSU component merging.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Dot Product of Two Sparse Vectors
- **College/Drive:** Meta University / Global Internship & New Grad 2024–2025
- **Problem Summary:** Given two sparse vectors, compute their dot product efficiently without iterating over large runs of zeroes.
- **Constraints:** $N \le 10^5$, non-zero elements $\le 10^4$.
- **LeetCode Equivalent:** [1570. Dot Product of Two Sparse Vectors](https://leetcode.com/problems/dot-product-of-two-sparse-vectors/)
- **Approach:** Store non-zero elements as pairs of `(index, value)`. Use Two Pointers (or binary search on smaller list) to compute products where indices match.
- **Complexity:** $O(L_1 + L_2)$ Time where $L_1, L_2$ are counts of non-zero elements; $O(L_1 + L_2)$ Space.

#### 2. Minimum Remove to Make Valid Parentheses
- **College/Drive:** Meta Rotational Engineer / Campus Drive 2024–2025
- **Problem Summary:** Given a string $s$ of `'('` , `')'` and lowercase English characters. Remove the minimum number of parentheses in any positions so that the resulting parentheses string is valid.
- **Constraints:** $1 \le |s| \le 10^5$.
- **LeetCode Equivalent:** [1249. Minimum Remove to Make Valid Parentheses](https://leetcode.com/problems/minimum-remove-to-make-valid-parentheses/)
- **Approach:** Stack tracking unmatched `'('` indices, plus set tracking invalid `')'` indices. Rebuild string skipping all flagged indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 3. Subarray Sum Equals K
- **College/Drive:** Meta SWE New Grad 2024–2025
- **Problem Summary:** Given an array of integers `nums` and an integer `k`, return the total number of subarrays whose sum equals to `k`.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$, $-1000 \le nums[i] \le 1000$, $-10^7 \le k \le 10^7$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Hash Map storing prefix sum frequencies: `map[prefix_sum - k]`. Update map with current prefix sum count.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 4. Lowest Common Ancestor of a Binary Tree III (With Parent Pointer)
- **College/Drive:** Meta London / US / India Campus 2024–2025
- **Problem Summary:** Given two nodes $p$ and $q$ in a binary tree where each node has a reference to its parent, find their lowest common ancestor.
- **Constraints:** Number of nodes $\le 10^5$.
- **LeetCode Equivalent:** [1650. Lowest Common Ancestor of a Binary Tree III](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree-iii/)
- **Approach:** Two-pointer linked list intersection: pointer $a$ starts at $p$, pointer $b$ starts at $q$. When reaching null/root parent, redirect to the other node's start. They meet at the LCA.
- **Complexity:** $O(H)$ Time, $O(1)$ Space.

#### 5. Valid Word Abbreviation
- **College/Drive:** Meta University Screening 2024–2025
- **Problem Summary:** Given a non-empty string `word` and an abbreviation `abbr`, return whether the string matches the given abbreviation (handling multi-digit counts without leading zeroes).
- **Constraints:** $1 \le |word| \le 20$, $1 \le |abbr| \le 10$.
- **LeetCode Equivalent:** [408. Valid Word Abbreviation](https://leetcode.com/problems/valid-word-abbreviation/)
- **Approach:** Two pointers: iterate through both strings, parse numeric digit runs, verify no leading `'0'`, advance the word pointer by the parsed number.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 6. Continuous Subarray Sum (Multiple of K)
- **College/Drive:** Meta Off-Campus Drive 2024
- **Problem Summary:** Given an integer array `nums` and an integer `k`, return `true` if `nums` has a good subarray of size at least 2 whose sum is a multiple of `k`.
- **Constraints:** $1 \le nums.length \le 10^5$, $0 \le nums[i] \le 10^9$, $1 \le k \le 2^{31} - 1$.
- **LeetCode Equivalent:** [523. Continuous Subarray Sum](https://leetcode.com/problems/continuous-subarray-sum/)
- **Approach:** Prefix sums modulo $k$. Store earliest index where `prefix_sum % k` was observed in a hash map. If remainder repeats at index $j$ where $j - i \ge 2$, return `true`.
- **Complexity:** $O(N)$ Time, $O(\min(N, K))$ Space.

#### 7. Simplify Path (Canonical Unix Path)
- **College/Drive:** Meta Global SWE Slot 2 (2024)
- **Problem Summary:** Given an absolute path for a Unix-style file system, convert it to the simplified canonical path (handle `.` and `..`).
- **Constraints:** $1 \le path.length \le 3000$.
- **LeetCode Equivalent:** [71. Simplify Path](https://leetcode.com/problems/simplify-path/)
- **Approach:** Split path by `/`. Use a stack: push valid directory names, pop on `..`, ignore empty tokens or `.`. Join result with `/`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 8. Accounts Merge (Email Disjoint Set Union)
- **College/Drive:** Meta London & Menlo Park Assessment 2024
- **Problem Summary:** Given a list of accounts where each element is a list of strings starting with a name followed by emails, merge accounts that share common emails.
- **Constraints:** $1 \le accounts.length \le 1000$, total emails $\le 10^4$.
- **LeetCode Equivalent:** [721. Accounts Merge](https://leetcode.com/problems/accounts-merge/)
- **Approach:** Union-Find / DSU mapping each email to an ID and parent. Group emails by connected component root, sort emails, and attach owner name.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space where $N$ is total emails.

#### 9. Exclusive Time of Functions (Call Stack Trace)
- **College/Drive:** Meta Systems / SWE Track 2024
- **Problem Summary:** On a single-threaded CPU, given execution logs of functions (`id:start/end:timestamp`), calculate the total execution time spent exclusively in each function.
- **Constraints:** $1 \le n \le 100$, $1 \le logs.length \le 10^4$.
- **LeetCode Equivalent:** [636. Exclusive Time of Functions](https://leetcode.com/problems/exclusive-time-of-functions/)
- **Approach:** Stack tracking active function IDs. Maintain `prev_time`. On `start`, credit elapsed time to top of stack, then push new ID. On `end`, credit elapsed time $+ 1$ to popped ID, and update `prev_time = timestamp + 1`.
- **Complexity:** $O(L)$ Time, $O(N)$ Space.

#### 10. Nested List Weight Sum
- **College/Drive:** Meta Production Engineering & SWE 2024
- **Problem Summary:** Given a nested list of integers, return the sum of all integers in the list weighted by their depth (depth starts at 1 for root).
- **Constraints:** Maximum nesting depth $\le 50$, total elements $\le 500$.
- **LeetCode Equivalent:** [339. Nested List Weight Sum](https://leetcode.com/problems/nested-list-weight-sum/)
- **Approach:** Recursive DFS or level-by-level BFS passing current depth. Multiply integer values by current depth and recurse for sublists.
- **Complexity:** $O(N)$ Time, $O(D)$ Space where $D$ is max depth.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Random Pick with Weight
- **College/Drive:** Meta Machine Learning / SWE Drive 2023–2024
- **Problem Summary:** Given an array of positive integers `w` where `w[i]` describes the weight of index `i`, write a function `pickIndex` which randomly picks an index in proportion to its weight.
- **Constraints:** $1 \le w.length \le 10^4$, $1 \le w[i] \le 10^5$, up to $10^4$ calls.
- **LeetCode Equivalent:** [528. Random Pick with Weight](https://leetcode.com/problems/random-pick-with-weight/)
- **Approach:** Compute running prefix sums of weights. Generate uniform random integer in $[1, \text{total\_sum}]$. Use Binary Search (`std::lower_bound`) to find the corresponding index.
- **Complexity:** $O(N)$ Init Time, $O(\log N)$ Query Time, $O(N)$ Space.

#### 12. Buildings With an Ocean View
- **College/Drive:** Meta Campus Slot 1 (2023–2024)
- **Problem Summary:** Given an integer array `heights` representing buildings from west to east. A building has an ocean view if all buildings to its right are strictly shorter. Return indices with an ocean view in sorted order.
- **Constraints:** $1 \le heights.length \le 10^5$, $1 \le heights[i] \le 10^9$.
- **LeetCode Equivalent:** [1762. Buildings With an Ocean View](https://leetcode.com/problems/buildings-with-an-ocean-view/)
- **Approach:** Monotonic stack or reverse iteration from right to left tracking `max_so_far`. Append indices where `heights[i] > max_so_far`, then reverse result.
- **Complexity:** $O(N)$ Time, $O(1)$ auxiliary Space.

#### 13. Valid Palindrome III (K-Palindrome)
- **College/Drive:** Meta Advanced SWE 2023
- **Problem Summary:** Given a string $s$ and an integer $k$, return `true` if $s$ is a $k$-palindrome (can become palindrome by deleting at most $k$ characters).
- **Constraints:** $1 \le s.length \le 1000$, $1 \le k \le s.length$.
- **LeetCode Equivalent:** [1216. Valid Palindrome III](https://leetcode.com/problems/valid-palindrome-iii/)
- **Approach:** Find Longest Palindromic Subsequence (LPS) length between $s$ and reverse of $s$ using DP. Return `true` if $N - \text{LPS}(s) \le k$.
- **Complexity:** $O(N^2)$ Time, $O(N)$ Space with DP state optimization.

#### 14. Construct Binary Tree from String with Brackets
- **College/Drive:** Meta Campus Assessment 2023
- **Problem Summary:** Construct a binary tree from a string consisting of integer values and parenthesis pairs, e.g. `"4(2(3)(1))(6(5))"`.
- **Constraints:** $1 \le s.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [536. Construct Binary Tree from String](https://leetcode.com/problems/construct-binary-tree-from-string/)
- **Approach:** Stack-based or recursive parser. Parse integer for root, locate matching parentheses boundaries for left and right children, and recurse.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 15. Custom Sort String
- **College/Drive:** Meta University 2023
- **Problem Summary:** Order string `order` specifies the precedence order of characters. Permute characters of `s` so that they match the order that `order` specifies.
- **Constraints:** $1 \le order.length \le 26$, $1 \le s.length \le 200$.
- **LeetCode Equivalent:** [791. Custom Sort String](https://leetcode.com/problems/custom-sort-string/)
- **Approach:** Frequency bucket count of characters in $s$. Append characters in sequence as defined by `order`, then append remaining unmentioned characters.
- **Complexity:** $O(N + \Sigma)$ Time, $O(\Sigma)$ Space where $\Sigma = 26$.

#### 16. K Closest Points to Origin
- **College/Drive:** Meta Campus Slot 1 (2023)
- **Problem Summary:** Find $K$ points closest to origin $(0, 0)$ on Euclidean plane.
- **Constraints:** $1 \le k \le points.length \le 10^4$, coordinates in $[-10^4, 10^4]$.
- **LeetCode Equivalent:** [973. K Closest Points to Origin](https://leetcode.com/problems/k-closest-points-to-origin/)
- **Approach:** Max-Heap of size $K$ or Quickselect in $O(N)$ average time.
- **Complexity:** $O(N \log K)$ Time with Heap, $O(K)$ Space.

#### 17. Vertical Order Traversal of Binary Tree
- **College/Drive:** Meta Campus Slot 2 (2023)
- **Problem Summary:** Group binary tree nodes by vertical columns, ordered from top to bottom, breaking ties by node values.
- **Constraints:** Number of nodes $\le 1000$.
- **LeetCode Equivalent:** [987. Vertical Order Traversal of a Binary Tree](https://leetcode.com/problems/vertical-order-traversal-of-a-binary-tree/)
- **Approach:** BFS with coordinate tuples `(col, row, val)`. Group by column, sort by row ascending, then by val ascending.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 18. Word Ladder (Shortest Mutation Sequence)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Find shortest transformation sequence length from `beginWord` to `endWord` using word dictionary.
- **Constraints:** $1 \le beginWord.length \le 10$, $1 \le wordList.length \le 5000$.
- **LeetCode Equivalent:** [127. Word Ladder](https://leetcode.com/problems/word-ladder/)
- **Approach:** Bidirectional BFS checking 1-letter substitutions against hash set.
- **Complexity:** $O(M^2 \times N)$ Time where $M$ is word length, $N$ is dictionary size.

#### 19. Range Sum of BST
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Return sum of values of all nodes with a value in the inclusive range $[low, high]$.
- **Constraints:** Number of nodes $\le 2 \times 10^4$.
- **LeetCode Equivalent:** [938. Range Sum of BST](https://leetcode.com/problems/range-sum-of-bst/)
- **Approach:** Pruned DFS leveraging BST properties. If `node.val < low`, explore right only; if `node.val > high`, explore left only.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 20. Binary Tree Maximum Path Sum
- **College/Drive:** Advanced SWE Screening 2023
- **Problem Summary:** Find maximum path sum of any non-empty path in binary tree.
- **Constraints:** Number of nodes $\le 3 \times 10^4$, node values $[-1000, 1000]$.
- **LeetCode Equivalent:** [124. Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/)
- **Approach:** Post-order DFS computing maximum non-negative branch contribution of each subtree `max(0, left) + max(0, right) + node.val`. Update global max at each node.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

---

## 💡 Meta Interview & OA Best Practices
1. **Never jump straight to code:** In technical interviews / interactive screenings, state the brute force, then optimize to optimal time/space before typing.
2. **Handle Edge Cases Early:** Mention empty inputs, single element arrays, negative values, and integer overflows ($2^{31}-1$).
3. **Write Idiomatic Code:** Use standard library containers (`unordered_map`, `std::priority_queue` in C++, or `collections.defaultdict` in Python) without boilerplate overhead.
