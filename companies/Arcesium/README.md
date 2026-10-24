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
- **Dynamic Programming & Sliding Window:** Subarray optimizations, bounded coin exchange, sequence scoring, LIS, partition labels.
- **Priority Queues & Financial Streams:** Stock price fluctuation tracker, merge $K$ sorted feeds, time-series trade reconciliation, frequency heaps.
- **Core CS & OOP MCQs:** Java Garbage Collection, SQL indexing & normalization, deadlock conditions, TCP handshake.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Hostile Groups / Bipartite Graph Verification
- **College/Drive:** BITS Pilani / NIT Trichy 2024–2025
- **Problem Summary:** You are given $N$ people and an array of pairs representing hostile relationships. Determine if it is possible to split the people into two distinct groups such that no two people in the same group are hostile toward each other.
- **Constraints:** $1 \le N \le 2000$, hostile pairs $\le 10^4$.
- **LeetCode Equivalent:** [886. Possible Bipartition](https://leetcode.com/problems/possible-bipartition/)
- **Approach:** Graph 2-Coloring via Breadth-First Search (BFS) or Depth-First Search (DFS). If an adjacent neighbor already has the same color, return `false`.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 2. Reverse String Chunks in Intervals of K
- **College/Drive:** IIIT Allahabad / DTU 2024–2025
- **Problem Summary:** Given a string $s$ and an integer $k$, reverse the first $k$ characters for every $2k$ characters counting from the start of the string.
- **Constraints:** $1 \le s.length \le 10^4$, $1 \le k \le 10^4$.
- **LeetCode Equivalent:** [541. Reverse String II](https://leetcode.com/problems/reverse-string-ii/)
- **Approach:** Step forward by $2k$ in a loop; reverse the subsegment $[i, \min(i + k - 1, n - 1)]$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. Investment Portfolio Cash Settlement (Running Minimum Balance)
- **College/Drive:** Arcesium Campus Drive 2024–2025
- **Problem Summary:** Given a sequence of $N$ daily trade cash inflows and outflows, determine the minimum initial capital required so that the running balance never drops below zero at any point.
- **Constraints:** $1 \le N \le 10^5$, $-10^6 \le \text{transaction}[i] \le 10^6$.
- **Approach:** Prefix sum scan tracking the minimum running balance; required initial capital is $\max(0, -\text{min\_prefix\_sum})$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Stock Price Fluctuation System
- **College/Drive:** NSUT / Manipal 2024–2025
- **Problem Summary:** Design a data structure that tracks fluctuating stock prices with timestamps. Support `update(timestamp, price)`, `current()`, `maximum()`, and `minimum()` in $O(\log N)$ or better.
- **Constraints:** Up to $10^5$ operations.
- **LeetCode Equivalent:** [2034. Stock Price Fluctuation](https://leetcode.com/problems/stock-price-fluctuation/)
- **Approach:** Hash Map for `timestamp -> price`, variable for latest timestamp, and `std::multiset` or two heaps for max/min price tracking with lazy removal.
- **Complexity:** $O(\log N)$ update, $O(1)$ queries.

#### 5. Course Schedule & Dependency Validation
- **College/Drive:** Campus Placement 2024–2025
- **Problem Summary:** Given $N$ tasks and prerequisite pairs, determine if all tasks can be scheduled without cyclic deadlocks.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Kahn's Algorithm (Topological Sort using in-degrees).
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 6. Minimum Swaps to Group All 1's Together II
- **College/Drive:** Arcesium Hyderabad Off-Campus 2024
- **Problem Summary:** A circular array of binary integers is given. Return the minimum number of swaps needed to group all 1's present in the array together in any circular location.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [2134. Minimum Swaps to Group All 1's Together II](https://leetcode.com/problems/minimum-swaps-to-group-all-1s-together-ii/)
- **Approach:** Sliding window of fixed size equal to total count of 1's in the array ($K$). Concatenate array with itself to simulate circular wraparound; find window with maximum count of 1's. Answer is $K - \text{max\_ones\_in\_window}$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Find All Anagrams in a String
- **College/Drive:** NIT Surathkal / IIT BHU 2024
- **Problem Summary:** Given strings $s$ and $p$, return all starting indices of $p$'s anagrams in $s$.
- **Constraints:** $1 \le |s|, |p| \le 3 \times 10^4$.
- **LeetCode Equivalent:** [438. Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string/)
- **Approach:** Fixed size sliding window of length $|p|$ maintaining character counts array.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Partition Labels / Chunk Partitioning
- **College/Drive:** Arcesium University Hiring 2024
- **Problem Summary:** Partition a string $s$ into as many parts as possible so that each letter appears in at most one part. Return list of partition sizes.
- **Constraints:** $1 \le s.length \le 500$.
- **LeetCode Equivalent:** [763. Partition Labels](https://leetcode.com/problems/partition-labels/)
- **Approach:** Record the last occurring index of each character. Greedily extend partition boundary `end = max(end, last[s[i]])`. When $i == end$, record chunk size and start new partition.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Reorganize String / Trade Order Sequence
- **College/Drive:** IIIT Delhi 2024
- **Problem Summary:** Rearrange string $s$ so that adjacent characters are not equal. If impossible, return `""`.
- **Constraints:** $1 \le s.length \le 500$.
- **LeetCode Equivalent:** [767. Reorganize String](https://leetcode.com/problems/reorganize-string/)
- **Approach:** Max-Heap of character frequencies. Greedily place the top character and buffer it until the next character is chosen.
- **Complexity:** $O(N \log \Sigma)$ Time, $O(\Sigma)$ Space.

#### 10. Longest Consecutive Sequence in $O(N)$
- **College/Drive:** BITS Goa 2024
- **Problem Summary:** Return the length of the longest consecutive elements sequence from an unsorted array in $O(N)$ time.
- **Constraints:** $0 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [128. Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/)
- **Approach:** Hash set storage; only initiate sequence streak loop if `num - 1` is not present in set.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Merge K Sorted Financial Transaction Lists
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Merge $K$ sorted linked lists of transactions into a single sorted list.
- **Constraints:** $K \le 10^4$.
- **LeetCode Equivalent:** [23. Merge k Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/)
- **Approach:** Min-Heap Priority Queue storing current node of each list.
- **Complexity:** $O(N \log K)$ Time, $O(K)$ Space.

#### 12. Longest Increasing Subsequence
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Find length of longest strictly increasing subsequence of trade volumes.
- **Constraints:** $1 \le nums.length \le 2500$.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Approach:** Patience sorting with binary search (`std::lower_bound`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 13. Subarray Sum Equals Target K
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Find number of contiguous subarrays that sum to target $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency counter.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 14. Word Break (Ticker Segmentation)
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Determine if continuous symbol string can be parsed into dictionary tickers.
- **Constraints:** $1 \le s.length \le 300$.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Approach:** 1D DP with hash set lookup.
- **Complexity:** $O(N^2 \cdot L)$ Time.

#### 15. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Compute minimum time for contagion to spread across entire 2D matrix.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS starting from all rotten cells.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 16. Daily Temperatures / Transaction Spikes
- **College/Drive:** Arcesium Slot 2023
- **Problem Summary:** Find days to wait for a warmer temperature.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 17. Number of Islands in Asset Matrix
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Count connected components of 1s in 2D binary grid.
- **Constraints:** $M, N \le 300$.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Approach:** BFS or DFS marking visited land cells.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 18. Valid Parentheses with Multiple Nestings
- **College/Drive:** Campus Screening 2023
- **Problem Summary:** Determine if brackets `()`, `{}`, `[]` are validly closed.
- **Constraints:** $1 \le s.length \le 10^4$.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Stack matching opening brackets with top.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 19. Coin Change (Fewest Coins DP)
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Return fewest coins needed to make up given amount.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table tracking minimum coins for each sub-amount.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 20. Product of Array Except Self without Division
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Return array `output` where `output[i]` is product of all elements except `nums[i]`.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two passes: prefix product pass from left, followed by running suffix product pass from right.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

---

## 🧠 Frequent CS Fundamentals MCQs in Arcesium OA
1. **Database Indexing (Clustered vs Non-Clustered):**
   - What is the difference between a Clustered and a Non-Clustered Index?
   - *Answer:* A Clustered Index alters the physical order of rows in the table (hence only one clustered index per table), whereas a Non-Clustered Index creates a separate B+ tree storing pointers to the actual data rows.
2. **Java Memory Model:**
   - Where are local primitive variables, object references, and the actual objects stored?
   - *Answer:* Local primitive variables and object reference variables are stored on the **Thread Stack**; the actual objects themselves are always instantiated on the **Shared Heap**.
3. **Optimistic vs Pessimistic Locking:**
   - When is Optimistic Concurrency Control preferred over Pessimistic Locking in financial software?
   - *Answer:* Optimistic locking (via version column check: `UPDATE table SET val = x, version = version + 1 WHERE id = y AND version = old_ver`) is preferred in read-heavy architectures with low write conflict probability, avoiding expensive database lock acquisitions.
