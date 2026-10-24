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
- **Dynamic Programming:** State DP, Tree DP, Digit DP, Partition DP, Subarray score maximization, LIS.
- **Graph & Tree Algorithms:** Topological sort on DAGs, Beautiful paths, Tree diameter, Lowest Common Ancestor, Multi-source BFS.
- **Sliding Window & Monotonic Deques:** Absolute difference bounded subarrays, sliding window maximum.
- **Intervals & Sorting:** Merge intervals, rotated sorted array search, meeting rooms.
- **Strings & Backtracking:** Word break, word ladder, decode string, reorganize string.

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

#### 6. Merge Intervals / Task Schedule Consolidation (DSE Track)
- **College/Drive:** Infosys DSE Pan-India 2024
- **Problem Summary:** Merge all overlapping intervals representing automated task execution windows.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time. Merge greedily if current interval overlaps with previous.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 7. Subarray Sum Equals K (DSE Track)
- **College/Drive:** VIT Vellore / SRM 2024
- **Problem Summary:** Find total continuous subarrays whose sum equals $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Running prefix sum with hash map frequency tracking.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 8. Search in Rotated Sorted Array
- **College/Drive:** Manipal Institute of Technology 2024
- **Problem Summary:** Search target element in a sorted rotated array in $O(\log N)$ time.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Modified binary search checking sorted half.
- **Complexity:** $O(\log N)$ Time.

#### 9. Directed Task Scheduling Order (Course Schedule II - SP Track)
- **College/Drive:** HackWithInfy 2024
- **Problem Summary:** Return valid ordering of tasks given prerequisite graph.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm using in-degrees and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 10. Word Ladder / Transformation Sequence (SP Track)
- **College/Drive:** NIT Trichy / Warangal 2024
- **Problem Summary:** Find shortest transformation path between two words using dictionary words.
- **LeetCode Equivalent:** [127. Word Ladder](https://leetcode.com/problems/word-ladder/)
- **Approach:** Bidirectional BFS or BFS with wildcard Hash Map.
- **Complexity:** $O(M^2 \times N)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Coin Change (Fewest Coins)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Minimum coins to make target amount.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 12. Number of Islands (2D Grid BFS)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Count connected components of 1s in binary matrix.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Complexity:** $O(M \times N)$ Time.

#### 13. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Largest sum contiguous subarray.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time.

#### 14. Trapping Rain Water
- **College/Drive:** HackWithInfy 2023
- **Problem Statement:** Elevation histogram water capacity.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time.

#### 15. Longest Increasing Subsequence
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Binary search LIS.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Complexity:** $O(N \log N)$ Time.

#### 16. Infection Propagation in Grid (Rotting Oranges)
- **College/Drive:** Infosys DSE 2023
- **Problem Statement:** Multi-source BFS to calculate minutes required for all items to spoil.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time and Space.

#### 17. Word Break (Dynamic Programming)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Determine if string `s` can be segmented into words from `wordDict`.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Complexity:** $O(N^2)$ Time, $O(N)$ Space.

#### 18. Lowest Common Ancestor of a Binary Tree (SP Track)
- **College/Drive:** HackWithInfy 2023
- **Problem Statement:** Find lowest common ancestor node of two nodes in binary tree.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 19. Reorganize String (Max-Heap)
- **College/Drive:** Infosys SP Off-Campus 2023
- **Problem Statement:** Rearrange characters so that no two identical characters are adjacent.
- **LeetCode Equivalent:** [767. Reorganize String](https://leetcode.com/problems/reorganize-string/)
- **Complexity:** $O(N \log \Sigma)$ Time.

#### 20. Decode String (Dual Stack)
- **College/Drive:** Infosys DSE 2023
- **Problem Statement:** Decode nested string pattern `k[string]`.
- **LeetCode Equivalent:** [394. Decode String](https://leetcode.com/problems/decode-string/)
- **Approach:** Dual stack for multipliers and string builders.
- **Complexity:** $O(\text{Output Length})$ Time.
