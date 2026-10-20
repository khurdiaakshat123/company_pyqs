# Amazon Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 📦

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Structure & Duration:**
  - **Part 1: Coding Challenge (90 minutes)** – 2 algorithmic coding problems (Medium to Hard).
  - **Part 2: Work Style Assessment (15–20 minutes)** – Situational judgment test evaluating Amazon's 16 Leadership Principles (LPs).
- **Proctoring:** Webcam enabled, tab-switch monitoring, copy-paste disabled inside editor.
- **Passing Cutoff:** Full score (100% test cases on both questions) is heavily prioritized for direct interview invites. The Work Style Assessment score is equally weighted.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Sliding Window & Two Pointers:** Substring matching, maximum/minimum segment costs, frequency balance.
- **Heaps & Priority Queues:** Top K frequent elements, minimum cost to connect ropes/servers, median stream.
- **Dynamic Programming:** Knapsack variants, bounded capacity choices, stock buy & sell variations.
- **Breadth-First Search (BFS):** Multi-source BFS on 2D grid (routing packages, infection/rotting grids).
- **Monotonic Stack / Queue:** Next greater element, subarray minimums sum, largest rectangle in histogram.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Amazon Fulfillment Centers / Minimum Keypresses
- **College/Drive:** IIT Roorkee / IIT Kharagpur 2024
- **Problem Summary:** Given a string of lowercase letters representing characters typed on an older keypad where each key can hold multiple characters. Assign letters to keys 1–9 such that total keypresses to type the string is minimized.
- **Approach:** Count character frequencies, sort descending, assign top 9 most frequent letters to 1 press each, next 9 to 2 presses, remaining to 3 presses.
- **Complexity:** $O(N + 26 \log 26) = O(N)$ Time.

#### 2. Maximum Delivery Center Throughput (Parcel Optimization)
- **College/Drive:** BITS Pilani / NIT Warangal 2024
- **Problem Summary:** Given $N$ servers, each with a processing speed. Divide servers into triplets such that the second maximum of each triplet is maximized overall.
- **Approach:** Sort speeds, pick the largest elements greedily to maximize the median of triplets.
- **Complexity:** $O(N \log N)$ Time.

#### 3. Sum of Subarray Ranges (Monotonic Stack)
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** Find the sum of `(max(subarray) - min(subarray))` across all contiguous subarrays of an array of size $N$.
- **Constraints:** $1 \le N \le 10^5$.
- **LeetCode Equivalent:** [2104. Sum of Subarray Ranges](https://leetcode.com/problems/sum-of-subarray-ranges/)
- **Approach:** Monotonic stack to find the count of subarrays where each element acts as the maximum and minimum respectively in $O(N)$.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 4. Minimum Total Cost to Connect Servers (Min-Heap)
- **College/Drive:** IIIT Delhi / VIT 2024
- **Problem Summary:** Repeatedly combine two smallest servers with cost equal to sum until one remains.
- **LeetCode Equivalent:** [1167. Minimum Cost to Connect Sticks](https://leetcode.com/problems/minimum-cost-to-connect-sticks/)
- **Approach:** Min-Heap (`priority_queue`).
- **Complexity:** $O(N \log N)$ Time.

#### 5. Maximum Sustainable Cluster Size (Sliding Window / Monotonic Queue)
- **College/Drive:** Amazon WOW / Campus 2024
- **Problem Summary:** Given processing power and booting power arrays, find maximum length of contiguous servers whose total power $\le \text{budget}$. Total power = $\max(\text{booting}) + \text{sum}(\text{processing}) \times k$.
- **LeetCode Equivalent:** [2444. Count Subarrays With Fixed Bounds](https://leetcode.com/problems/count-subarrays-with-fixed-bounds/)
- **Approach:** Sliding window with Monotonic Decreasing Deque tracking maximum booting power.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Rotting Oranges (Multi-Source BFS)
- **College/Drive:** On-Campus Slot 1 (2023)
- **Problem Summary:** Minimum minutes to rot all fresh oranges on grid.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time.

#### 7. Reorder Data in Log Files
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Reorder logs such that letter-logs come before digit-logs, sorted lexicographically.
- **LeetCode Equivalent:** [937. Reorder Data in Log Files](https://leetcode.com/problems/reorder-data-in-log-files/)
- **Complexity:** $O(M \cdot N \log N)$ Time.

#### 8. Course Schedule II (Topological Sort)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Valid ordering of course completion dependencies.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Complexity:** $O(V + E)$ Time.

#### 9. Word Break (Dynamic Programming)
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Check if string can be segmented into dictionary words.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Complexity:** $O(N^2)$ Time.

#### 10. LRU Cache Implementation
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Design $O(1)$ get and put cache with least recently used eviction.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Complexity:** $O(1)$ Time per op.
