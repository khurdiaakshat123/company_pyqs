# Meesho Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🛍️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **HackerEarth**
- **Test Duration:** 90 to 110 minutes
- **Structure Breakdown:**
  - **3 Algorithmic Coding Questions** (Ranging from Medium to Hard / Competitive Programming Div. 2 level).
  - 10 to 15 Core Computer Science MCQs (DBMS/SQL, Operating Systems, Computer Networks).
- **Evaluation Criteria:**
  - Meesho is renowned for setting exceptionally demanding Online Assessments with CP-style problems and massive numerical constraints ($K \le 10^{12}$ or $N \le 36$).
  - Solving 2 questions completely with all test cases passed + strong MCQ accuracy is typically necessary for an interview callback.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Meet-in-the-Middle & Bitmask DP:** Subset sum with $N \le 36$, partition problems, knapsack with large weights.
- **Array Optimization with Large K:** Periodic simulation, powers-of-two decomposition, modular arithmetic for $K \le 10^{12}$.
- **Strings & Sliding Window Frequencies:** Character frequency thresholds, anagram substrings, rolling hash.
- **Greedy Array Rearrangement:** Maximizing index-weighted products after element swaps, rearrangement inequality.
- **Graph & Delivery Networks:** Shortest path with fuel tank refills, MST for delivery hubs, topological sorting.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Partition with Meet-in-the-Middle ($N \le 36$)
- **College/Drive:** IIT Roorkee / BITS Pilani 2024
- **Problem Summary:** Given an array of $N$ integers ($N \le 36$) and a target $T$, find the number of subsets whose sum is at most $T$.
- **Approach:** Standard recursion $O(2^{36})$ times out; dynamic programming memory limit exceeded due to large element values ($10^9$).
  - Split array into two halves of size $N/2 \le 18$.
  - Generate and sort all $2^{18}$ subset sums of the second half.
  - For each subset sum in the first half, use `std::upper_bound` to binary search compatible subsets in the second half.
- **Complexity:** $O(2^{N/2} \log(2^{N/2})) = O(N \cdot 2^{N/2})$ Time.

#### 2. Large K Periodic Bitwise Array Simulation ($K \le 10^{12}$)
- **College/Drive:** IIT Kharagpur / DTU 2024
- **Problem Summary:** Given an array of integers $A$. In each step, replace $A[i]$ with $A[i] \oplus A[(i + 1) \% N]$. Determine the array configuration after $K$ steps, where $K$ can be up to $10^{12}$.
- **Approach:** The operation is linear over $GF(2)$. By Lucas' Theorem and properties of binomial coefficients modulo 2, after $2^p$ steps, $A[i] \to A[i] \oplus A[(i + 2^p) \% N]$. Decompose $K$ into powers of 2.
- **Complexity:** $O(N \log K)$ Time.

#### 3. Maximizing Index-Weighted Difference Sum
- **College/Drive:** IIIT Allahabad / NIT Trichy 2024
- **Problem Summary:** Given two arrays $A$ and $B$ of size $N$. You can permute $B$ in any order. Maximize the sum $\sum_{i=1}^N i \cdot (B[i] - A[i])$.
- **Approach:** Rearrangement inequality: To maximize $\sum i \cdot B[i]$, sort array $B$ in strictly ascending order and align larger elements with larger indices $i$.
- **Complexity:** $O(N \log N)$ Time.

#### 4. Substring Frequency Thresholds (Sliding Window)
- **College/Drive:** Meesho Off-Campus Drive 2024
- **Problem Summary:** Return the count of substrings in $S$ where the most frequent character appears at least $K$ times and at most $M$ times.
- **Approach:** Two Pointers / Sliding window iterating over unique characters from 1 to 26.
- **Complexity:** $O(26 \times N)$ Time.

#### 5. Shortest Path in Delivery Network with Fuel Tank Refills
- **College/Drive:** IIT BHU / NSUT 2024
- **Problem Summary:** In a city graph with $N$ hubs, delivery vans have a fuel capacity $C$. Certain nodes have gas stations with fuel price $P_i$ per liter. Find minimum cost to travel from hub $S$ to hub $D$.
- **Approach:** Dijkstra on expanded state `(node, current_fuel)` or Priority Queue state tracking.
- **Complexity:** $O(C \cdot (V + E) \log(C \cdot V))$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Longest Increasing Path in a Matrix
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Find length of longest strictly increasing path in integer matrix.
- **LeetCode Equivalent:** [329. Longest Increasing Path in a Matrix](https://leetcode.com/problems/longest-increasing-path-in-a-matrix/)
- **Approach:** DFS with 2D memoization table.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 7. Minimum Cost to Connect All Fulfillment Centers (MST)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Connect all fulfillment hubs with minimum total road construction cost.
- **LeetCode Equivalent:** [1584. Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)
- **Approach:** Kruskal's algorithm with DSU.
- **Complexity:** $O(E \log E)$ Time.

#### 8. Course Schedule III (Greedy Task Scheduling)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Maximum tasks scheduled before deadlines.
- **LeetCode Equivalent:** [630. Course Schedule III](https://leetcode.com/problems/course-schedule-iii/)
- **Approach:** Sort by deadline; maintain Max-Heap of durations.
- **Complexity:** $O(N \log N)$ Time.

#### 9. Subarray XOR Queries with Maximum Value
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Find maximum XOR sum for subarray queries using Trie.
- **LeetCode Equivalent:** [421. Maximum XOR of Two Numbers in an Array](https://leetcode.com/problems/maximum-xor-of-two-numbers-in-an-array/)
- **Complexity:** $O(32 \cdot N)$ Time.

#### 10. Rotting Oranges / Hub Outbreak Contagion
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Minimum minutes to spread infection across entire fulfillment grid.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

---

## 🧠 Frequent CS Fundamentals MCQs in Meesho OA
1. **Database Indexing & B+ Trees:**
   - Why do database engines store data in B+ Tree leaf nodes rather than interior nodes?
   - *Answer:* Interior nodes can hold more index keys (higher fan-out), leading to shallower trees and fewer disk I/O operations.
2. **CPU Scheduling & Inverted Paging:**
   - What problem does an Inverted Page Table solve in Operating Systems?
   - *Answer:* It dramatically reduces the memory footprint required to store page tables by maintaining only one entry per physical frame instead of one per virtual page per process.
