# Infosys Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏢

## 📌 OA Overview & Test Logistics
Infosys conducts recruitment through tiered tracks via **HackerEarth** (for SP & DSE roles) and **Infosys Internal Assessment Portal**:
1. **Specialist Programmer (SP - 9.5 LPA) & Digital Specialist Engineer (DSE - 6.25 LPA):**
   - **Platform:** **HackerEarth**
   - **Duration:** 180 minutes (3 hours)
   - **Format:** 3 Coding Questions (No MCQs, No Aptitude)
     - Question 1: Easy-Medium (DSE benchmark)
     - Question 2: Medium-Hard (DSE/SP benchmark)
     - Question 3: Hard (SP benchmark - Advanced DP, Trees/Graphs)
2. **Systems Engineer (SE - 3.6 LPA):**
   - **Duration:** 100 minutes (54 Questions)
   - **Sections:** Mathematical Ability (10 Q), Logical Reasoning (15 Q), Verbal Ability (20 Q), Pseudocode (5 Q), Numerical Puzzles (4 Q).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Dynamic Programming:** State DP, Tree DP, Digit DP, Partition DP, Subarray score maximization.
- **Graph & Tree Algorithms:** Shortest path, Cycle detection, Tree diameter, Rerooting, Multi-source BFS.
- **Number Theory & Combinatorics:** Modular arithmetic, Prime factorization (Sieve of Eratosthenes), GCD.
- **Greedy & Disjoint Sets (DSU):** Component connectivity, Kruskal's MST, Interval compression.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Beautiful Path in Weighted Directed Graph (SP Track)
- **College/Drive:** Infosys SP National Drive 2024
- **Problem Summary:** Given a directed graph with $N$ vertices and $M$ edges, where each vertex has an English letter. A path is called "beautiful" if the frequency of the most frequent letter on that path is maximized. Return this maximum frequency, or $-1$ if the graph contains a cycle reachable along a path.
- **Approach:** Topological Sort (Kahn's Algorithm) combined with DP: `dp[u][char]` stores the maximum frequency of `char` on any path ending at node `u`. If topological sort cannot process all reachable nodes, a cycle exists.
- **Complexity:** $O(26 \times (V + E))$ Time, $O(26 \times V)$ Space.

#### 2. Minimum Operations to Equalize Subarrays (DSE Track)
- **College/Drive:** Infosys DSE On-Campus 2024
- **Problem Summary:** Given an array $A$ of size $N$, partition it into $K$ contiguous subarrays. In each operation, you can increment or decrement any element by 1. Find the minimum operations to make all elements within each subarray equal to the median of that subarray.
- **Approach:** Prefix sums on sorted subarrays or quickselect / median calculation with prefix array.
- **Complexity:** $O(N \log N)$ Time.

#### 3. Maximum Subsequence Value under Parity Constraints (SP Track)
- **College/Drive:** National Level HackWithInfy 2024
- **Problem Summary:** Select a subsequence from an array such that no two adjacent chosen elements have the same parity (alternating odd/even) and the sum is maximized.
- **Approach:** 1D DP maintaining two running maximums: `dp_even` (ending with an even number) and `dp_odd` (ending with an odd number).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Tree Node Deletion to Minimize Components (SP Track)
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Given a tree with $N$ nodes, delete at most $K$ edges such that each resulting connected component has an even sum of node values.
- **Approach:** Post-order DFS. Calculate subtree sums from the leaves upward; whenever a subtree sum is even, greedily cut that edge.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 5. Longest Subarray with Absolute Difference at Most K (DSE Track)
- **College/Drive:** Pool Campus Drive 2024
- **Problem Summary:** Given an array of integers `nums` and an integer `limit`, return the size of the longest non-empty subarray such that the absolute difference between any two elements of this subarray is less than or equal to `limit`.
- **LeetCode Equivalent:** [1438. Longest Continuous Subarray With Absolute Diff Less Than or Equal to Limit](https://leetcode.com/problems/longest-continuous-subarray-with-absolute-diff-less-than-or-equal-to-limit/)
- **Approach:** Two Pointers / Sliding window with two Monotonic Deques (one min-deque and one max-deque).
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Coin Change (Fewest Coins)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Minimum coins to make target amount.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 7. Number of Islands (2D Grid BFS)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Count connected components of 1s in binary matrix.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Complexity:** $O(M \times N)$ Time.

#### 8. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Largest sum contiguous subarray.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time.

#### 9. Trapping Rain Water
- **College/Drive:** HackWithInfy 2023
- **Problem Statement:** Elevation histogram water capacity.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time.

#### 10. Longest Increasing Subsequence
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Binary search LIS.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Complexity:** $O(N \log N)$ Time.
