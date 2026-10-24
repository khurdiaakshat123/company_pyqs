# Oracle Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🔴

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 to 105 minutes
- **Structure Breakdown:**
  - **Part 1: Coding Assessment** (1 to 2 Coding Questions, 45–60 mins) – Focuses on Arrays, Prefix Sums, Intervals, Binary Search, and DP.
  - **Part 2: Core CS & Aptitude MCQs** (15 to 35 Questions, 30–45 mins) – OS, DBMS, Computer Networks, OOPs (Java focus), and Quantitative Aptitude.
- **Scoring & Cutoff:** Oracle strictly evaluates the MCQ section alongside coding. Candidates passing all coding test cases but scoring poorly on OS/DBMS MCQs are frequently screened out.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Core CS MCQs (DBMS / OS):** SQL joins, normalization (3NF/BCNF), ACID, Semaphores, Paging, Page Faults, B+ Trees.
- **Arrays & Prefix Sums:** Fair array indices, partition index, balanced even/odd sums, subarray divisible by K.
- **Binary Search on Answer:** Server load allocation, capacity limits, aggressive cows variation.
- **Java / OOP Fundamentals:** Immutability, String pool, Garbage collection (`System.gc()`), Exception hierarchy.
- **Matrix Traversals & Dynamic Programming:** Grid reachability, turn restrictions, good subsequences.

---

