# Barclays Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏦

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerEarth**
- **Test Duration:** 90 to 105 minutes
- **Structure Breakdown:**
  1. **Technical MCQs Section:** 20 to 25 MCQs (30 mins) covering Core Java (Collections, Concurrency, Garbage Collection, Spring Boot basics), DBMS/SQL, Operating Systems, and Quantitative Aptitude.
  2. **Coding Section:** 2 Coding Questions (Medium difficulty, 60–75 mins).
- **Passing Cutoff:** Full score on at least 1 coding question + major test cases on the 2nd, combined with strong performance on Java/DBMS MCQs (>75%).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Java Fundamentals & OOP MCQs:** `ConcurrentHashMap`, Thread lifecycle, String immutability, Generics, Stream API, Garbage Collection algorithms.
- **Dynamic Programming:** Knapsack variants, longest increasing subsequence, coin change, non-adjacent elements sum, LCS.
- **Arrays & Two Pointers:** Trapping rain water, container with most water, subarray target sums, interval scheduling.
- **SQL Queries & Normalization:** Joins, `GROUP BY`, indexing, ACID properties, window functions (`ROW_NUMBER`, `DENSE_RANK`).
- **Graph & Tree Algorithms:** Shortest path, cycle detection, lowest common ancestor, connected components.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Maximum Sum of Non-Adjacent Elements (House Robber)
- **College/Drive:** BITS Pilani / VIT 2024–2025
- **Problem Summary:** You are given an array of integers representing the amount of money at each house. Adjacent houses have security alarms connected. Return the maximum amount of money you can rob without alerting the police.
- **Constraints:** $1 \le nums.length \le 100$, $0 \le nums[i] \le 400$.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** Space-optimized DP: `dp = max(prev1, prev2 + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Container With Most Water
- **College/Drive:** Thapar University / Manipal 2024–2025
- **Problem Summary:** Given $n$ vertical lines on the x-axis, find two lines that together with the x-axis form a container holding the maximum water.
- **Constraints:** $2 \le n \le 10^5$.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Approach:** Two pointers (`left = 0`, `right = n-1`). Greedily move the pointer pointing to the smaller height inward.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. Connected Components in Financial Transaction Network
- **College/Drive:** Barclays Elevate / Campus Hiring 2024–2025
- **Problem Summary:** Given $n$ bank accounts and a list of bidirectional transfers between them, find the total number of independent financial transaction clusters (connected components).
- **Constraints:** $1 \le n \le 2000$, edges $\le 5000$.
- **LeetCode Equivalent:** [323. Number of Connected Components in an Undirected Graph](https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/)
- **Approach:** Disjoint Set Union (DSU with path compression and rank) or Breadth-First Search (BFS).
- **Complexity:** $O(V + E \cdot \alpha(V))$ Time, $O(V)$ Space.

#### 4. Minimum Cost to Connect All Data Servers (MST)
- **College/Drive:** DTU / NSUT 2024–2025
- **Problem Summary:** Connect all $N$ servers in a network with minimum total cabling cost where edge costs are given.
- **Constraints:** $N \le 1000$.
- **LeetCode Equivalent:** [1584. Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)
- **Approach:** Kruskal's Algorithm with DSU or Prim's algorithm using Priority Queue.
- **Complexity:** $O(E \log E)$ Time, $O(V + E)$ Space.

#### 5. Longest Substring with At Most K Distinct Characters
- **College/Drive:** Pune University / Campus Placement 2024–2025
- **Problem Summary:** Given a transaction code string $S$ and an integer $K$, find the length of the longest substring containing at most $K$ distinct characters.
- **Constraints:** $1 \le |s| \le 5 \times 10^4$, $1 \le K \le 50$.
- **LeetCode Equivalent:** [340. Longest Substring with At Most K Distinct Characters](https://leetcode.com/problems/longest-substring-with-at-most-k-distinct-characters/)
- **Approach:** Sliding window with a hash map frequency counter. Shrink window from the left when map size exceeds $K$.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 6. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Barclays Pune Drive 2024
- **Problem Summary:** Minimum minutes to infect all oranges in grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten oranges at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 7. Course Schedule II (Topological Sort Workflow)
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Find ordering to complete all tasks given prerequisites.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm using indegrees and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 8. Subarray Sums Divisible by K
- **College/Drive:** Barclays India Screening 2024
- **Problem Summary:** Find non-empty continuous subarrays whose sum is divisible by $k$.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- **Approach:** Prefix sum modulo $k$ frequency hash map.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 9. Daily Temperatures / Log Metric Monotonic Stack
- **College/Drive:** BITS Goa 2024
- **Problem Summary:** Return days to wait for a warmer day.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Word Break (Dynamic Programming)
- **College/Drive:** Off-Campus Hiring 2024
- **Problem Summary:** Check if string can be segmented into words in a dictionary.
- **Constraints:** $1 \le s.length \le 300$.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Approach:** 1D boolean DP array.
- **Complexity:** $O(N^2 \cdot L)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Coin Change (Fewest Coins)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Determine minimum coins required to make up amount $A$ given denominations array.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times A)$ Time, $O(A)$ Space.

#### 12. Trapping Rain Water
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Compute amount of trapped water between elevation map bars after rain.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 13. Subarray Sum Equals K
- **College/Drive:** Off-Campus Drive 2023
- **Problem Summary:** Find total number of continuous subarrays whose sum equals $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sum with hash map of prefix frequencies.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 14. Lowest Common Ancestor in Binary Tree
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Given binary tree and two nodes, return their lowest common ancestor.
- **Constraints:** Nodes $\le 10^5$.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Approach:** Post-order DFS returning non-null branch.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 15. Longest Increasing Subsequence
- **College/Drive:** Campus Slot 3 (2023)
- **Problem Summary:** Find length of longest strictly increasing subsequence in an array.
- **Constraints:** $1 \le nums.length \le 2500$.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Approach:** Binary search with tails array (`std::lower_bound`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 16. Merge Intervals
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Merge all overlapping intervals in list.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time and merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 17. Longest Common Subsequence
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Given two strings `text1` and `text2`, return the length of their longest common subsequence.
- **Constraints:** $1 \le |text1|, |text2| \le 1000$.
- **LeetCode Equivalent:** [1143. Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/)
- **Approach:** 2D DP: `dp[i][j] = dp[i-1][j-1] + 1` if match, else `max(dp[i-1][j], dp[i][j-1])`.
- **Complexity:** $O(M \cdot N)$ Time and Space.

#### 18. Valid Parentheses
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Determine if string brackets are properly closed.
- **Constraints:** $1 \le s.length \le 10^4$.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Stack matching opening with closing brackets.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 19. Search in Rotated Sorted Array
- **College/Drive:** Technical Assessment 2023
- **Problem Summary:** Find target in rotated sorted array in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 5000$.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking sorted half.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 20. Product of Array Except Self
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Output array where each index is product of all elements except itself without division.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Prefix product from left, suffix product from right.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

---

## 🧠 Frequent Java & DBMS MCQs Asked in Barclays OA
1. **`ConcurrentHashMap` Internal Mechanics:**
   - How does `ConcurrentHashMap` achieve thread safety without synchronizing the whole map?
   - *Answer:* In Java 8+, it uses CAS (Compare-And-Swap) for empty bucket insertion and bucket-level synchronized blocks on the head node for collisions, avoiding whole-table locking.
2. **`volatile` vs `synchronized`:**
   - Does `volatile` guarantee atomicity of compound operations like `count++`?
   - *Answer:* No, `volatile` guarantees visibility across CPU caches and prevents instruction reordering, but doesn't guarantee atomicity. Use `AtomicInteger` or `synchronized`.
3. **SQL Indexing Trade-offs:**
   - Why do multiple non-clustered indexes slow down `INSERT` and `UPDATE` operations?
   - *Answer:* Because each row mutation requires updating the B+ tree structure for all affected secondary indexes.
4. **Spring Bean Scopes:**
   - What is the difference between Singleton and Prototype scopes in Spring?
   - *Answer:* Singleton creates a single shared instance per Spring IoC container (default), while Prototype instantiates a new independent bean instance each time it is requested from the container.
