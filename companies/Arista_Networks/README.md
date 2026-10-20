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
- **Graph Reachability & Routing:** MST cabling, cycle detection, critical connections (bridges) in network topologies.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Daily Server Workload Reduction (Max-Heap)
- **College/Drive:** BITS Pilani / IIT Roorkee 2024
- **Problem Summary:** You are given an array of integers `weights` representing daily processing workloads of $N$ server queues, and an integer $K$. Each day, you can select the server queue with the maximum workload and reduce its workload by $\lfloor \text{weight} / 2 \rfloor$. Calculate the minimum total remaining workload across all servers after $K$ days.
- **LeetCode Equivalent:** [1962. Remove Stones to Minimize the Total](https://leetcode.com/problems/remove-stones-to-minimize-the-total/)
- **Approach:** Max-Heap (`std::priority_queue<int>`). Pop the maximum, divide by 2, push back, repeat $K$ times.
- **Complexity:** $O(N + K \log N)$ Time, $O(N)$ Space.

#### 2. Network Switch Buffer Overflow (Circular Array)
- **College/Drive:** NIT Surathkal / DTU 2024
- **Problem Summary:** A network switch has a buffer of capacity $C$ implemented as a circular buffer. Packets arrive with varying sizes and priority. If an incoming packet causes capacity to be exceeded, lower-priority packets in the buffer are dropped. Simulate $N$ incoming packet events and output the final buffer content.
- **Approach:** Deque / Ring buffer with priority-based eviction logic.
- **Complexity:** $O(N)$ Time, $O(C)$ Space.

#### 3. Subarray Sums Divisible by Subnet Size K
- **College/Drive:** IIIT Hyderabad / IIT BHU 2024
- **Problem Summary:** Given an array of packet counts, find the number of non-empty subarrays whose sum is divisible by $K$.
- **LeetCode Equivalent:** [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- **Approach:** Running prefix sum modulo $K$. Store remainder counts in hash map / array of size $K$. Add `count[rem]` to total.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 4. Critical Connections in Data Center Topology (Bridges)
- **College/Drive:** IIT Guwahati / NIT Trichy 2024
- **Problem Summary:** In a data center network of $N$ servers, find all single links whose failure would partition the network into disconnected segments.
- **LeetCode Equivalent:** [1192. Critical Connections in a Network](https://leetcode.com/problems/critical-connections-in-a-network/)
- **Approach:** Tarjan's bridge-finding algorithm using DFS discovery times and low values.
- **Complexity:** $O(V + E)$ Time, $O(V)$ Space.

#### 5. Sliding Window Maximum in Router Ingress Queue
- **College/Drive:** Arista On-Campus 2024
- **Problem Summary:** Given packet sizes passing through a router window of size $K$, output the maximum packet size seen in every sliding window.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Approach:** Monotonic Decreasing Deque storing indices.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Minimum Cost to Connect All Network Racks (Kruskal's MST)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Connect all $N$ data center racks with minimum cabling cost.
- **LeetCode Equivalent:** [1584. Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)
- **Approach:** Kruskal's algorithm with Disjoint Set Union (DSU).
- **Complexity:** $O(E \log E)$ Time.

#### 7. IP Packet Header Checksum & String Parsing
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Parse raw hexadecimal strings representing packet headers, validate bitwise checksums, and extract source and destination addresses.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Reverse Bits of a 32-bit Unsigned Integer
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Reverse bits of a given 32-bit unsigned integer representing network mask.
- **LeetCode Equivalent:** [190. Reverse Bits](https://leetcode.com/problems/reverse-bits/)
- **Approach:** Bitwise shifting: `result = (result << 1) | (n & 1); n >>= 1;` for 32 iterations.
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

#### 9. Course Schedule II (Topology Dependency Resolution)
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Find valid configuration sequence of route dependencies.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm for Topological Sort using indegree array.
- **Complexity:** $O(V + E)$ Time.

#### 10. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Find length of longest non-repeating character sequence in network payload string.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

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
