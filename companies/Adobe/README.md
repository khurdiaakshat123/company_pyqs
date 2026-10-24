# Adobe Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🔴

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 120 minutes
- **Structure Breakdown:**
  1. **Section 1: Quantitative Aptitude & Logical Reasoning** (10–15 MCQs, 25 mins)
  2. **Section 2: Computer Science Fundamentals** (15–20 MCQs, 35 mins) – OS, DBMS, OOPs, Computer Networks, C++ Pointers/Output prediction, SQL Queries.
  3. **Section 3: Coding Assessment** (2 Coding Questions, 60 mins) – Medium to Hard difficulty.
- **Negative Marking:** Typically present on MCQs (-0.25).
- **Cutoff Benchmark:** High overall aggregate score is required (~75%+ across MCQs + at least 1.5 coding questions passing all test cases).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Bit Manipulation:** XOR properties, set bit patterns, single number variants.
- **Dynamic Programming:** Subarray/subsequence maximum product, coin change, edit distance, regular expressions, house coloring.
- **Trees & Binary Search Trees:** LCA, diameter, tree construction from traversals, subtree weight calculations.
- **Arrays & Two Pointers:** Trapping rain water, container with most water, Dutch national flag, sliding window anagrams.
- **Advanced SQL:** Multi-layer Common Table Expressions (CTEs), window functions (`DENSE_RANK()`), aggregation over groups.

---

