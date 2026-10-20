# ServiceNow Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) ⚡

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  - 2 to 4 Algorithmic Coding Problems (LeetCode Medium to Hard).
  - (Role-dependent) 10 MCQs on Core Computer Science (OS, DBMS, OOPs, Computer Networks).
- **Passing Benchmark:** Solving $\ge 2$ questions completely with optimal time complexity.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Difference Arrays & Range Additions:** Converting arrays with range increments.
- **Linked Lists & Pointers:** In-place modifications, reversals between bounds.
- **Task Scheduling & HashMaps:** Incident management simulation, dependency resolution.
- **Graphs & BFS:** Server dependency graphs, blast radius of outages.

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

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Course Schedule / Module Deployment Dependencies
- **College/Drive:** On-Campus Drive Slot 1 (2023)
- **Problem Statement:** Validate if a deployment pipeline has cyclical dependencies that would cause deadlock during rollout.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Cycle detection in directed graph using DFS 3-coloring (`WHITE`, `GRAY`, `BLACK`) or Kahn's Algorithm.
- **Complexity:** $O(V + E)$ Time.

#### 6. Continuous Subarray Sum Divisible by K
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Return `true` if `nums` has a continuous subarray of size at least two whose elements sum up to a multiple of $k$.
- **LeetCode Equivalent:** [523. Continuous Subarray Sum](https://leetcode.com/problems/continuous-subarray-sum/)
- **Approach:** Prefix sum modulo $k$ stored in a HashMap mapping `remainder -> first_seen_index`.
- **Complexity:** $O(N)$ Time, $O(\min(N, K))$ Space.

#### 7. Maximum Level Sum of a Binary Tree
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Return the smallest level $x$ such that the sum of all the values of nodes at level $x$ is maximal.
- **LeetCode Equivalent:** [1161. Maximum Level Sum of a Binary Tree](https://leetcode.com/problems/maximum-level-sum-of-a-binary-tree/)
- **Approach:** BFS level-order traversal with level size loop.
- **Complexity:** $O(N)$ Time, $O(W)$ Space.

#### 8. String Compression with In-Place Modifiers
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Given an array of characters, compress it in-place using counts for consecutive repeated characters.
- **LeetCode Equivalent:** [443. String Compression](https://leetcode.com/problems/string-compression/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.
