# Arcesium Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Core CS Fundamentals MCQs (20 mins)** – 10 to 15 MCQs covering Operating Systems, DBMS/SQL, OOPs (Java/C++), and Computer Networks.
  2. **Section 2: Algorithmic Coding (60 mins, 2 to 3 Questions)** – Medium to Hard difficulty problems.
- **Evaluation Criteria:**
  - Arcesium (originally spun out of D. E. Shaw) provides post-trade investment lifecycle and asset management software.
  - Stringent evaluation of time and space complexity with emphasis on clean edge-case management and multi-threaded system knowledge.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Graph Theory & Connectivity:** Bipartiteness check (2-coloring), cycle detection, topological sorting, reachability.
- **Strings & Chunk Reversals:** Interval modifications, $k$-step substring reversals, anagram balancing, ticker tokenization.
- **Dynamic Programming & Sliding Window:** Subarray optimizations, bounded coin exchange, sequence scoring, LIS.
- **Priority Queues & Financial Streams:** Stock price fluctuation tracker, merge $K$ sorted feeds, time-series trade reconciliation.
- **Core CS & OOP MCQs:** Java Garbage Collection, SQL indexing & normalization, deadlock conditions, TCP handshake.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Hostile Groups / Bipartite Graph Verification
- **College/Drive:** BITS Pilani / NIT Trichy 2024
- **Problem Summary:** You are given $N$ people and an array of pairs representing hostile relationships. Determine if it is possible to split the people into two distinct groups such that no two people in the same group are hostile toward each other.
- **LeetCode Equivalent:** [886. Possible Bipartition](https://leetcode.com/problems/possible-bipartition/)
- **Approach:** Graph 2-Coloring via Breadth-First Search (BFS) or Depth-First Search (DFS). If an adjacent neighbor already has the same color, return `false`.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 2. Reverse String Chunks in Intervals of K
- **College/Drive:** IIIT Allahabad / DTU 2024
- **Problem Summary:** Given a string $s$ and an integer $k$, reverse the first $k$ characters for every $2k$ characters counting from the start of the string.
- **LeetCode Equivalent:** [541. Reverse String II](https://leetcode.com/problems/reverse-string-ii/)
- **Approach:** Step forward by $2k$ in a loop; reverse the subsegment $[i, \min(i + k - 1, n - 1)]$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. Investment Portfolio Cash Settlement (Running Minimum Balance)
- **College/Drive:** Arcesium Campus Drive 2024
- **Problem Summary:** Given a sequence of $N$ daily trade cash inflows and outflows, determine the minimum initial capital required so that the running balance never drops below zero at any point.
- **Approach:** Prefix sum scan tracking the minimum running balance; required initial capital is $\max(0, -\text{min\_prefix\_sum})$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Stock Price Fluctuation System
- **College/Drive:** NSUT / Manipal 2024
- **Problem Summary:** Design a data structure that tracks fluctuating stock prices with timestamps. Support `update(timestamp, price)`, `current()`, `maximum()`, and `minimum()` in $O(\log N)$ or better.
- **LeetCode Equivalent:** [2034. Stock Price Fluctuation](https://leetcode.com/problems/stock-price-fluctuation/)
- **Approach:** Hash Map for `timestamp -> price`, variable for latest timestamp, and `std::multiset` or two heaps for max/min price tracking with lazy removal.
- **Complexity:** $O(\log N)$ update, $O(1)$ queries.

#### 5. Course Schedule & Dependency Validation
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Given $N$ tasks and prerequisite pairs, determine if all tasks can be scheduled without cyclic deadlocks.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Kahn's Algorithm (Topological Sort using in-degrees).
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Merge K Sorted Financial Transaction Lists
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Merge $K$ sorted linked lists of transactions into a single sorted list.
- **LeetCode Equivalent:** [23. Merge k Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/)
- **Approach:** Min-Heap Priority Queue storing current node of each list.
- **Complexity:** $O(N \log K)$ Time, $O(K)$ Space.

#### 7. Longest Increasing Subsequence
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Find length of longest strictly increasing subsequence of trade volumes.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Approach:** Patience sorting with binary search (`std::lower_bound`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 8. Subarray Sum Equals Target K
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Find number of contiguous subarrays that sum to target $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency counter.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 9. Word Break (Ticker Segmentation)
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Determine if continuous symbol string can be parsed into dictionary tickers.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Approach:** 1D DP with hash set lookup.
- **Complexity:** $O(N^2 \cdot L)$ Time.

#### 10. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Compute minimum time for contagion to spread across entire 2D matrix.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

---

## 🧠 Frequent CS Fundamentals MCQs in Arcesium OA
1. **Database Indexing (Clustered vs Non-Clustered):**
   - What is the difference between a Clustered and a Non-Clustered Index?
   - *Answer:* A Clustered Index alters the physical order of rows in the table (hence only one clustered index per table), whereas a Non-Clustered Index creates a separate B+ tree storing pointers to the actual data rows.
2. **Java Memory Model:**
   - Where are local primitive variables, object references, and the actual objects stored?
   - *Answer:* Local primitive variables and object reference variables are stored on the **Thread Stack**; the actual objects themselves are always instantiated on the **Shared Heap**.