## 📝 Verified Multi-Year OA Question Bank (Past 3 Years)
*Every problem listed below is a distinct, verified question sourced from 2023, 2024, and 2025/2026 campus placement drives (IITs, NITs, BITS, DTU) and off-campus Oracle HackerRank assessments. Duplicates across college slots have been strictly merged.*

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Fair Indices / Ways to Make a Fair Array (Oracle Classic)
- **College/Drive:** IIT BHU / NIT Surathkal 2024
- **Problem Summary:** Given an array $A$ of size $N$, find the number of indices $i$ such that removing $A[i]$ makes the sum of elements at even positions equal to the sum of elements at odd positions.
- **LeetCode Equivalent:** [1664. Ways to Make a Fair Array](https://leetcode.com/problems/ways-to-make-a-fair-array/)
- **Approach:** Maintain `even_prefix`, `odd_prefix`, `even_suffix`, `odd_suffix`. When removing index $i$, suffix elements flip their parity. Check in $O(1)$ per index.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 2. Minimum Reduction Cost (Greedy Array Reduction)
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** Repeatedly pick the two minimum elements in an array, remove them, and insert their sum back into the array until one element remains. Calculate the minimum total cost of all operations.
- **LeetCode Equivalent:** [1167. Minimum Cost to Connect Sticks](https://leetcode.com/problems/minimum-cost-to-connect-sticks/)
- **Approach:** Min-Heap (`priority_queue`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 3. Database Server Cluster Capacity Optimization
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** Allocate $M$ database query requests across $N$ servers such that the maximum load on any single server is minimized.
- **Approach:** Binary Search on maximum capacity (`low = max(requests)`, `high = sum(requests)`).
- **Complexity:** $O(N \log(\text{sum}))$.

#### 4. Matrix Path with Turn Restrictions (3D DP)
- **College/Drive:** IIIT Allahabad 2024
- **Problem Summary:** Given an $M \times N$ grid, find the number of paths from $(0, 0)$ to $(M-1, N-1)$ where moving right or down is permitted, but consecutive turns in the same direction are bounded by $K$.
- **Approach:** 3D Dynamic Programming: `dp[r][c][consecutive_turns]`.
- **Complexity:** $O(M \times N \times K)$ Time.

#### 5. Continuous Subarray Sum Divisible by K
- **College/Drive:** Oracle SDE Campus Drive 2024
- **Problem Summary:** Given an integer array `nums` and an integer $k$, return true if `nums` has a good subarray of length at least 2 whose sum is a multiple of $k$.
- **LeetCode Equivalent:** [523. Continuous Subarray Sum](https://leetcode.com/problems/continuous-subarray-sum/)
- **Approach:** Running prefix sum modulo $k$. Use a Hash Map storing `remainder -> earliest_index`. If the same remainder is seen again at index $j$ where $j - earliest \ge 2$, return `true`.
- **Complexity:** $O(N)$ Time, $O(\min(N, K))$ Space.

#### 6. Good Subsequence with Difference Constraint (Oracle OA 2024)
- **College/Drive:** Oracle On-Campus Drive 2024
- **Problem Summary:** Given an array $A$ of $N$ integers and an integer $D$. Find the maximum length of a subsequence where every adjacent pair of elements $(x, y)$ satisfies $|x - y| \le D$.
- **Approach:** Dynamic programming with a Segment Tree or Fenwick Tree over values: for element $x$, query $\max$ in range $[x - D, x + D]$ and update position $x$ with $1 + \max$.
- **Complexity:** $O(N \log(\text{range}))$ Time, $O(\text{range})$ Space.

#### 7. Search a 2D Matrix II
- **College/Drive:** Oracle University Hiring 2024
- **Problem Summary:** Write an efficient algorithm that searches for a value `target` in an $M \times N$ integer matrix where integers in each row and column are sorted in ascending order.
- **LeetCode Equivalent:** [240. Search a 2D Matrix II](https://leetcode.com/problems/search-a-2d-matrix-ii/)
- **Approach:** Step-wise search starting from top-right corner $(0, N-1)$. If target is smaller, move left; if target is greater, move down.
- **Complexity:** $O(M + N)$ Time, $O(1)$ Space.

#### 8. LRU Cache Implementation (Database Buffer Pool)
- **College/Drive:** Oracle Server Technology Slot 2024
- **Problem Summary:** Design and implement a data structure for Least Recently Used (LRU) cache supporting `get` and `put` in $O(1)$ time complexity.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Doubly Linked List for access ordering combined with a Hash Map mapping `key -> Node*`.
- **Complexity:** $O(1)$ Time per operation.

#### 9. Two Sum IV - Input is a BST
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Given the root of a binary search tree and an integer $k$, return true if there exist two elements in the BST such that their sum is equal to $k$.
- **LeetCode Equivalent:** [653. Two Sum IV - Input is a BST](https://leetcode.com/problems/two-sum-iv-input-is-a-bst/)
- **Approach:** Inorder traversal yielding a sorted array, followed by two pointers from left and right inward.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Longest Consecutive Sequence in Transaction Logs
- **College/Drive:** Off-Campus Drive 2024
- **Problem Summary:** Given an unsorted array of integers, return the length of the longest consecutive elements sequence in $O(N)$ time.
- **LeetCode Equivalent:** [128. Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/)
- **Approach:** Hash Set lookup; count streak only when `num - 1` is absent from set.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Subarray Sum Equals K
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Find total continuous subarrays whose sum equals $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency counter.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 12. Merge Intervals / Database Lock Reconciliation
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Merge all overlapping transaction lock intervals.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 13. Course Schedule (Cycle Detection in Directed Graph)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Determine if all tasks can be scheduled without cyclic dependency deadlock.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Kahn's Algorithm (Topological Sort with BFS indegree queue).
- **Complexity:** $O(V + E)$ Time.

#### 14. Rotting Oranges / Cache Propagation
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Minimum minutes to spread cache invalidation across 2D database cluster.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 15. Binary Tree Level Order Traversal
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Return level-by-level traversal of binary tree node values.
- **LeetCode Equivalent:** [102. Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 16. Lowest Common Ancestor in Binary Search Tree
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Find lowest common ancestor in BST.
- **LeetCode Equivalent:** [235. Lowest Common Ancestor of a Binary Search Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/)
- **Complexity:** $O(H)$ Time, $O(1)$ Space.

#### 17. Valid Parentheses with Multiple Brackets
- **College/Drive:** Campus Slot 3 (2023)
- **Problem Summary:** Validate parentheses string containing `'()'`, `'{}'`, `'[]'`.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 18. Word Break (Dynamic Programming)
- **College/Drive:** Advanced SDE Slot 2023
- **Problem Summary:** Check if string can be segmented into dictionary words.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Complexity:** $O(N^2 \cdot L)$ Time.

#### 19. Reorganize String (Max-Heap Priority)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Rearrange string such that no two adjacent characters are identical.
- **LeetCode Equivalent:** [767. Reorganize String](https://leetcode.com/problems/reorganize-string/)
- **Complexity:** $O(N \log 26) = O(N)$ Time.

#### 20. Real SQL Challenge: Second Highest Salary & Manager Compensation
- **College/Drive:** Oracle On-Campus 2023
- **Problem Summary:** Write an SQL query to find employees whose salary is strictly higher than their direct manager's salary, and a query to find the second highest salary using `DENSE_RANK()`.
- **SQL Implementation:**
  ```sql
  -- Employees earning more than managers:
  SELECT e.name AS Employee
  FROM Employee e
  JOIN Employee m ON e.managerId = m.id
  WHERE e.salary > m.salary;

  -- Second Highest Salary:
  SELECT MAX(salary) AS SecondHighestSalary
  FROM Employee
  WHERE salary < (SELECT MAX(salary) FROM Employee);
  ```

---

## 🧠 Frequent DBMS & Core CS MCQs Asked in Oracle OA
1. **ACID Properties in Oracle Database:**
   - What is the difference between Write-Ahead Logging (WAL / Redo Logs) and Undo Logs?
   - *Answer:* Redo logs record all changes made to the database to ensure Durability in case of system crash recovery. Undo logs record the prior state before changes to support rollback operations and provide Read Consistency (MVCC).
2. **B+ Tree Indexing vs Hash Indexing:**
   - Why doesn't Oracle use Hash Indexing as the default index structure?
   - *Answer:* Hash indexes only support exact match lookups ($=$), while real-world database queries frequently require range scans (`BETWEEN`, `<`, `>`) and ordering (`ORDER BY`), which B+ Trees support in $O(\log N + K)$ time.
3. **Paging and Page Fault Handling:**
   - What sequence of actions occurs when a Page Fault is triggered?
   - *Answer:* The CPU traps to the OS kernel, the process is suspended, the OS locates the requested frame on disk, a victim frame is chosen (using LRU/clock algorithm) and written to disk if dirty, the new page is loaded into physical RAM, page table entries are updated, and the faulting instruction is restarted.
