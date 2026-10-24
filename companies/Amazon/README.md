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
- **Sliding Window & Two Pointers:** Substring matching, maximum/minimum segment costs, grouping binary elements.
- **Heaps & Priority Queues:** Top K frequent elements, minimum cost to connect sticks, request scheduling across least busy servers.
- **Dynamic Programming:** Knapsack variants, bounded capacity choices, binary string expansion with wildcard replacement.
- **Breadth-First Search (BFS):** Multi-source BFS on 2D grid (routing packages, infection/rotting grids).
- **Monotonic Stack / Queue:** Sum of subarray ranges, largest rectangle in histogram, maximum sustainable cluster size.
- **Greedy Optimization:** Armor shield usage, minimum keypresses on custom keypad, second maximum triplets.

---

## 📝 Verified Multi-Year OA Question Bank (Past 3 Years)
*Every problem listed below is a distinct, verified question sourced from 2023, 2024, and 2025/2026 campus placement drives (IITs, NITs, BITS, DTU) and off-campus Amazon OAs. Duplicates across college slots have been strictly merged.*

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

#### 6. Binary String Expansion with Wildcard '!' (Amazon OA 2024 SDE-1/2)
- **College/Drive:** Amazon Off-Campus Hiring 2024
- **Problem Summary:** Given a string containing `'0'`, `'1'`, and `'!'`, each `'!'` must be replaced by either `'0'` or `'1'`. Each `"01"` subsequence incurs cost $X$, and each `"10"` subsequence incurs cost $Y$. Find the minimum total cost among all possible valid replacements.
- **Approach:** 
  - Since cost depends linearly on prefix/suffix counts of 0s and 1s, the optimal replacement is monotonic: all `'!'` up to some index $i$ become `'0'`, and all subsequent `'!'` become `'1'` (or vice-versa).
  - Compute costs for all partition split points using prefix/suffix count arrays in $O(N)$ time.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Stock Inventory Non-Positive Balance Index (Amazon OA 2024)
- **College/Drive:** Amazon SDE New Grad 2024
- **Problem Summary:** Given an array representing daily incoming and outgoing inventory changes, find the earliest day index where the cumulative inventory balance becomes $\le 0$, or return -1 if inventory remains positive throughout.
- **Approach:** Single-pass prefix sum: accumulate daily changes into `running_balance`, return current index as soon as `running_balance <= 0`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Request Queue Scheduling Across Least Busy Servers
- **College/Drive:** Amazon Campus Placement 2024
- **Problem Summary:** There are $K$ servers and a stream of incoming requests. Each request arrives at time $t$ and takes duration $d$. A request must be assigned to an available server with the minimum current load (number of requests handled), breaking ties with the smallest server index. If all servers are busy, drop the request. Output total dropped requests.
- **Approach:** Two Priority Queues:
  - `busy_servers`: Min-Heap storing `(free_time, server_id, current_load)`.
  - `available_servers`: Min-Heap storing `(current_load, server_id)`.
  - At each arrival time $t$, pop all expired jobs from `busy_servers` into `available_servers`.
- **Complexity:** $O(N \log K)$ Time, $O(K)$ Space.