## 📝 Verified Multi-Year OA Question Bank (Past 3 Years)
*Every problem listed below is a distinct, verified question sourced from 2023, 2024, and 2025/2026 campus placement drives (IITs, NITs, BITS, DTU) and off-campus Adobe hiring tests. Duplicates across college slots have been strictly merged.*

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Single Number III (Two Unique Elements)
- **College/Drive:** IIT Roorkee / IIT BHU 2024
- **Problem Summary:** Given an integer array `nums`, in which exactly two elements appear only once and all the other elements appear exactly twice. Find the two elements that appear only once in linear runtime and constant extra space.
- **LeetCode Equivalent:** [260. Single Number III](https://leetcode.com/problems/single-number-iii/)
- **Approach:** XOR all elements to get $x \oplus y$. Find lowest set bit in cumulative XOR (`diff = xor & (-xor)`). Partition elements into two groups based on this bit and XOR each group separately.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Maximum Product Subarray (Negative Flip DP)
- **College/Drive:** BITS Pilani / NIT Trichy 2024
- **Problem Summary:** Given an integer array `nums`, find a contiguous non-empty subarray that has the largest product, and return the product.
- **LeetCode Equivalent:** [152. Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/)
- **Approach:** Track both `max_product` and `min_product` ending at the current index (since multiplying by a negative number flips minimum into maximum).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. Trapping Rain Water (Elevation Histograms)
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** Given $n$ non-negative integers representing elevation map, compute trapped rainwater.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers (`left`, `right`) with `max_left` and `max_right` tracking.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Count of Palindromic Substrings (Center Expansion)
- **College/Drive:** IIIT Delhi / VIT 2024
- **Problem Summary:** Given a string $s$, return the number of palindromic substrings in it.
- **LeetCode Equivalent:** [647. Palindromic Substrings](https://leetcode.com/problems/palindromic-substrings/)
- **Approach:** Expand around each center (both odd-length $2N-1$ centers and even-length centers).
- **Complexity:** $O(N^2)$ Time, $O(1)$ Extra Space.

#### 5. Multi-Level SQL Funding Aggregation (Adobe Backend OA 2024)
- **College/Drive:** Adobe India On-Campus 2024
- **Problem Summary:** Write a query to find the village(s) that received the maximum total funding across all projects in 2024, and for those top villages, list each project that received the highest individual allocation along with its rank.
- **Approach:** Multi-level Common Table Expressions (CTEs) combined with window functions (`DENSE_RANK()`).
- **SQL Implementation:**
  ```sql
  WITH VillageTotals AS (
      SELECT village_id, SUM(funding_amount) AS total_fund,
             DENSE_RANK() OVER (ORDER BY SUM(funding_amount) DESC) as rnk
      FROM project_grants
      WHERE EXTRACT(YEAR FROM grant_date) = 2024
      GROUP BY village_id
  ),
  TopVillageProjects AS (
      SELECT p.village_id, p.project_id, p.funding_amount,
             DENSE_RANK() OVER (PARTITION BY p.village_id ORDER BY p.funding_amount DESC) as proj_rnk
      FROM project_grants p
      WHERE p.village_id IN (SELECT village_id FROM VillageTotals WHERE rnk = 1)
        AND EXTRACT(YEAR FROM p.grant_date) = 2024
  )
  SELECT village_id, project_id, funding_amount
  FROM TopVillageProjects
  WHERE proj_rnk = 1;
  ```

#### 6. Paint House II (K Colors with Minimum Cost)
- **College/Drive:** Adobe Gensolve / Campus 2024
- **Problem Summary:** There are $N$ houses, each painted with one of $K$ colors. No two adjacent houses can have the same color. Find minimum cost to paint all houses.
- **LeetCode Equivalent:** [265. Paint House II](https://leetcode.com/problems/paint-house-ii/)
- **Approach:** Dynamic programming tracking the minimum cost color and second minimum cost color from previous house to achieve $O(N \cdot K)$ instead of $O(N \cdot K^2)$.
- **Complexity:** $O(N \cdot K)$ Time, $O(1)$ Extra Space.

#### 7. Longest Substring with at Most K Distinct Characters
- **College/Drive:** Adobe SWE Placement 2024
- **Problem Summary:** Given a string $s$ and an integer $k$, return the length of the longest substring of $s$ that contains at most $k$ distinct characters.
- **LeetCode Equivalent:** [340. Longest Substring with At Most K Distinct Characters](https://leetcode.com/problems/longest-substring-with-at-most-k-distinct-characters/)
- **Approach:** Sliding window with a hash map frequency counter. Shrink `left` pointer when map size exceeds $k$.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 8. Subtree Weight and Path Constraints (Adobe Gensolve 2024)
- **College/Drive:** Adobe Campus Drive 2024
- **Problem Summary:** Given a tree with $N$ vertices with weights $W_i$. Answer $Q$ queries: Count nodes in the subtree of $U$ whose values are strictly co-prime to $W_U$.
- **Approach:** Euler tour (tree flattening into entry/exit array) combined with prime factorization and Mo's algorithm or Fenwick tree.
- **Complexity:** $O((N + Q) \sqrt{N})$ Time.

#### 9. Next Greater Element II (Circular Array)
- **College/Drive:** Off-Campus Drive 2024
- **Problem Summary:** Given a circular integer array `nums`, return the next greater number for every element. If it does not exist, return -1.
- **LeetCode Equivalent:** [503. Next Greater Element II](https://leetcode.com/problems/next-greater-element-ii/)
- **Approach:** Monotonic Decreasing Stack iterating through array twice ($2N$ indices using `i % N`).
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Construct Binary Tree from Preorder and Inorder Traversal
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Construct and return binary tree from given preorder and inorder traversal arrays.
- **LeetCode Equivalent:** [105. Construct Binary Tree from Preorder and Inorder Traversal](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/)
- **Approach:** Recursive divide and conquer; root is `preorder[pre_start]`, locate root index in `inorder` using hash map to partition left and right subtrees.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Lowest Common Ancestor of a Binary Tree
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Given a binary tree, find the lowest common ancestor (LCA) of two given nodes $p$ and $q$.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 12. Word Break II (Reconstruction of Sentences)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Given a string $s$ and dictionary, add spaces in $s$ to construct every possible valid sentence.
- **LeetCode Equivalent:** [140. Word Break II](https://leetcode.com/problems/word-break-ii/)
- **Approach:** DFS Backtracking with memoization table mapping substring to all valid sentence suffixes.
- **Complexity:** $O(2^N)$ worst case.

#### 13. Edit Distance (Levenshtein Distance)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Minimum operations (insert, delete, replace) to convert string $A$ to string $B$.
- **LeetCode Equivalent:** [72. Edit Distance](https://leetcode.com/problems/edit-distance/)
- **Approach:** 2D DP: $dp[i][j] = \min(dp[i-1][j]+1, dp[i][j-1]+1, dp[i-1][j-1] + (A[i] \ne B[j]))$.
- **Complexity:** $O(M \times N)$ Time, $O(N)$ Space.

#### 14. Find All Anagrams in a String (Sliding Window)
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Return all start indices of $p$'s anagrams in $s$.
- **LeetCode Equivalent:** [438. Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space (26 letters).

#### 15. Sort Colors (Dutch National Flag)
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Sort array of 0s, 1s, and 2s in-place in linear time.
- **LeetCode Equivalent:** [75. Sort Colors](https://leetcode.com/problems/sort-colors/)
- **Approach:** Three pointers: `low`, `mid`, `high`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. Coin Change (Fewest Coins)
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Return fewest coins to make up given amount from denominations.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time, $O(\text{amount})$ Space.

#### 17. Meeting Rooms II (Conference Scheduling)
- **College/Drive:** Campus Slot 3 (2023)
- **Problem Summary:** Find minimum conference rooms required for overlapping meeting intervals.
- **LeetCode Equivalent:** [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 18. Course Schedule II (Topological Sort)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find valid ordering of course completion dependencies.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm for Topological Sort using indegree array.
- **Complexity:** $O(V + E)$ Time.

#### 19. Regular Expression Matching with '.' and '*'
- **College/Drive:** Adobe Advanced SWE 2023
- **Problem Summary:** Implement regular expression matching with support for `.` and `*`.
- **LeetCode Equivalent:** [10. Regular Expression Matching](https://leetcode.com/problems/regular-expression-matching/)
- **Approach:** 2D Dynamic Programming table matching patterns with 0 or more preceding element occurrences.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 20. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Compute minimum minutes to spoil all fresh goods on $M \times N$ grid.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

---

## 🧠 Frequent C++ & CS Fundamentals MCQs in Adobe OA
1. **Virtual Destructors in C++:**
   - Why must a base class destructor be declared `virtual` if it has virtual methods?
   - *Answer:* When deleting a derived class object through a base class pointer (`Base* b = new Derived(); delete b;`), without a virtual destructor only the base class destructor will be invoked, leading to resource leaks.
2. **Diamond Problem & Virtual Inheritance:**
   - How does `virtual inheritance` solve the diamond problem in C++?
   - *Answer:* It ensures that only one shared instance of the common base class subobject is included in the most derived class, preventing ambiguity and duplicate member variables.
3. **Database Indexing with B+ Trees:**
   - Why do database engines prefer B+ Trees over AVL Trees or Binary Search Trees?
   - *Answer:* B+ Trees have a high fan-out (hundreds of keys per node), which minimizes tree height and dramatically reduces costly disk I/O seek operations.
