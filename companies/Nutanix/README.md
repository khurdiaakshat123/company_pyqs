# Nutanix Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) ☁️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 to 120 minutes
- **Structure Breakdown:**
  - 2 to 3 Algorithmic Coding Problems (Competitive Programming / Hard).
  - (In select drives) 10 to 15 Core Systems MCQs (Virtual Memory, Hypervisors, Operating Systems, File Systems).
- **Evaluation Criteria:**
  - Nutanix builds enterprise cloud infrastructure and hyperconverged storage systems (45+ LPA CTC for SDE-1).
  - High algorithmic rigor with strict execution time limits.
  - Solving both coding problems with 100% test-case coverage is standard for an interview call.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Monotonic Queue & DP Optimization:** Jump Game VI, bounded window maximums, subarray sum variants.
- **Tree DP & Subtree Aggregations:** House Robber III, lowest common ancestors, tree diameter.
- **Meet-in-the-Middle Optimization:** Partition problems with large values and $N \le 40$.
- **Shortest Paths & 0-1 BFS:** Minimum cost path in grid, network delay time, multi-route transit.
- **Interval Scheduling & Greedy:** Non-overlapping intervals, meeting rooms, VM core allocations.
- **Systems & Hypervisor MCQs:** Type-1 vs Type-2 hypervisors, page tables, TLB shootdowns, distributed consensus (Raft/Paxos).

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Jump Game VI / Storage Queue Buffer (Monotonic Deque + DP)
- **College/Drive:** IIT Kanpur / IIT Madras 2024
- **Problem Statement:** You are given a 0-indexed integer array `nums` and an integer `k`. You are initially standing at index 0. In one move, you can jump at most `k` steps forward without stepping outside the array boundaries. Your goal is to reach index $n - 1$ with the maximum score.
- **LeetCode Equivalent:** [1696. Jump Game VI](https://leetcode.com/problems/jump-game-vi/)
- **Approach:** Dynamic programming optimized with a Monotonic Decreasing Deque: $dp[i] = nums[i] + \max_{j = \max(0, i-k)}^{i-1} dp[j]$. Deque stores indices of maximum $dp$ values in window of size $k$.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 2. Virtual Disk Partitioning with Meet-in-the-Middle
- **College/Drive:** IIT Roorkee / BITS Pilani 2024
- **Problem Statement:** Given an array of $N$ storage blocks ($N \le 34$) with individual capacities up to $10^9$. Partition the storage blocks into two virtual disks such that the absolute capacity difference between the two virtual disks is minimized.
- **Approach:** Meet-in-the-Middle: Generate all $2^{17}$ subset sums of the first half and sort them. For each subset sum in the second half, binary search the closest complement in the first half using `std::lower_bound`.
- **Complexity:** $O(N \cdot 2^{N/2})$ Time.

#### 3. Storage Cluster Interconnection (Kruskal's MST)
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Statement:** There are $N$ hyperconverged nodes on a network grid. Nodes can be connected using 10GbE cables (cost is Manhattan distance between nodes) or via high-speed fiber bridges. Find the minimum total cost to make all nodes interconnected.
- **LeetCode Equivalent:** [1584. Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)
- **Approach:** Prim's Algorithm or Kruskal's with Disjoint Set Union (DSU).
- **Complexity:** $O(N^2)$ Time.

#### 4. House Robber III / Independent Storage Sets in Tree
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Statement:** The storage nodes of a distributed file system form a binary tree. Two directly-linked nodes cannot be selected simultaneously due to replication constraints. Find the maximum total capacity that can be harvested.
- **LeetCode Equivalent:** [337. House Robber III](https://leetcode.com/problems/house-robber-iii/)
- **Approach:** Tree DP: For each node, return pair `(with_root, without_root)`.
  $$\text{with} = val + left.\text{without} + right.\text{without}$$
  $$\text{without} = \max(left.\text{with}, left.\text{without}) + \max(right.\text{with}, right.\text{without})$$
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 5. Minimum Cost to Make at Least One Valid Path in a Grid (0-1 BFS)
- **College/Drive:** IIT Bombay 2024
- **Problem Statement:** Given an $M \times N$ grid where each cell has a sign pointing right, left, down, or up. You can modify the sign on a cell with cost 1. Find the minimum cost to make at least one valid path from $(0, 0)$ to $(M-1, N-1)$.
- **LeetCode Equivalent:** [1368. Minimum Cost to Make at Least One Valid Path in a Grid](https://leetcode.com/problems/minimum-cost-to-make-at-least-one-valid-path-in-a-grid/)
- **Approach:** 0-1 BFS using `std::deque`. If moving in direction of existing arrow, edge cost is 0 (push front); if changing direction, edge cost is 1 (push back).
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 6. Network Delay Time / Hypervisor Packet Broadcast
- **College/Drive:** IIT Kharagpur 2024
- **Problem Statement:** You are given a network of $N$ servers, labeled $1$ to $N$, and `times`, a list of directed edges representing transmission latency. Send a signal from node $K$. Return the minimum time it takes for all $N$ servers to receive the signal. If impossible, return $-1$.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's algorithm using a Min-Heap priority queue.
- **Complexity:** $O(E \log V)$ Time, $O(V + E)$ Space.

#### 7. Maximum Subarray Sum with One Deletion
- **College/Drive:** BITS Pilani 2024
- **Problem Statement:** Given an array of integers, return the maximum sum for a non-empty subarray with at most one element deletion.
- **LeetCode Equivalent:** [1186. Maximum Subarray Sum with One Deletion](https://leetcode.com/problems/maximum-subarray-sum-with-one-deletion/)
- **Approach:** Two DP state arrays: `dp_no_del[i]` (maximum contiguous subarray ending at $i$ with 0 deletions) and `dp_one_del[i]` (maximum subarray ending at $i$ with exactly 1 deletion).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Bus Routes / Multi-VLAN Transit Network
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Statement:** You are given an array `routes` where `routes[i]` is a bus route that the $i$-th bus repeats forever. You want to travel from `source` to `target`. Return the least number of buses you must take.
- **LeetCode Equivalent:** [815. Bus Routes](https://leetcode.com/problems/bus-routes/)
- **Approach:** BFS on routes (treating each bus route as a graph node). Pre-build mapping from `stop -> list_of_routes`.
- **Complexity:** $O(N^2)$ where $N$ is number of routes, $O(N)$ Space.

#### 9. Non-Overlapping Intervals (VM Core Time Allocation)
- **College/Drive:** DTU Delhi 2024
- **Problem Statement:** Given an array of intervals `intervals` where `intervals[i] = [start_i, end_i]`, return the minimum number of intervals you need to remove to make the rest of the intervals non-overlapping.
- **LeetCode Equivalent:** [435. Non-overlapping Intervals](https://leetcode.com/problems/non-overlapping-intervals/)
- **Approach:** Greedy interval scheduling: Sort intervals by end time `end_i`. Always keep the interval that finishes earliest.
- **Complexity:** $O(N \log N)$ Time, $O(1)$ Space.

#### 10. LRU Distributed Cache Design
- **College/Drive:** IIT Delhi 2024
- **Problem Statement:** Design a data structure that follows the constraints of a Least Recently Used (LRU) cache with $O(1)$ `get` and `put`.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Hash Map combined with Doubly Linked List with dummy head and tail.
- **Complexity:** $O(1)$ Time per operation, $O(\text{Capacity})$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Sliding Window Maximum (Cache Buffer)
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Maximum element in sliding window of size $K$.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Complexity:** $O(N)$ Time.

#### 12. Course Schedule II (Disk Snapshot Dependency)
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Valid order to execute dependent disk snapshot tasks.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Complexity:** $O(V + E)$ Time.

#### 13. Coin Change II (Storage Unit Allocations)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Number of combinations to form target block capacity.
- **LeetCode Equivalent:** [518. Coin Change II](https://leetcode.com/problems/coin-change-ii/)
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 14. Word Ladder (Log Transformation Sequence)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Shortest transformation path between two file names.
- **LeetCode Equivalent:** [127. Word Ladder](https://leetcode.com/problems/word-ladder/)
- **Complexity:** $O(M^2 \times N)$ Time.

#### 15. Trapping Rain Water
- **College/Drive:** NIT Surathkal 2023
- **Problem Statement:** Given $n$ non-negative integers representing an elevation map where the width of each bar is 1, compute how much water it can trap after raining.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers (`left`, `right`) with running maximum heights.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. Infection Spread in Server Rack (Rotting Oranges)
- **College/Drive:** Nutanix Campus Placement 2023
- **Problem Statement:** Multi-source BFS to calculate minutes required for all online nodes to receive security patch.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time and Space.

#### 17. Longest Increasing Subsequence (VM CPU Scaling)
- **College/Drive:** NSUT Delhi 2023
- **Problem Statement:** Given an integer array `nums`, return the length of the longest strictly increasing subsequence.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Approach:** Patience sorting with binary search (`std::lower_bound` on tail array).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 18. Lowest Common Ancestor of a Binary Tree
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Given a binary tree, find the lowest common ancestor (LCA) of two given nodes `p` and `q`.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Approach:** Recursive DFS returning root when `root == p || root == q`. If both left and right recursive calls return non-null, root is the LCA.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 19. Reconstruct Itinerary (Virtual Machine Migration Routing)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Statement:** Given a list of airline tickets, reconstruct the itinerary in lexicographical order starting from `"JFK"`.
- **LeetCode Equivalent:** [332. Reconstruct Itinerary](https://leetcode.com/problems/reconstruct-itinerary/)
- **Approach:** Hierholzer's algorithm for finding Eulerian Path using DFS and adjacency lists.
- **Complexity:** $O(E \log E)$ Time.

#### 20. Decode Ways (Binary Packet Format)
- **College/Drive:** Nutanix University Hiring 2023
- **Problem Statement:** A message containing letters from A-Z is being encoded to numbers using 'A' -> "1", 'B' -> "2", ... 'Z' -> "26". Return total number of ways to decode it.
- **LeetCode Equivalent:** [91. Decode Ways](https://leetcode.com/problems/decode-ways/)
- **Approach:** 1D DP: $dp[i] = dp[i-1] \text{ (if single valid)} + dp[i-2] \text{ (if double valid)}$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent Systems & Hypervisor MCQs Asked in Nutanix OA
1. **Type-1 vs Type-2 Hypervisors:**
   - What is the difference between a Bare-Metal (Type-1) hypervisor (e.g., Nutanix AHV, ESXi) and a Hosted (Type-2) hypervisor (e.g., VirtualBox)?
   - *Answer:* A Type-1 hypervisor runs directly on the bare-metal hardware without an underlying host OS, minimizing context switching overhead and latency. A Type-2 hypervisor runs on top of an existing host OS as an application.
2. **TLB Shootdowns:**
   - What is a TLB Shootdown in a multi-core virtualized environment?
   - *Answer:* When a hypervisor modifies page table mappings on one CPU core, it must invalidate stale translation lookaside buffer (TLB) entries across all other CPU cores via inter-processor interrupts (IPIs), which incurs significant synchronization latency.
