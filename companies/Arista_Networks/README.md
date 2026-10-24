# Arista Networks Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🌐

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** (Strictly proctored)
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Systems, C/C++ & Linux MCQs (30 mins)** – Heavy emphasis on C/C++ Pointers, Memory Management (`malloc` vs `calloc`, struct padding, alignment), Linux commands (`kill`, `chmod`, `netstat`, `strace`), and OS Networking internals (sockets, TCP 3-way handshake, OSI model).
  2. **Section 2: Coding Assessment (60 mins, 3 Questions)** – Medium to Hard algorithmic problems. In many drives, programming languages are restricted strictly to **C, C++, and Java**.
- **Passing Cutoff:** Arista is a high-performance cloud networking and switching company; candidates must clear the Linux/Systems MCQ cutoffs alongside at least 2 complete coding problems.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **C/C++ Memory & Linux MCQs:** Pointer arithmetic, virtual memory, struct padding, signal handling, socket buffers, IPC mechanisms.
- **Heaps & Priority Queues:** Greedy day-by-day workload reductions, packet queue simulations, top-K bandwidth consumers.
- **Bitwise & Networking Math:** Subnet mask parsing, IP packet checksum validation, reversing bits, bitwise trie lookups.
- **Arrays & Two Pointers:** Subarray sums divisible by $K$, sliding window maximum, circular ring buffers.
- **Graph Reachability & Routing:** MST cabling, cycle detection, critical connections (bridges) in network topologies, Dijkstra.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Daily Server Workload Reduction (Max-Heap)
- **College/Drive:** BITS Pilani / IIT Roorkee 2024–2025
- **Problem Summary:** You are given an array of integers `weights` representing daily processing workloads of $N$ server queues, and an integer $K$. Each day, you can select the server queue with the maximum workload and reduce its workload by $\lfloor \text{weight} / 2 \rfloor$. Calculate the minimum total remaining workload across all servers after $K$ days.
- **Constraints:** $1 \le weights.length \le 10^5$, $1 \le K \le 10^5$.
- **LeetCode Equivalent:** [1962. Remove Stones to Minimize the Total](https://leetcode.com/problems/remove-stones-to-minimize-the-total/)
- **Approach:** Max-Heap (`std::priority_queue<int>`). Pop the maximum, divide by 2, push back, repeat $K$ times.
- **Complexity:** $O(N + K \log N)$ Time, $O(N)$ Space.

#### 2. Network Switch Buffer Overflow (Circular Array)
- **College/Drive:** NIT Surathkal / DTU 2024–2025
- **Problem Summary:** A network switch has a buffer of capacity $C$ implemented as a circular buffer. Packets arrive with varying sizes and priority. If an incoming packet causes capacity to be exceeded, lower-priority packets in the buffer are dropped. Simulate $N$ incoming packet events and output the final buffer content.
- **Constraints:** $1 \le N \le 10^5$, $C \le 1000$.
- **Approach:** Deque / Ring buffer with priority-based eviction logic.
- **Complexity:** $O(N)$ Time, $O(C)$ Space.

#### 3. Subarray Sums Divisible by Subnet Size K
- **College/Drive:** IIIT Hyderabad / IIT BHU 2024–2025
- **Problem Summary:** Given an array of packet counts, find the number of non-empty subarrays whose sum is divisible by $K$.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$, $2 \le K \le 10^4$.
- **LeetCode Equivalent:** [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- **Approach:** Running prefix sum modulo $K$. Store remainder counts in hash map / array of size $K$. Add `count[rem]` to total.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 4. Critical Connections in Data Center Topology (Bridges)
- **College/Drive:** IIT Guwahati / NIT Trichy 2024–2025
- **Problem Summary:** In a data center network of $N$ servers, find all single links whose failure would partition the network into disconnected segments.
- **Constraints:** $1 \le N \le 10^5$, $edges \le 10^5$.
- **LeetCode Equivalent:** [1192. Critical Connections in a Network](https://leetcode.com/problems/critical-connections-in-a-network/)
- **Approach:** Tarjan's bridge-finding algorithm using DFS discovery times and low values.
- **Complexity:** $O(V + E)$ Time, $O(V)$ Space.

#### 5. Sliding Window Maximum in Router Ingress Queue
- **College/Drive:** Arista On-Campus 2024–2025
- **Problem Summary:** Given packet sizes passing through a router window of size $K$, output the maximum packet size seen in every sliding window.
- **Constraints:** $1 \le nums.length \le 10^5$, $1 \le K \le nums.length$.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Approach:** Monotonic Decreasing Deque storing indices.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 6. Minimum Cost to Connect All Network Racks (Kruskal's MST)
- **College/Drive:** Campus Slot 1 (2024)
- **Problem Summary:** Connect all $N$ data center racks with minimum cabling cost.
- **Constraints:** $1 \le N \le 1000$.
- **LeetCode Equivalent:** [1584. Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)
- **Approach:** Kruskal's algorithm with Disjoint Set Union (DSU).
- **Complexity:** $O(E \log E)$ Time.

#### 7. IP Packet Header Checksum & String Parsing
- **College/Drive:** Campus Slot 2 (2024)
- **Problem Summary:** Parse raw hexadecimal strings representing packet headers, validate bitwise checksums, and extract source and destination addresses.
- **Constraints:** String length $\le 1000$.
- **Approach:** Convert hex pairs to 16-bit words, compute one's complement sum, and verify final checksum word.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Reverse Bits of a 32-bit Unsigned Integer
- **College/Drive:** Off-Campus Hiring 2024
- **Problem Summary:** Reverse bits of a given 32-bit unsigned integer representing network mask.
- **Constraints:** 32-bit integer.
- **LeetCode Equivalent:** [190. Reverse Bits](https://leetcode.com/problems/reverse-bits/)
- **Approach:** Bitwise shifting: `result = (result << 1) | (n & 1); n >>= 1;` for 32 iterations.
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

#### 9. Course Schedule II (Topology Dependency Resolution)
- **College/Drive:** Campus Hiring 2024
- **Problem Summary:** Find valid configuration sequence of route dependencies.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm for Topological Sort using indegree array.
- **Complexity:** $O(V + E)$ Time.

#### 10. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Find length of longest non-repeating character sequence in network payload string.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Network Delay Time / Packet Routing
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Compute time for packet to reach all nodes from source router.
- **Constraints:** $1 \le N \le 100$, $1 \le edges \le 6000$.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's algorithm with Min-Heap.
- **Complexity:** $O(E \log V)$ Time.

#### 12. Trapping Rain Water
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 13. Subarray Sum Equals K
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Count continuous subarrays summing to $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency counter.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 14. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Minimum minutes to infect all items in 2D grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 15. Daily Temperatures / Metric Spike Monotonic Stack
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Find days to wait for a higher value.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 16. Coin Change (Fewest Coins)
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Minimum coins needed to make change.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 17. Merge Intervals
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Merge all overlapping intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time; merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 18. Product of Array Except Self without Division
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 19. Search in Rotated Sorted Array
- **College/Drive:** Off-Campus 2023
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

## 🧠 Frequent Linux, C & Networking MCQs in Arista OA
1. **Linux Command `kill -9` vs `kill -15`:**
   - `SIGTERM (15)` requests a process to terminate gracefully, allowing cleanup. `SIGKILL (9)` forcefully terminates the process immediately and cannot be caught, blocked, or ignored.
2. **Fastest Linux IPC Mechanism:**
   - Shared Memory (`shmget` / `mmap`), because processes map the same physical memory pages into their address spaces, eliminating kernel-to-user memory copy operations.
3. **Struct Padding & Alignment in C:**
   ```c
   struct Packet {
       char type;      // 1 byte + 3 bytes padding
       int seq_num;    // 4 bytes
       short port;     // 2 bytes + 2 bytes padding
   }; // sizeof(struct Packet) = 12 bytes on 32/64-bit systems
   ```
4. **TCP 3-Way Handshake & SYN Flooding:**
   - What is SYN Flood attack and how do SYN Cookies mitigate it?
   - *Answer:* Attacker floods server with SYN packets without sending final ACK, filling the SYN backlog queue. SYN Cookies encode connection state into the initial sequence number (ISN), avoiding state allocation on server until final ACK arrives.
