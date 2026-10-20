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
- **Monotonic Queue & DP Optimization:** Jump Game VI, bounded window maximums.
- **Tree DP & Subtree Aggregations:** House Robber III, subtree path sums, rerooting.
- **Meet-in-the-Middle Optimization:** Partition problems with large values and $N \le 40$.
- **Graphs & Minimum Spanning Trees:** Storage node cluster interconnection.

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

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Sliding Window Maximum (Cache Buffer)
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Maximum element in sliding window of size $K$.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Complexity:** $O(N)$ Time.

#### 6. Course Schedule II (Disk Snapshot Dependency)
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Valid order to execute dependent disk snapshot tasks.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Complexity:** $O(V + E)$ Time.

#### 7. Coin Change II (Storage Unit Allocations)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Number of combinations to form target block capacity.
- **LeetCode Equivalent:** [518. Coin Change II](https://leetcode.com/problems/coin-change-ii/)
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 8. Word Ladder (Log Transformation Sequence)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Shortest transformation path between two file names.
- **LeetCode Equivalent:** [127. Word Ladder](https://leetcode.com/problems/word-ladder/)
- **Complexity:** $O(M^2 \times N)$ Time.
