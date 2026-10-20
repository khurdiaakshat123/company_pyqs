# Rubrik Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🛡️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  - 2 to 4 Algorithmic Coding Questions (Competitive Programming / LeetCode Hard level).
  - (In some on-campus drives) 5 to 10 Technical MCQs covering Operating Systems, Multithreading, Concurrency, and Memory Alignment.
- **Evaluation Criteria:**
  - Rubrik builds cloud data management and zero-trust cybersecurity systems. Their OA is known as one of the most mathematically and algorithmically demanding assessments.
  - Test cases impose strict $10^5$ to $2 \times 10^5$ constraints requiring rigorous $O(N)$ or $O(N \log N)$ approaches with minimal constant factors.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Advanced Bit Manipulation & Ranges | Hard | Bitwise AND/OR/XOR range combinations modulo $10^9+7$, bitmask DP |
| **Very High** | Dynamic Programming on Strings/Trees | Hard | Tree DP, palindrome partitioning, subsequence transitions |
| **High** | Heaps & Custom Greedy Scheduling | Medium - Hard | Priority queues, interval selection under strict constraints |
| **High** | Systems & Concurrency MCQs | Medium - Hard | Deadlock prevention, lock-free queues, paging, virtual memory |
| **Medium** | Graph Component Optimization | Hard | Tarjan's bridges/SCCs, 2-SAT, shortest path with state expansion |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Sum of Bitwise AND Over All Subarrays
- **Problem Summary:** Given an array of integers $A$ of length $N$, find the sum of bitwise AND of all possible contiguous subarrays modulo $10^9 + 7$.
- **Approach:**
  - Standard brute force is $O(N^2)$, which times out on $N = 10^5$.
  - Bitwise contribution technique: For each of the 30 bits, evaluate the number of contiguous subarrays where that bit is 1 (all elements in the subsegment have that bit set). Multiply by $2^{\text{bit}}$ and sum modulo $10^9 + 7$.
- **Complexity:** $O(30 \times N) = O(N)$ Time, $O(1)$ Extra Space.

### 2. File Snapshot Tree Synchronization
- **Problem Summary:** Given a tree representing a nested directory structure where each directory node contains an access permission bitmask. A security policy requires synchronizing access: find the minimum number of edge cuts required such that no component contains conflicting security permissions.
- **Approach:** Tree DP with bitmask propagation or Disjoint Set Union (DSU) checking component validity.
- **Complexity:** $O(N \times 2^K)$ Time where $K \le 5$.

### 3. Trapping Rain Water II (3D Elevation Grid)
- **Problem Summary:** Given an $m \times n$ integer matrix `heightMap` representing the height of each unit cell in a 2D elevation map, return the volume of water it can trap after raining.
- **LeetCode Equivalent:** [407. Trapping Rain Water II](https://leetcode.com/problems/trapping-rain-water-ii/)
- **Approach:** Min-Heap storing boundary cells. Pop the lowest boundary cell, explore its 4 neighbors, update trapped water if neighbor is lower, push neighbor with $\max(\text{neighbor}, \text{current})$ into heap.
- **Complexity:** $O(M \times N \log(M \times N))$ Time.

### 4. Longest Chunked Palindrome Decomposition
- **Problem Summary:** You are given a string `text`. You should split it into $k$ non-empty substrings $(sub_1, sub_2, \dots, sub_k)$ such that $sub_1 == sub_k$, $sub_2 == sub_{k-1}$, etc. Return the largest possible $k$.
- **LeetCode Equivalent:** [1147. Longest Chunked Palindrome Decomposition](https://leetcode.com/problems/longest-chunked-palindrome-decomposition/)
- **Approach:** Greedy matching from outer ends inward using Rolling Hash (Rabin-Karp) or Two Pointers.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.