#### 9. Minimum Health to Beat Game with Armor Shield
- **College/Drive:** Amazon University Recruiting 2024
- **Problem Summary:** You are playing a game with $N$ levels where level $i$ deals `damage[i]` damage. You start with initial health and have an armor shield that can absorb up to `armor` damage for exactly one level of your choice. Find minimum initial health required to finish all levels with health $\ge 1$.
- **LeetCode Equivalent:** [2214. Minimum Health to Beat Game](https://leetcode.com/problems/minimum-health-to-beat-game/)
- **Approach:** Greedily use the armor on the level with the highest damage: `damage_absorbed = min(max_element(damage), armor)`. Total health = $\sum \text{damage} - \text{damage\_absorbed} + 1$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 10. Optimal Parcel Delivery / K-Truck Capacity Packing
- **College/Drive:** Amazon Campus Drive 2024
- **Problem Summary:** Given $N$ packages of known weights and $K$ identical delivery trucks. Packages must be delivered in given order. Find the minimum truck capacity such that all packages are delivered within $D$ days.
- **LeetCode Equivalent:** [1011. Capacity To Ship Packages Within D Days](https://leetcode.com/problems/capacity-to-ship-packages-within-d-days/)
- **Approach:** Binary Search on answer in range $[\max(\text{weights}), \sum \text{weights}]$. Greedily count days needed for a mid capacity.
- **Complexity:** $O(N \log(\sum \text{weights}))$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Rotting Oranges (Multi-Source BFS)
- **College/Drive:** On-Campus Slot 1 (2023)
- **Problem Summary:** Minimum minutes to rot all fresh oranges on grid.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time.

#### 12. Reorder Data in Log Files
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Reorder logs such that letter-logs come before digit-logs, sorted lexicographically.
- **LeetCode Equivalent:** [937. Reorder Data in Log Files](https://leetcode.com/problems/reorder-data-in-log-files/)
- **Complexity:** $O(M \cdot N \log N)$ Time.

#### 13. Course Schedule II (Topological Sort)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Valid ordering of course completion dependencies.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Complexity:** $O(V + E)$ Time.

#### 14. Word Break (Dynamic Programming)
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Check if string can be segmented into dictionary words.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Complexity:** $O(N^2)$ Time.

#### 15. LRU Cache Implementation
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Design $O(1)$ get and put cache with least recently used eviction.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Complexity:** $O(1)$ Time per op.

#### 16. Minimum Swaps to Group All 1s Together
- **College/Drive:** Amazon Campus Slot 2023
- **Problem Summary:** Given a binary array, return the minimum number of swaps required to group all `1`s present in the array together in any place in the array.
- **LeetCode Equivalent:** [1151. Minimum Swaps to Group All 1's Together](https://leetcode.com/problems/minimum-swaps-to-group-all-1s-together/)
- **Approach:** Count total 1s ($K$). Use a sliding window of fixed size $K$. Minimum swaps needed is $K - \max(\text{1s in any window of size } K)$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 17. Robot Bounded In Circle
- **College/Drive:** Off-Campus Drive 2023
- **Problem Summary:** A robot on infinite plane starts at $(0, 0)$ facing north. Given instructions `'G'`, `'L'`, `'R'`, return true if there exists a circle such that robot never leaves the circle after infinite repetitions.
- **LeetCode Equivalent:** [1041. Robot Bounded In Circle](https://leetcode.com/problems/robot-bounded-in-circle/)
- **Approach:** Simulate instructions once. Robot is bounded if position returns to $(0, 0)$ or direction is not north.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 18. Maximum Area of a Piece of Cake After Cuts
- **College/Drive:** Amazon Intern Slot 2023
- **Problem Summary:** Given rectangular cake dimensions $H \times W$ and arrays `horizontalCuts` and `verticalCuts`. Return the maximum area of a piece of cake after all cuts modulo $10^9+7$.
- **LeetCode Equivalent:** [1465. Maximum Area of a Piece of Cake After Horizontal and Vertical Cuts](https://leetcode.com/problems/maximum-area-of-a-piece-of-cake-after-horizontal-and-vertical-cuts/)
- **Approach:** Sort cut arrays. Find maximum difference between consecutive horizontal cuts and vertical cuts. Max area = $(max\_h \times max\_v) \pmod{10^9+7}$.
- **Complexity:** $O(H \log H + V \log V)$ Time.

#### 19. Pairs of Songs With Total Durations Divisible by 60
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Return number of pairs $(i, j)$ with $i < j$ such that `(time[i] + time[j]) % 60 == 0`.
- **LeetCode Equivalent:** [1010. Pairs of Songs With Total Durations Divisible by 60](https://leetcode.com/problems/pairs-of-songs-with-total-durations-divisible-by-60/)
- **Approach:** 60-element remainder frequency array: add `count[(60 - rem) % 60]` to total.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 20. Count Binary Substrings (Two Groups Counter)
- **College/Drive:** Amazon WOW Hiring 2023
- **Problem Summary:** Count non-empty substrings that have an equal number of consecutive 0's and 1's.
- **LeetCode Equivalent:** [696. Count Binary Substrings](https://leetcode.com/problems/count-binary-substrings/)
- **Approach:** Group consecutive identical characters into run lengths. For each adjacent group pair, add $\min(len_1, len_2)$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 21. Critical Connections in AWS Network Infrastructure (Tarjan's Bridges)
- **College/Drive:** Amazon Systems Slot 2023
- **Problem Summary:** Given network of $N$ data center routers and connections, find all critical connections whose failure partitions the network into multiple components.
- **LeetCode Equivalent:** [1192. Critical Connections in a Network](https://leetcode.com/problems/critical-connections-in-a-network/)
- **Approach:** Tarjan’s DFS bridge-finding algorithm using `discovery_time` and `lowest_reachable_time`.
- **Complexity:** $O(V + E)$ Time, $O(V)$ Space.

#### 22. Maximum Number of Books from Contiguous Shelves (Monotonic Stack DP)
- **College/Drive:** Amazon Fall 2023
- **Problem Summary:** Given $N$ shelves with `books[i]` books. You must select a contiguous subsegment of shelves and take books such that the number of books taken strictly increases shelf-by-shelf. Maximize total books collected.
- **LeetCode Equivalent:** [2355. Maximum Number of Books You Can Take](https://leetcode.com/problems/maximum-number-of-books-you-can-take/)
- **Approach:** Monotonic stack finding the previous index $j$ where $books[j] < books[i] - (i - j)$. Use arithmetic progression formulas to compute transitions in $O(1)$.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.
