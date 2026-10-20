# D. E. Shaw Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 📈

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 80 to 120 minutes
- **Structure Breakdown:**
  1. **Section 1: Coding Challenges** (2 to 3 Coding Problems, 60–75 mins) – Rigorous Medium to Hard difficulty problems.
  2. **Section 2: Computer Science Fundamentals** (10 MCQs, 20 mins) – OS, DBMS (transactions, indexing), Computer Networks, Algorithms.
  3. **Section 3: Quantitative Aptitude & Puzzles** (10 MCQs, 20 mins) – Complex combinatorics, probability, algebra, and logic puzzles.
- **Critical Caveat (Sequential Navigation):** Many D. E. Shaw assessments enforce strict sequential navigation—once you submit or move past a section or question, you cannot revisit it.
- **Cutoff Benchmark:** Extremely high (~90%+). Quantitative aptitude and core CS are used as strict gating filters before coding is even evaluated.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Dynamic Programming | Hard | State transitions, partition DP, multi-choice constraints, bounded knapsack |
| **Very High** | Greedy with Custom Comparators | Medium - Hard | Sorting under multi-criteria conditions, interval operations |
| **High** | Graph Algorithms & Dijkstra | Hard | Modified Dijkstra with $K$ hops or vertex penalties, multi-constraint paths |
| **High** | Bit Manipulation & Binary Math | Medium - Hard | Set-bit gaps, binary representation properties, XOR ranges |
| **Medium** | Advanced Data Structures | Hard | Segment Trees, Fenwick Trees, Disjoint Set Union |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Maximum Gap Between Consecutive Set Bits in Array Transformation
- **Problem Summary:** Given an array of integers, transform each integer into its binary representation. Filter numbers having at least $K$ set bits, compute the maximum gap between consecutive set bits for each number, and sort the array based on:
  1. Descending order of maximum set-bit gap.
  2. Ascending order of original numerical value (tie-breaker).
- **Approach:** Bitwise scanning with bitwise shifts `(n >> i) & 1`, custom struct comparator sorting.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

### 2. Minimum Cost Flight Path with at most K Stops (D. E. Shaw Variant)
- **Problem Summary:** There are $n$ cities connected by flights with costs. Find the cheapest price from `src` to `dst` with at most $k$ stops. If flight route edges are subject to dynamic surge pricing based on arrival hour, find the optimal route.
- **LeetCode Equivalent:** [787. Cheapest Flights Within K Stops](https://leetcode.com/problems/cheapest-flights-within-k-stops/)
- **Approach:** Modified Dijkstra's Algorithm or Bellman-Ford algorithm relaxing edges at most $K+1$ times.
- **Complexity:** $O(K \times E)$ Time, $O(V)$ Space.

### 3. Array Partition to Maximize Minimum Segment Score
- **Problem Summary:** Divide an array of size $N$ into $M$ non-empty contiguous segments such that the minimum score across all segments is maximized.
- **Approach:** Binary Search on the target minimum score combined with a Greedy verification function.
- **Complexity:** $O(N \log(\text{Range}))$.

### 4. Partition Array Into Two Arrays to Minimize Sum Difference
- **Problem Summary:** You are given an integer array `nums` of $2n$ integers. You need to partition `nums` into two arrays of length $n$ to minimize the absolute difference of the sums of the arrays.
- **LeetCode Equivalent:** [2035. Partition Array Into Two Arrays to Minimize Sum Difference](https://leetcode.com/problems/partition-array-into-two-arrays-to-minimize-sum-difference/)
- **Approach:** Meet-in-the-middle technique: Generate all subset sums for first half grouped by size, binary search corresponding complement in second half.
- **Complexity:** $O(2^N \times N)$ where $N \le 15$.

---

## 🧠 Frequent CS Fundamentals MCQs in D. E. Shaw OA
1. **Transaction Isolation & Phantom Reads:** Which SQL isolation level prevents phantom reads? (`SERIALIZABLE`; MySQL InnoDB also mitigates this in `REPEATABLE READ` via Next-Key locks).
2. **Page Table Size Calculation:** Calculate the size of a single-level page table for a 32-bit virtual address space with 4 KB page size and 4-byte page table entries.
   - *Calculation:* $\text{Number of pages} = \frac{2^{32}}{2^{12}} = 2^{20}$. Page table size = $2^{20} \times 4 \text{ bytes} = 4 \text{ MB}$.
3. **Database B-Tree Order:** What is the maximum number of keys in a B-Tree node of order $M$? ($M - 1$ keys).
