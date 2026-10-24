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
- **College/Drive:** IIT Roorkee / BITS Pilani 2024–2025
- **Problem Summary:** Given an array of $N$ integers ($N \le 36$) and a target $T$, find the number of subsets whose sum is at most $T$.
- **Constraints:** $1 \le N \le 36$, elements up to $10^9$.
- **Approach:** Standard recursion $O(2^{36})$ times out; dynamic programming memory limit exceeded due to large element values ($10^9$).
  - Split array into two halves of size $N/2 \le 18$.
  - Generate and sort all $2^{18}$ subset sums of the second half.
  - For each subset sum in the first half, use `std::upper_bound` to binary search compatible subsets in the second half.
- **Complexity:** $O(2^{N/2} \log(2^{N/2})) = O(N \cdot 2^{N/2})$ Time.

#### 2. Large K Periodic Bitwise Array Simulation ($K \le 10^{12}$)
- **College/Drive:** IIT Kharagpur / DTU 2024–2025
- **Problem Summary:** Given an array of integers $A$. In each step, replace $A[i]$ with $A[i] \oplus A[(i + 1) \% N]$. Determine the array configuration after $K$ steps, where $K$ can be up to $10^{12}$.
- **Constraints:** $N \le 10^5$, $K \le 10^{12}$.
- **Approach:** The operation is linear over $GF(2)$. By Lucas' Theorem and properties of binomial coefficients modulo 2, after $2^p$ steps, $A[i] \to A[i] \oplus A[(i + 2^p) \% N]$. Decompose $K$ into powers of 2.
- **Complexity:** $O(N \log K)$ Time.

#### 3. Maximizing Index-Weighted Difference Sum
- **College/Drive:** IIIT Allahabad / NIT Trichy 2024–2025
- **Problem Summary:** Given two arrays $A$ and $B$ of size $N$. You can permute $B$ in any order. Maximize the sum $\sum_{i=1}^N i \cdot (B[i] - A[i])$.
- **Constraints:** $1 \le N \le 10^5$.
- **Approach:** Rearrangement inequality: To maximize $\sum i \cdot B[i]$, sort array $B$ in strictly ascending order and align larger elements with larger indices $i$.
- **Complexity:** $O(N \log N)$ Time.

#### 4. Substring Frequency Thresholds (Sliding Window)
- **College/Drive:** Meesho Off-Campus Drive 2024–2025
- **Problem Summary:** Return the count of substrings in $S$ where the most frequent character appears at least $K$ times and at most $M$ times.
- **Constraints:** $1 \le |S| \le 10^5$.
- **Approach:** Two Pointers / Sliding window iterating over unique characters from 1 to 26.
- **Complexity:** $O(26 \times N)$ Time.

#### 5. Shortest Path in Delivery Network with Fuel Tank Refills
- **College/Drive:** IIT BHU / NSUT 2024–2025
- **Problem Summary:** In a city graph with $N$ hubs, delivery vans have a fuel capacity $C$. Certain nodes have gas stations with fuel price $P_i$ per liter. Find minimum cost to travel from hub $S$ to hub $D$.
- **Constraints:** $V \le 1000, C \le 100$.
- **Approach:** Dijkstra on expanded state `(node, current_fuel)` or Priority Queue state tracking.
- **Complexity:** $O(C \cdot (V + E) \log(C \cdot V))$ Time.

#### 6. Longest Increasing Path in a Matrix
- **College/Drive:** Campus Slot 1 (2024)
- **Problem Summary:** Find length of longest strictly increasing path in integer matrix.
- **Constraints:** $1 \le M, N \le 200$.
- **LeetCode Equivalent:** [329. Longest Increasing Path in a Matrix](https://leetcode.com/problems/longest-increasing-path-in-a-matrix/)
- **Approach:** DFS with 2D memoization table.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 7. Minimum Cost to Connect All Fulfillment Centers (MST)
- **College/Drive:** Campus Slot 2 (2024)
- **Problem Summary:** Connect all fulfillment hubs with minimum total road construction cost.
- **Constraints:** $N \le 1000$.
- **LeetCode Equivalent:** [1584. Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)
- **Approach:** Kruskal's algorithm with DSU.
- **Complexity:** $O(E \log E)$ Time.

#### 8. Course Schedule III (Greedy Task Scheduling)
- **College/Drive:** Off-Campus Hiring 2024
- **Problem Summary:** Maximum tasks scheduled before deadlines.
- **Constraints:** $1 \le courses.length \le 10^4$.
- **LeetCode Equivalent:** [630. Course Schedule III](https://leetcode.com/problems/course-schedule-iii/)
- **Approach:** Sort by deadline; maintain Max-Heap of durations.
- **Complexity:** $O(N \log N)$ Time.

#### 9. Subarray XOR Queries with Maximum Value
- **College/Drive:** Campus Hiring 2024
- **Problem Summary:** Find maximum XOR sum for subarray queries using Trie.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [421. Maximum XOR of Two Numbers in an Array](https://leetcode.com/problems/maximum-xor-of-two-numbers-in-an-array/)
- **Approach:** Binary Trie storing 32-bit representations.
- **Complexity:** $O(32 \cdot N)$ Time.

#### 10. Rotting Oranges / Hub Outbreak Contagion
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Minimum minutes to spread infection across entire fulfillment grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Trapping Rain Water
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Subarray Sum Equals K
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Count total continuous subarrays whose sum equals $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency counter.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 13. Daily Temperatures
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Find days to wait for a warmer day.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 14. Coin Change (Fewest Coins)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Minimum coins needed to make change.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 15. Merge Intervals
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Merge all overlapping fulfillment intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time and merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 16. Product of Array Except Self without Division
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 17. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Sliding window with hash map storing last seen indices.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

#### 18. House Robber (1D Dynamic Programming)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Maximize order value without selecting two adjacent fulfillment nodes.
- **Constraints:** $1 \le nums.length \le 100$.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** DP: `dp[i] = max(dp[i-1], dp[i-2] + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 19. Search in Rotated Sorted Array
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Find target in rotated sorted array in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 5000$.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking sorted half.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 20. Container With Most Water
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Two pointers inward maximizing area between vertical lines.
- **Constraints:** $2 \le heights.length \le 10^5$.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent CS Fundamentals MCQs in Meesho OA
1. **Database Indexing & B+ Trees:**
   - Why do database engines store data in B+ Tree leaf nodes rather than interior nodes?
   - *Answer:* Interior nodes can hold more index keys (higher fan-out), leading to shallower trees and fewer disk I/O operations.
2. **CPU Scheduling & Inverted Paging:**
   - What problem does an Inverted Page Table solve in Operating Systems?
   - *Answer:* It dramatically reduces the memory footprint required to store page tables by maintaining only one entry per physical frame instead of one per virtual page per process.
3. **Database Write-Ahead Logging (WAL):**
   - How does Write-Ahead Logging guarantee the Durability of ACID?
   - *Answer:* Changes are appended sequentially to a durable log file on non-volatile disk before the corresponding in-memory buffer pages are written back to main storage tables.
