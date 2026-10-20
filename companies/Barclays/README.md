# Barclays Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🏦

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerEarth**
- **Test Duration:** 90 to 105 minutes
- **Structure Breakdown:**
  1. **Technical MCQs Section:** 20 to 25 MCQs (30 mins) covering Core Java (Collections, Concurrency, Garbage Collection), DBMS/SQL, Operating Systems, and Quantitative Aptitude.
  2. **Coding Section:** 2 Coding Questions (Medium difficulty, 60–75 mins).
- **Passing Cutoff:** Full score on at least 1 coding question + major test cases on the 2nd, combined with strong performance on Java/DBMS MCQs.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Java Fundamentals & OOP MCQs | Medium | `ConcurrentHashMap`, Thread lifecycle, String immutability, Generics, Stream API |
| **Very High** | Dynamic Programming | Medium | Knapsack variants, longest increasing subsequence, coin change |
| **High** | Arrays & Two Pointers | Medium | Trapping rain water, container with most water, subarray target sums |
| **High** | SQL Queries & Normalization | Medium | Joins, `GROUP BY`, indexing, ACID properties |
| **Medium** | Graph & Tree Algorithms | Medium | Shortest path, cycle detection, lowest common ancestor |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Maximum Sum of Non-Adjacent Elements (House Robber)
- **Problem Summary:** You are a professional robber planning to rob houses along a street. Each house has a certain amount of money stashed, the only constraint stopping you from robbing each of them is that adjacent houses have security systems connected. Return the maximum amount of money you can rob tonight without alerting the police.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** Space-optimized DP: `dp = max(prev1, prev2 + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 2. Container With Most Water
- **Problem Summary:** You are given an integer array `height` of length $n$. There are $n$ vertical lines drawn such that the two endpoints of the $i$-th line are $(i, 0)$ and $(i, height[i])$. Find two lines that together with the x-axis form a container, such that the container contains the most water.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Approach:** Two pointers (`left = 0`, `right = n-1`). Shrink the pointer pointing to the smaller height.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 3. Number of Connected Components in Undirected Graph
- **Problem Summary:** You have a graph of $n$ nodes. You are given an integer $n$ and an array `edges` where `edges[i] = [a_i, b_i]` indicates that there is an edge between $a_i$ and $b_i$ in the graph. Return the number of connected components.
- **LeetCode Equivalent:** [323. Number of Connected Components in an Undirected Graph](https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/)
- **Approach:** Disjoint Set Union (DSU with path compression) or DFS.
- **Complexity:** $O(V + E)$ Time.

---

## 🧠 Frequent Java MCQs Asked in Barclays OA
1. **HashMap vs ConcurrentHashMap:** How does `ConcurrentHashMap` achieve thread safety without synchronizing the whole map?
   - *Answer:* Through segment-level locking (Java 7) and fine-grained CAS (Compare-And-Swap) plus `synchronized` blocks on the bucket head node (Java 8+).
2. **Volatile in Java:** Does `volatile` guarantee atomicity of compound operations like `count++`?
   - *Answer:* No, `volatile` only guarantees visibility and ordering (prevents instruction reordering), but not atomicity (use `AtomicInteger`).
