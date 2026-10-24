# ServiceNow Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) ⚡

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  - 2 to 4 Algorithmic Coding Problems (LeetCode Medium to Hard).
  - (Role-dependent) 10 MCQs on Core Computer Science (OS, DBMS, OOPs, Computer Networks, and Cloud Microservices).
- **Passing Benchmark:** Solving $\ge 2$ questions completely with optimal time complexity + solid accuracy on CS MCQs.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Difference Arrays & Range Additions:** Converting arrays with range increments, SLA interval tracking.
- **Linked Lists & Pointers:** In-place modifications, reversals between bounds, cycle detection.
- **Task Scheduling & Heaps:** Incident management simulation, CPU cool-down task scheduling, priority queues.
- **Graphs & BFS:** Microservice dependency graphs, blast radius of outages, topological sort.
- **Enterprise SQL Queries:** Incident triage metrics, average resolution times, window functions.
- **Core CS MCQs:** Database transaction isolation levels, optimistic vs pessimistic locking, multithreading, REST APIs.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Minimum Operations to Convert Array A to B via Subarray Range Addition
- **College/Drive:** IIT Roorkee / BITS Goa 2024
- **Problem Statement:** You are given two integer arrays $A$ and $B$ of length $N$. In one operation, you can choose any contiguous subarray and add an integer $K$ to all elements in that subarray. Return the minimum number of operations required to make $A$ identical to $B$.
- **Approach:** Construct difference array $D[i] = B[i] - A[i]$. The minimum operations to reduce $D$ to all zeroes is $\sum \max(0, D[i] - D[i-1])$ for positive differences plus corresponding sum for negative differences.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 2. Reverse Linked List II (Bounded Range In-Place Reversal)
- **College/Drive:** NIT Calicut / DTU 2024
- **Problem Statement:** Given the head of a singly linked list and two integers `left` and `right` where `left <= right`, reverse the nodes of the list from position `left` to position `right`, and return the reversed list in one pass.
- **LeetCode Equivalent:** [92. Reverse Linked List II](https://leetcode.com/problems/reverse-linked-list-ii/)
- **Approach:** Traverse to node `left - 1`. Sub-list reversal using pointer swapping without allocating new nodes.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. IT Outage Blast Radius / Affected Service Nodes (Graph BFS)
- **College/Drive:** IIIT Allahabad 2024
- **Problem Statement:** An enterprise network connects $N$ microservices with directed dependency edges. If service $S$ crashes, all dependent services cascade and fail. Calculate the total blast radius (count of all impacted nodes) and identify the single service whose failure would impact the highest number of services.
- **Approach:** Multi-source BFS or Reverse Topological Sort with bitsets for reachability.
- **Complexity:** $O(V \times (V + E))$ or $O(\frac{V^3}{64})$ with bitset.

#### 4. Real SQL: Unresolved High-Priority Incident Tickets
- **College/Drive:** VIT / Manipal 2024
- **Problem Statement:** Write a query to find support engineers who currently have more than 5 open priority-1 tickets assigned, along with the average resolution time of their closed tickets over the last 30 days.
- **SQL Implementation:**
  ```sql
  SELECT engineer_id,
         COUNT(CASE WHEN status = 'OPEN' AND priority = 1 THEN 1 END) as open_p1_tickets,
         AVG(CASE WHEN status = 'CLOSED' THEN DATEDIFF(hour, created_at, resolved_at) END) as avg_resolution_hours
  FROM Incidents
  WHERE created_at >= CURRENT_DATE - INTERVAL '30 days'
  GROUP BY engineer_id
  HAVING COUNT(CASE WHEN status = 'OPEN' AND priority = 1 THEN 1 END) > 5;
  ```

#### 5. Merge Intervals (Enterprise Maintenance Windows)
- **College/Drive:** IIT Delhi 2024
- **Problem Statement:** Merge all overlapping maintenance downtime windows for datacenter clusters.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort intervals by start time. Merge greedily if current interval starts before previous ends.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 6. Task Scheduler / SLA Incident Queue Cooldown
- **College/Drive:** IIT Kharagpur 2024
- **Problem Statement:** Given a characters array `tasks`, representing the tasks a CPU needs to do, where each letter represents a different task. Tasks could be done in any order. Each task is done in one unit of time. For each unit of time, the CPU could complete either one task or just be idle. However, there is a non-negative integer `n` that represents the cooldown period between two same tasks. Return the least number of units of times that the CPU will take to finish all the given tasks.
- **LeetCode Equivalent:** [621. Task Scheduler](https://leetcode.com/problems/task-scheduler/)
- **Approach:** Greedy math / Max-Heap: Find maximum frequency $M$ and number of tasks having frequency $M$. Total time is $\max(\text{len}(tasks), (M - 1) \times (n + 1) + \text{max\_count})$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. LRU Session Token Cache Implementation
- **College/Drive:** BITS Pilani 2024
- **Problem Statement:** Implement an LRU Cache for managing user session tokens with $O(1)$ `get` and `put`.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Hash Map pointing to Doubly Linked List nodes.
- **Complexity:** $O(1)$ Time per operation.

#### 8. Trapping Rain Water
- **College/Drive:** NIT Trichy 2024
- **Problem Statement:** Calculate total trapped water volume given elevation profile.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers inward from boundaries.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Subarray Sum Equals K (SLA Breach Window)
- **College/Drive:** DTU Delhi 2024
- **Problem Statement:** Given an array of integers `nums` and target `k`, return total contiguous subarrays whose sum equals `k`.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Running prefix sum with hash map frequency tracking.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Search in Rotated Sorted Array
- **College/Drive:** NSUT Delhi 2024
- **Problem Statement:** Find target in rotated sorted array in $O(\log N)$ time.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Modified binary search checking if left or right half is monotonically sorted.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Course Schedule / Module Deployment Dependencies
- **College/Drive:** On-Campus Drive Slot 1 (2023)
- **Problem Statement:** Validate if a deployment pipeline has cyclical dependencies that would cause deadlock during rollout.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Cycle detection in directed graph using DFS 3-coloring (`WHITE`, `GRAY`, `BLACK`) or Kahn's Algorithm.
- **Complexity:** $O(V + E)$ Time.

#### 12. Continuous Subarray Sum Divisible by K
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Return `true` if `nums` has a continuous subarray of size at least two whose elements sum up to a multiple of $k$.
- **LeetCode Equivalent:** [523. Continuous Subarray Sum](https://leetcode.com/problems/continuous-subarray-sum/)
- **Approach:** Prefix sum modulo $k$ stored in a HashMap mapping `remainder -> first_seen_index`.
- **Complexity:** $O(N)$ Time, $O(\min(N, K))$ Space.

#### 13. Maximum Level Sum of a Binary Tree
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Return the smallest level $x$ such that the sum of all the values of nodes at level $x$ is maximal.
- **LeetCode Equivalent:** [1161. Maximum Level Sum of a Binary Tree](https://leetcode.com/problems/maximum-level-sum-of-a-binary-tree/)
- **Approach:** BFS level-order traversal with level size loop.
- **Complexity:** $O(N)$ Time, $O(W)$ Space.

#### 14. String Compression with In-Place Modifiers
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Given an array of characters, compress it in-place using counts for consecutive repeated characters.
- **LeetCode Equivalent:** [443. String Compression](https://leetcode.com/problems/string-compression/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 15. Longest Substring Without Repeating Characters
- **College/Drive:** IIIT Hyderabad 2023
- **Problem Statement:** Find length of longest substring without duplicate characters.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with hash map storing last seen character indices.
- **Complexity:** $O(N)$ Time.

#### 16. Incident Alert Cascading (Rotting Oranges)
- **College/Drive:** Campus Placement 2023
- **Problem Statement:** Multi-source BFS to calculate minutes required for an incident alert to propagate through all connected infrastructure nodes.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time and Space.

#### 17. Word Break (Template Token Validator)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Determine if workflow string can be segmented into dictionary terms.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Complexity:** $O(N^2)$ Time, $O(N)$ Space.

#### 18. Lowest Common Ancestor of a Binary Tree
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Find lowest common ancestor node of two given nodes in a binary tree.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 19. SLA Alert Frequency Balance (Reorganize String)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Rearrange characters so that no two identical characters are adjacent.
- **LeetCode Equivalent:** [767. Reorganize String](https://leetcode.com/problems/reorganize-string/)
- **Complexity:** $O(N \log \Sigma)$ Time.

#### 20. Template Field Expression Expansion (Decode String)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Decode nested string encoding format `k[string]`.
- **LeetCode Equivalent:** [394. Decode String](https://leetcode.com/problems/decode-string/)
- **Approach:** Dual stack for counts and strings.
- **Complexity:** $O(\text{Output Length})$ Time.

---

## 🧠 Frequent CS & DBMS MCQs Asked in ServiceNow OA
1. **Optimistic vs Pessimistic Locking:**
   - In a high-concurrency ticket management system, when is Optimistic Locking preferred over Pessimistic Locking?
   - *Answer:* Optimistic locking (using record version numbers or timestamps) is preferred when read operations vastly outnumber write operations and write collisions are infrequent, avoiding expensive database lock acquisitions.
2. **Transaction Isolation Levels (Read Committed vs Repeatable Read):**
   - What anomaly does Repeatable Read prevent that Read Committed permits?
   - *Answer:* Repeatable Read prevents **Non-Repeatable Reads** (where re-reading the same row within a transaction returns different values modified by another committed transaction).
