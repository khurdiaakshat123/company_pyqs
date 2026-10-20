# D. E. Shaw Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 📈

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

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Dynamic Programming:** State transitions, partition DP, multi-choice constraints, bounded knapsack.
- **Greedy with Custom Comparators:** Sorting under multi-criteria conditions, interval operations.
- **Graph Algorithms & Dijkstra:** Modified Dijkstra with $K$ hops or vertex penalties, multi-constraint paths.
- **Bit Manipulation & Binary Math:** Set-bit gaps, binary representation properties, XOR ranges.
- **Advanced Data Structures:** Segment Trees, Fenwick Trees, Disjoint Set Union.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Maximum Gap Between Consecutive Set Bits (D. E. Shaw Classic)
- **College/Drive:** IIT Bombay / IIT Delhi 2024
- **Problem Summary:** Given an array of integers, transform each integer into its binary representation. Filter numbers having at least $K$ set bits, compute the maximum gap between consecutive set bits for each number, and sort the array based on:
  1. Descending order of maximum set-bit gap.
  2. Ascending order of original numerical value (tie-breaker).
- **Approach:** Bitwise scanning with bitwise shifts `(n >> i) & 1`, custom struct comparator sorting.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 2. Cheapest Flights with Dynamic Hourly Surge (Modified Dijkstra)
- **College/Drive:** BITS Pilani / IIT Roorkee 2024
- **Problem Summary:** There are $n$ cities connected by flights with costs. Find the cheapest price from `src` to `dst` with at most $k$ stops. If flight route edges are subject to dynamic surge pricing based on arrival hour, find the optimal route.
- **LeetCode Equivalent:** [787. Cheapest Flights Within K Stops](https://leetcode.com/problems/cheapest-flights-within-k-stops/)
- **Approach:** Modified Dijkstra's Algorithm or Bellman-Ford algorithm relaxing edges at most $K+1$ times.
- **Complexity:** $O(K \times E)$ Time, $O(V)$ Space.

#### 3. Array Partition into Two Arrays to Minimize Sum Difference
- **College/Drive:** IIT Kanpur / IIIT Hyderabad 2024
- **Problem Summary:** You are given an integer array `nums` of $2n$ integers ($2n \le 30$). You need to partition `nums` into two arrays of length $n$ to minimize the absolute difference of the sums of the arrays.
- **LeetCode Equivalent:** [2035. Partition Array Into Two Arrays to Minimize Sum Difference](https://leetcode.com/problems/partition-array-into-two-arrays-to-minimize-sum-difference/)
- **Approach:** Meet-in-the-middle technique: Generate all subset sums for first half grouped by size, binary search corresponding complement in second half.
- **Complexity:** $O(2^N \times N)$ where $N \le 15$.

#### 4. Array Partition to Maximize Minimum Segment Score
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** Divide an array of size $N$ into $M$ non-empty contiguous segments such that the minimum score across all segments is maximized.
- **Approach:** Binary Search on the target minimum score combined with a Greedy verification function.
- **Complexity:** $O(N \log(\text{Range}))$.

#### 5. Shortest Path with Fuel Capacity Constraint
- **College/Drive:** D. E. Shaw SMT Drive 2024
- **Problem Summary:** Given a weighted graph where each node has a fuel station selling fuel at price $P_i$. A car with fuel tank capacity $C$ travels from node 0 to $N-1$. Find minimum cost to reach destination.
- **Approach:** Dijkstra's Algorithm on expanded state graph `(node, fuel_level)`.
- **Complexity:** $O(C \times (V + E) \log(V \times C))$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Word Break II (All Possible Sentences)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Segment string into all valid dictionary word sequences.
- **LeetCode Equivalent:** [140. Word Break II](https://leetcode.com/problems/word-break-ii/)
- **Complexity:** Exponential worst-case, memoized DFS.

#### 7. Maximum Profit in Job Scheduling
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Maximum profit non-overlapping weighted jobs.
- **LeetCode Equivalent:** [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)
- **Complexity:** $O(N \log N)$ Time.

#### 8. Trapping Rain Water (Two Pointers)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Elevation histogram water capacity.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time.

#### 9. Course Schedule (Cycle Detection)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Cycle detection in directed graph of module prerequisites.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Complexity:** $O(V + E)$ Time.

#### 10. Longest Increasing Subsequence
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Binary search LIS.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Complexity:** $O(N \log N)$ Time.
