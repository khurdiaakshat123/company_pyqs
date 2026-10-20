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
- **Dynamic Programming:** Knapsack variants, longest increasing subsequence, coin change, non-adjacent elements sum.
- **Arrays & Two Pointers:** Trapping rain water, container with most water, subarray target sums, interval scheduling.
- **SQL Queries & Normalization:** Joins, `GROUP BY`, indexing, ACID properties, window functions (`ROW_NUMBER`, `DENSE_RANK`).
- **Graph & Tree Algorithms:** Shortest path, cycle detection, lowest common ancestor, connected components.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Maximum Sum of Non-Adjacent Elements (House Robber)
- **College/Drive:** BITS Pilani / VIT 2024
- **Problem Summary:** You are given an array of integers representing the amount of money at each house. Adjacent houses have security alarms connected. Return the maximum amount of money you can rob without alerting the police.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** Space-optimized DP: `dp = max(prev1, prev2 + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Container With Most Water
- **College/Drive:** Thapar University / Manipal 2024
- **Problem Summary:** Given $n$ vertical lines on the x-axis, find two lines that together with the x-axis form a container holding the maximum water.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Approach:** Two pointers (`left = 0`, `right = n-1`). Greedily move the pointer pointing to the smaller height inward.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. Connected Components in Financial Transaction Network
- **College/Drive:** Barclays Elevate / Campus Hiring 2024
- **Problem Summary:** Given $n$ bank accounts and a list of bidirectional transfers between them, find the total number of independent financial transaction clusters (connected components).
- **LeetCode Equivalent:** [323. Number of Connected Components in an Undirected Graph](https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/)
- **Approach:** Disjoint Set Union (DSU with path compression and rank) or Breadth-First Search (BFS).
- **Complexity:** $O(V + E \cdot \alpha(V))$ Time, $O(V)$ Space.

#### 4. Minimum Cost to Connect All Data Servers (MST)
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** Connect all $N$ servers in a network with minimum total cabling cost where edge costs are given.
- **LeetCode Equivalent:** [1584. Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/) / Kruskal's MST
- **Approach:** Kruskal's Algorithm with DSU or Prim's algorithm using Priority Queue.
- **Complexity:** $O(E \log E)$ Time, $O(V + E)$ Space.

#### 5. Longest Substring with At Most K Distinct Characters
- **College/Drive:** Pune University / Campus Placement 2024
- **Problem Summary:** Given a transaction code string $S$ and an integer $K$, find the length of the longest substring containing at most $K$ distinct characters.
- **LeetCode Equivalent:** [340. Longest Substring with At Most K Distinct Characters](https://leetcode.com/problems/longest-substring-with-at-most-k-distinct-characters/)
- **Approach:** Sliding window with a hash map frequency counter. Shrink window from the left when map size exceeds $K$.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Coin Change (Fewest Coins)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Determine minimum coins required to make up amount $A$ given denominations array.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times A)$ Time, $O(A)$ Space.

#### 7. Trapping Rain Water
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Compute amount of trapped water between elevation map bars after rain.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Subarray Sum Equals K
- **College/Drive:** Off-Campus Drive 2023
- **Problem Summary:** Find total number of continuous subarrays whose sum equals $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sum with hash map of prefix frequencies.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 9. Lowest Common Ancestor in Binary Tree
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Given binary tree and two nodes, return their lowest common ancestor.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 10. Longest Increasing Subsequence
- **College/Drive:** Campus Slot 3 (2023)
- **Problem Summary:** Find length of longest strictly increasing subsequence in an array.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Approach:** Binary search with tails array (`std::lower_bound`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

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
