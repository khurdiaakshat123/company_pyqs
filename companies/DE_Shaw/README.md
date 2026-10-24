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
- **Dynamic Programming:** State transitions, partition DP, multi-choice constraints, bounded knapsack, edit distance.
- **Greedy with Custom Comparators:** Sorting under multi-criteria conditions, interval operations.
- **Graph Algorithms & Dijkstra:** Modified Dijkstra with $K$ hops or fuel state, multi-constraint paths.
- **Bit Manipulation & Binary Math:** Set-bit gaps, binary representation properties, XOR ranges.
- **Advanced Data Structures:** Segment Trees, Fenwick Trees, Disjoint Set Union, Monotonic Stacks with prefix-of-prefix sums.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Maximum Gap Between Consecutive Set Bits (D. E. Shaw Classic)
- **College/Drive:** IIT Bombay / IIT Delhi 2024–2025
- **Problem Summary:** Given an array of integers, transform each integer into its binary representation. Filter numbers having at least $K$ set bits, compute the maximum gap between consecutive set bits for each number, and sort the array based on:
  1. Descending order of maximum set-bit gap.
  2. Ascending order of original numerical value (tie-breaker).
- **Constraints:** $1 \le N \le 10^5$, $1 \le A[i] \le 10^9$.
- **Approach:** Bitwise scanning with bitwise shifts `(n >> i) & 1`, custom struct comparator sorting.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 2. Cheapest Flights with Dynamic Hourly Surge (Modified Dijkstra)
- **College/Drive:** BITS Pilani / IIT Roorkee 2024–2025
- **Problem Summary:** There are $n$ cities connected by flights with costs. Find the cheapest price from `src` to `dst` with at most $k$ stops. If flight route edges are subject to dynamic surge pricing based on arrival hour, find the optimal route.
- **Constraints:** $1 \le n \le 100$, $0 \le k \le n$.
- **LeetCode Equivalent:** [787. Cheapest Flights Within K Stops](https://leetcode.com/problems/cheapest-flights-within-k-stops/)
- **Approach:** Modified Dijkstra's Algorithm or Bellman-Ford algorithm relaxing edges at most $K+1$ times.
- **Complexity:** $O(K \times E)$ Time, $O(V)$ Space.

#### 3. Array Partition into Two Arrays to Minimize Sum Difference
- **College/Drive:** IIT Kanpur / IIIT Hyderabad 2024–2025
- **Problem Summary:** You are given an integer array `nums` of $2n$ integers ($2n \le 30$). You need to partition `nums` into two arrays of length $n$ to minimize the absolute difference of the sums of the arrays.
- **Constraints:** $1 \le n \le 15$ (array size up to 30), $-10^7 \le nums[i] \le 10^7$.
- **LeetCode Equivalent:** [2035. Partition Array Into Two Arrays to Minimize Sum Difference](https://leetcode.com/problems/partition-array-into-two-arrays-to-minimize-sum-difference/)
- **Approach:** Meet-in-the-middle technique: Generate all subset sums for first half grouped by subset size $k$, sort each group, and binary search corresponding complement in second half of size $n - k$.
- **Complexity:** $O(2^N \times N)$ where $N \le 15$.

#### 4. Array Partition to Maximize Minimum Segment Score
- **College/Drive:** DTU / NSUT 2024–2025
- **Problem Summary:** Divide an array of size $N$ into $M$ non-empty contiguous segments such that the minimum score across all segments is maximized.
- **Constraints:** $1 \le M \le N \le 10^5$.
- **Approach:** Binary Search on the target minimum score combined with a Greedy verification function.
- **Complexity:** $O(N \log(\text{Range}))$.

#### 5. Shortest Path with Fuel Capacity Constraint
- **College/Drive:** D. E. Shaw SMT Drive 2024–2025
- **Problem Summary:** Given a weighted graph where each node has a fuel station selling fuel at price $P_i$. A car with fuel tank capacity $C$ travels from node 0 to $N-1$. Find minimum cost to reach destination.
- **Constraints:** $V \le 1000, C \le 100$.
- **Approach:** Dijkstra's Algorithm on expanded state graph `(node, fuel_level)`.
- **Complexity:** $O(C \times (V + E) \log(V \times C))$ Time.

#### 6. Count Subarrays with Fixed Bounds
- **College/Drive:** IIT BHU / IIT Kharagpur 2024
- **Problem Summary:** Given an integer array `nums` and two integers `minK` and `maxK`, return the number of subarrays where the minimum value equals `minK` and maximum value equals `maxK`.
- **Constraints:** $2 \le nums.length \le 10^5$, $1 \le nums[i], minK, maxK \le 10^6$.
- **LeetCode Equivalent:** [2444. Count Subarrays With Fixed Bounds](https://leetcode.com/problems/count-subarrays-with-fixed-bounds/)
- **Approach:** Three pointers tracking: `last_bad_idx` (element outside $[minK, maxK]$), `last_min_idx`, and `last_max_idx`. At index $i$, valid subarrays ending here is $\max(0, \min(last\_min, last\_max) - last\_bad)$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Minimum Difficulty of a Job Schedule
- **College/Drive:** D. E. Shaw Campus Slot 2024
- **Problem Summary:** You want to schedule a list of jobs in $d$ days. Each day, you must finish at least one job. The difficulty of a day is the maximum difficulty of a job done that day. Return the minimum difficulty of a job schedule.
- **Constraints:** $1 \le jobDifficulty.length \le 300$, $1 \le d \le 10$.
- **LeetCode Equivalent:** [1335. Minimum Difficulty of a Job Schedule](https://leetcode.com/problems/minimum-difficulty-of-a-job-schedule/)
- **Approach:** 2D Dynamic Programming: `dp[day][i] = min_{k} (dp[day-1][k] + max(jobDifficulty[k...i]))`. Can be optimized with monotonic stack.
- **Complexity:** $O(D \cdot N^2)$ or $O(D \cdot N)$ Time, $O(D \cdot N)$ Space.

#### 8. Longest Path With Different Adjacent Characters
- **College/Drive:** IIT Madras 2024
- **Problem Summary:** You are given a tree rooted at node 0 with $n$ nodes and a string $s$ where $s[i]$ is the character assigned to node $i$. Find the length of the longest path in the tree such that no pair of adjacent nodes on the path have the same character.
- **Constraints:** $1 \le n \le 10^5$.
- **LeetCode Equivalent:** [2246. Longest Path With Different Adjacent Characters](https://leetcode.com/problems/longest-path-with-different-adjacent-characters/)
- **Approach:** Post-order DFS. At each node, collect top two longest non-matching branch paths from child subtrees. Update global max with `top1 + top2 + 1` and return `top1 + 1`.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 9. Sum of Total Strength of Wizards
- **College/Drive:** D. E. Shaw Advanced Algo Slot 2024
- **Problem Summary:** The strength of a group of wizards is defined as the minimum strength of any wizard multiplied by the sum of strengths of all wizards in the group. Find the sum of total strength of all contiguous groups of wizards modulo $10^9 + 7$.
- **Constraints:** $1 \le strength.length \le 10^5$.
- **LeetCode Equivalent:** [2281. Sum of Total Strength of Wizards](https://leetcode.com/problems/sum-of-total-strength-of-wizards/)
- **Approach:** Monotonic Stack to find left and right boundaries where `strength[i]` is strictly minimum. Use Prefix Sums of Prefix Sums to compute the sum of all subarrays containing `strength[i]` in $O(1)$ time.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Minimum Cost to Make Array Equal
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** Given two arrays `nums` and `cost`. You can increase or decrease `nums[i]` by 1 at cost `cost[i]`. Find the minimum cost to make all elements in `nums` equal.
- **Constraints:** $1 \le n \le 10^5$.
- **LeetCode Equivalent:** [2448. Minimum Cost to Make Array Equal](https://leetcode.com/problems/minimum-cost-to-make-array-equal/)
- **Approach:** Weighted Median concept or Convex function ternary search / binary search. The optimal target value is the weighted median of the pairs `(nums[i], cost[i])`.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Word Break II (All Possible Sentences)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Segment string into all valid dictionary word sequences.
- **Constraints:** $1 \le s.length \le 20$.
- **LeetCode Equivalent:** [140. Word Break II](https://leetcode.com/problems/word-break-ii/)
- **Approach:** Memoized DFS + Trie dictionary pruning.
- **Complexity:** $O(2^N)$ worst case, heavily memoized.

#### 12. Maximum Profit in Job Scheduling
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Maximum profit non-overlapping weighted jobs.
- **Constraints:** $1 \le N \le 5 \times 10^4$.
- **LeetCode Equivalent:** [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)
- **Approach:** Sort by end time; DP with binary search (`upper_bound`).
- **Complexity:** $O(N \log N)$ Time.

#### 13. Trapping Rain Water (Two Pointers)
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Compute elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 14. Course Schedule (Cycle Detection)
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Cycle detection in directed graph of module prerequisites.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Kahn's Algorithm / BFS indegree count.
- **Complexity:** $O(V + E)$ Time.

#### 15. Longest Increasing Subsequence
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find length of longest strictly increasing subsequence.
- **Constraints:** $1 \le nums.length \le 2500$.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Approach:** Patience sorting with `std::lower_bound`.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 16. Rotting Oranges (Multi-Source BFS)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Minimum time until all oranges rot in 2D grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS starting with all initially rotten cells.
- **Complexity:** $O(M \cdot N)$ Time and Space.

#### 17. Subarray Product Less Than K
- **College/Drive:** Off-Campus Slot 2023
- **Problem Summary:** Number of contiguous subarrays where product is strictly less than $K$.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [713. Subarray Product Less Than K](https://leetcode.com/problems/subarray-product-less-than-k/)
- **Approach:** Two-pointer sliding window adding `(right - left + 1)`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 18. Edit Distance (Levenshtein Distance)
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Minimum operations (insert, delete, replace) to convert `word1` to `word2`.
- **Constraints:** $0 \le |word1|, |word2| \le 500$.
- **LeetCode Equivalent:** [72. Edit Distance](https://leetcode.com/problems/edit-distance/)
- **Approach:** 2D Dynamic Programming table: `dp[i][j] = min(dp[i-1][j], dp[i][j-1], dp[i-1][j-1]) + 1` if characters differ.
- **Complexity:** $O(M \cdot N)$ Time, $O(N)$ Space.

#### 19. Coin Change (Fewest Coins DP)
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Fewest coins needed to make up target amount.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP array initialized to infinity.
- **Complexity:** $O(N \times \text{amount})$ Time, $O(\text{amount})$ Space.

#### 20. Binary Tree Maximum Path Sum
- **College/Drive:** Advanced SDE Assessment 2023
- **Problem Summary:** Find maximum path sum of any non-empty path in binary tree.
- **Constraints:** Number of nodes $\le 3 \times 10^4$.
- **LeetCode Equivalent:** [124. Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/)
- **Approach:** Post-order DFS computing maximum positive branch contribution.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

---

## 🧠 Frequent CS & Aptitude Questions in D. E. Shaw OA
1. **Database Indexing & B+ Trees:**
   - Why do databases use B+ Trees instead of AVL or Red-Black Trees for on-disk indices?
   - *Answer:* High fanout (hundreds of child pointers per node) dramatically reduces tree height, reducing disk I/O seek operations from $O(\log_2 N)$ to $O(\log_B N)$. Furthermore, all leaf nodes are connected via a doubly linked list, enabling efficient $O(K)$ sequential range scans.
2. **Probability / Puzzle (The 100 Prisoners Problem):**
   - 100 prisoners numbered 1–100 must find their own number in one of 100 boxes, opening at most 50 boxes each. What strategy gives $> 30\%$ survival probability?
   - *Answer:* Loop-following strategy: each prisoner starts by opening the box labeled with their own number, then opens the box indicated by the number inside, following the cycle. The team survives if all permutation cycles have length $\le 50$, which occurs with probability $1 - \ln(2) \approx 31.18\%$.
3. **Deadlock Detection (Banker's Algorithm):**
   - What condition causes an unsafe state to become an actual deadlock?
   - *Answer:* An unsafe state is not immediately a deadlock, but it lacks a guarantee that all processes can finish without mutual deadlock if every process requests its maximum declared resources simultaneously.
