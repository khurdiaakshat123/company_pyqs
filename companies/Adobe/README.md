# Adobe Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🔴

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

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Bit Manipulation | Medium | XOR properties, set bit patterns, single number variants |
| **Very High** | Dynamic Programming | Medium - Hard | Subarray/subsequence maximum product, coin change, edit distance |
| **High** | Trees & Binary Search Trees | Medium | LCA, diameter, tree construction, path sums |
| **High** | Arrays & Two Pointers | Medium | Trapping rain water, container with most water, Dutch national flag |
| **Medium** | Core CS & OOP Concepts | Medium | Virtual functions, inheritance diamond problem, ACID, paging, semaphores |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Single Number III (Two Unique Elements)
- **Problem Summary:** Given an integer array `nums`, in which exactly two elements appear only once and all the other elements appear exactly twice. Find the two elements that appear only once in linear runtime and constant extra space.
- **LeetCode Equivalent:** [260. Single Number III](https://leetcode.com/problems/single-number-iii/)
- **Approach:** XOR all elements to get $x \oplus y$. Find the lowest set bit in the cumulative XOR (`diff = xor & (-xor)`). Partition elements into two groups based on this bit and XOR each group separately.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 2. Maximum Product Subarray
- **Problem Summary:** Given an integer array `nums`, find a contiguous non-empty subarray that has the largest product, and return the product.
- **LeetCode Equivalent:** [152. Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/)
- **Approach:** Track both `max_product` and `min_product` ending at the current index (since multiplying by a negative number flips minimum into maximum).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 3. Trapping Rain Water Variations
- **Problem Summary:** Given $n$ non-negative integers representing an elevation map where the width of each bar is 1, compute how much water it can trap after raining.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers (`left`, `right`) with `max_left` and `max_right` tracking.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 4. Count of Palindromic Substrings (DP or Center Expansion)
- **Problem Summary:** Given a string $s$, return the number of palindromic substrings in it.
- **LeetCode Equivalent:** [647. Palindromic Substrings](https://leetcode.com/problems/palindromic-substrings/)
- **Approach:** Expand around center for all $2N-1$ possible centers (single-character and two-character centers).
- **Complexity:** $O(N^2)$ Time, $O(1)$ Space.

---

## 🧠 Frequent CS MCQs Asked in Adobe OA
1. **Virtual Destructors in C++:** Why should base class destructors always be declared `virtual`?
   - *Answer:* To ensure that deleting a derived class object through a base class pointer invokes the derived class destructor first, preventing memory leaks.
2. **Deadlock Recovery:** Which of the following is NOT a technique for deadlock recovery? (Process termination, Resource preemption, Rollback, Banker's algorithm - *Banker's is avoidance, not recovery*).
3. **Database Indexing:** What data structure does InnoDB MySQL use for primary indexes? (B+ Tree).
