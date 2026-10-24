# Citi (Citigroup) Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **HackerEarth**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Technical & SQL Quiz (30 mins)** – 15 to 20 MCQs covering SQL Queries, Database Normalization, Java/C++ OOP Concepts (Polymorphism, Inheritance, Exception handling), and Computer Networks.
  2. **Section 2: Coding Assessment (60 mins, 2 Questions):**
     - Question 1: Easy to Medium (Strings, Arrays, Two Pointers)
     - Question 2: Medium (Graph traversals, Dynamic Programming, or 2D Matrix paths)
- **Passing Cutoff:** Full clearance on at least 1 coding question + substantial test cases on the 2nd + high accuracy on the SQL/OOP section (>75%).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **SQL Queries & Database MCQs:** Complex joins, window functions (`RANK()`, `ROW_NUMBER()`, `DENSE_RANK()`), subqueries, ACID properties.
- **Arrays & Two Pointers:** Subarray sums, palindrome verification, interval scheduling, trapping rain water, prefix products.
- **Java & OOP Fundamentals:** Abstract classes vs interfaces, Java Collections (`HashMap` vs `TreeMap`), thread states, immutability.
- **Graph & Matrix Traversals:** Number of islands, grid path counting, cycle detection, BFS/DFS.
- **Dynamic Programming:** Coin change, minimum path sum, house robber, 0/1 knapsack.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Count Number of Islands (Citi Classic)
- **College/Drive:** BITS Pilani / NIT Surathkal 2024–2025
- **Problem Summary:** Given an $M \times N$ 2D binary grid representing a map of `'1'`s (land) and `'0'`s (water), return the number of islands. An island is surrounded by water and is formed by connecting adjacent lands horizontally or vertically.
- **Constraints:** $1 \le M, N \le 300$.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Approach:** Standard BFS or DFS marking visited land cells in-place with `'0'`.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 2. Valid Palindrome with at Most One Deletion
- **College/Drive:** VIT Vellore / Manipal 2024–2025
- **Problem Summary:** Given a string $s$, return `true` if $s$ can be a palindrome after deleting at most one character from it.
- **Constraints:** $1 \le s.length \le 10^5$.
- **LeetCode Equivalent:** [680. Valid Palindrome II](https://leetcode.com/problems/valid-palindrome-ii/)
- **Approach:** Two pointers from left and right. When mismatch occurs at $(i, j)$, check if $s[i+1 \dots j]$ or $s[i \dots j-1]$ is a palindrome.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. Real SQL Challenge: Customers with Zero Recent Orders
- **College/Drive:** Citi Graduate Analyst Campus Drive 2024–2025
- **Problem Summary:** Write a query to find the names of all customers who have not placed an order in the last 180 days.
- **SQL Solution:**
  ```sql
  SELECT c.customer_name
  FROM Customers c
  LEFT JOIN Orders o ON c.customer_id = o.customer_id
                     AND o.order_date >= CURRENT_DATE - INTERVAL '180 days'
  WHERE o.order_id IS NULL;
  ```

#### 4. Coin Change (Fewest Coins)
- **College/Drive:** DTU / NSUT 2024–2025
- **Problem Summary:** Return the fewest number of coins that you need to make up a payment amount from available coin denominations.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP array initialized to $\infty$: `dp[i] = min(dp[i], dp[i - coin] + 1)`.
- **Complexity:** $O(N \times \text{amount})$ Time, $O(\text{amount})$ Space.

#### 5. Trapping Rain Water (Two Pointers)
- **College/Drive:** Pune University / IIIT Allahabad 2024–2025
- **Problem Summary:** Given $n$ non-negative integers representing elevation map, compute trapped water.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers inward maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 6. Course Schedule (Topological Sort)
- **College/Drive:** Citi Pune Campus 2024
- **Problem Summary:** Determine if workflow tasks can be scheduled without cyclic deadlocks.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Kahn's Algorithm using indegrees and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 7. Daily Temperatures / Metric Spike Monotonic Stack
- **College/Drive:** Campus Slot 2024
- **Problem Summary:** Return days to wait for a higher value.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 8. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Compute minimum time for contagion to spread across entire 2D matrix.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 9. Subarray Sums Divisible by K
- **College/Drive:** Citi India Screening 2024
- **Problem Summary:** Count non-empty continuous subarrays with sum divisible by $k$.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- **Approach:** Prefix sums modulo $k$ stored in Hash Map.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 10. Valid Parentheses
- **College/Drive:** Off-Campus Screening 2024
- **Problem Summary:** Check if string brackets are balanced.
- **Constraints:** $1 \le s.length \le 10^4$.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Stack matching opening with closing brackets.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Minimum Path Sum in Grid
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Minimum cost path from $(0,0)$ to $(M-1, N-1)$ moving only right or down.
- **Constraints:** $1 \le M, N \le 200$.
- **LeetCode Equivalent:** [64. Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/)
- **Approach:** 2D DP: `dp[i][j] = grid[i][j] + min(dp[i-1][j], dp[i][j-1])`.
- **Complexity:** $O(M \times N)$ Time, $O(N)$ Space.

#### 12. Subarray Sum Equals K
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Find total continuous subarrays whose sum equals $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency counter.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 13. Merge Intervals (Financial Transaction Windows)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Merge all overlapping transaction settlement intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time; merge overlaps.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 14. Lowest Common Ancestor in Binary Tree
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Find lowest common ancestor node in binary tree.
- **Constraints:** Nodes $\le 10^5$.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Approach:** Post-order DFS returning non-null branch.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 15. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find length of longest substring without duplicate characters.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with hash map storing last seen indices.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 16. Product of Array Except Self without Division
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 17. House Robber (1D Dynamic Programming)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Maximize stolen value without robbing two adjacent houses.
- **Constraints:** $1 \le nums.length \le 100$.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** DP: `dp[i] = max(dp[i-1], dp[i-2] + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 18. Best Time to Buy and Sell Stock
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Maximize profit with a single transaction.
- **Constraints:** $1 \le prices.length \le 10^5$.
- **LeetCode Equivalent:** [121. Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- **Approach:** One pass tracking minimum price so far.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 19. Search in Rotated Sorted Array
- **College/Drive:** Technical Assessment 2023
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

## 🧠 Frequent Java & OOP MCQs in Citi OA
1. **Abstract Class vs Interface (Java 8+):**
   - Can an interface have method implementations in Java 8+?
   - *Answer:* Yes, through `default` and `static` methods. However, interfaces still cannot hold mutable state (instance variables), whereas abstract classes can.
2. **`equals()` and `hashCode()` Contract:**
   - What happens if two objects are equal according to `equals()`, but have different hash codes?
   - *Answer:* The contract is violated. Storing them in a `HashSet` or `HashMap` will result in duplicate entries and lookups failing to locate the object.
3. **Database Joins & NULL Values:**
   - What is the difference between `LEFT JOIN` and `INNER JOIN` when matching on nullable foreign keys?
   - *Answer:* An `INNER JOIN` discards any rows from the left table where the join condition does not match (including where the foreign key is NULL). A `LEFT JOIN` preserves all left-table rows, populating right-table columns with NULL if no match exists.
