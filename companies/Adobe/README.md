# Adobe Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🔴

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 120 minutes
- **Structure Breakdown:**
  1. **Section 1: Quantitative Aptitude & Logical Reasoning** (10–15 MCQs, 25 mins)
  2. **Section 2: Computer Science Fundamentals** (15–20 MCQs, 35 mins) – OS, DBMS, OOPs, Computer Networks, C++ Pointers/Output prediction.
  3. **Section 3: Coding Assessment** (2 Coding Questions, 60 mins) – Medium to Hard difficulty.
- **Negative Marking:** Typically present on MCQs (-0.25).
- **Cutoff Benchmark:** High overall aggregate score is required (~75%+ across MCQs + at least 1.5 coding questions passing all test cases).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Bit Manipulation:** XOR properties, set bit patterns, single number variants.
- **Dynamic Programming:** Subarray/subsequence maximum product, coin change, edit distance.
- **Trees & Binary Search Trees:** LCA, diameter, tree construction, path sums.
- **Arrays & Two Pointers:** Trapping rain water, container with most water, Dutch national flag.
- **Core CS & OOP Concepts:** Virtual functions, inheritance diamond problem, ACID, paging, semaphores.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

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
- **Approach:** Expand around center for all $2N-1$ possible centers (single-character and two-character centers).
- **Complexity:** $O(N^2)$ Time, $O(1)$ Space.

#### 5. Implement Trie (Prefix Tree with Wildcards)
- **College/Drive:** Adobe SheCodes / Campus 2024
- **Problem Summary:** Design a Trie supporting `insert(word)`, `search(word)`, and `startsWith(prefix)`.
- **LeetCode Equivalent:** [208. Implement Trie (Prefix Tree)](https://leetcode.com/problems/implement-trie-prefix-tree/)
- **Complexity:** $O(L)$ Time per operation, $O(26 \times \text{Total Nodes})$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Longest Increasing Subsequence
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Binary search with patience sorting for LIS.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Complexity:** $O(N \log N)$ Time.

#### 7. Clone Graph / PDF Document Object Model
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Deep copy a connected undirected graph representing document object relationships.
- **LeetCode Equivalent:** [133. Clone Graph](https://leetcode.com/problems/clone-graph/)
- **Approach:** BFS / DFS with a Hash Map mapping `original_node -> cloned_node`.
- **Complexity:** $O(V + E)$ Time.

#### 8. Median of Two Sorted Arrays
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Find median of two sorted arrays in $O(\log(\min(M, N)))$ time.
- **LeetCode Equivalent:** [4. Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)
- **Complexity:** $O(\log(\min(M, N)))$ Time.

#### 9. Container With Most Water
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Two pointers inward maximizing area between vertical lines.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Complexity:** $O(N)$ Time.

#### 10. Single Number II (Elements Appearing Three Times)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Every element appears three times except for one which appears once.
- **LeetCode Equivalent:** [137. Single Number II](https://leetcode.com/problems/single-number-ii/)
- **Approach:** Count bits modulo 3 for all 32 bit positions.
- **Complexity:** $O(32 \times N) = O(N)$ Time.

---

## 🧠 Frequent CS MCQs Asked in Adobe OA
1. **Virtual Destructors in C++:** Why should base class destructors always be declared `virtual`?
   - *Answer:* To ensure that deleting a derived class object through a base class pointer invokes the derived class destructor first, preventing memory leaks.
2. **Deadlock Recovery:** Which of the following is NOT a technique for deadlock recovery? (Process termination, Resource preemption, Rollback, Banker's algorithm - *Banker's is avoidance, not recovery*).
3. **Database Indexing:** What data structure does InnoDB MySQL use for primary indexes? (B+ Tree).
