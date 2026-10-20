# Arista Networks Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🌐

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** (Strictly proctored)
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Systems, C/C++ & Linux MCQs (30 mins)** – Heavy emphasis on C/C++ Pointers, Memory Management (`malloc` vs `calloc`, struct padding), Linux commands (`kill`, `chmod`, `netstat`, `strace`), and OS Networking internals.
  2. **Section 2: Coding Assessment (60 mins, 3 Questions)** – Medium to Hard algorithmic problems. In many rounds, permitted programming languages are restricted strictly to **C, C++, and Java**.
- **Passing Cutoff:** Arista is a high-performance cloud networking company; candidates must clear the Linux/Systems MCQ cutoffs alongside at least 2 complete coding problems.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | C/C++ Memory & Linux MCQs | Medium | Pointer arithmetic, virtual memory, signal handling, socket buffers |
| **Very High** | Heaps & Priority Queues | Medium | Greedy day-by-day weight reductions, stream processing |
| **High** | Array & Matrix Manipulations | Medium | Prefix sums, running totals, transformation matrices |
| **High** | Strings & Alphanumeric Simulation | Medium | Custom parsing, packet grouping rules, delimiter balancing |
| **Medium** | Graph Reachability & Routing | Medium - Hard | Shortest path, cycle detection in network topologies |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Daily Server Workload Reduction (Max-Heap)
- **Problem Summary:** You are given an array of integers `weights` representing daily processing workloads of $N$ server queues, and an integer $K$. Each day, you can select the server queue with the maximum workload and reduce its workload by $\lfloor \text{weight} / 2 \rfloor$. Calculate the minimum total remaining workload across all servers after $K$ days.
- **LeetCode Equivalent:** [1962. Remove Stones to Minimize the Total](https://leetcode.com/problems/remove-stones-to-minimize-the-total/)
- **Approach:** Max-Heap (`std::priority_queue<int>`). Pop the maximum, divide by 2, push back, repeat $K$ times.
- **Complexity:** $O(N + K \log N)$ Time, $O(N)$ Space.

### 2. Network Switch Buffer Overflow (Circular Array)
- **Problem Summary:** A network switch has a buffer of capacity $C$ implemented as a circular buffer. Packets arrive with varying sizes and priority. If an incoming packet causes capacity to be exceeded, lower-priority packets in the buffer are dropped. Simulate $N$ incoming packet events and output the final buffer content.
- **Approach:** Deque / Ring buffer with priority-based eviction logic.
- **Complexity:** $O(N)$ Time, $O(C)$ Space.

### 3. IP Packet Header Checksum & String Parsing
- **Problem Summary:** Parse raw hexadecimal strings representing packet headers, validate bitwise checksums, and extract source and destination addresses.
- **Complexity:** $O(N)$ Time.

### 4. Longest Subarray with Contiguous Sum Divisible by Subnet Mask Size
- **Problem Summary:** Given an array of packet counts, find the maximum length of a subarray whose total packet count is divisible by $K$.
- **LeetCode Equivalent:** [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

---

## 🧠 Frequent Linux & C Systems Questions in Arista OA
1. **Linux Command `kill -9`:** Sends `SIGKILL`, which immediately terminates the process and cannot be caught, blocked, or ignored by the process.
2. **IPC Mechanisms:** What is the fastest inter-process communication mechanism on Linux? (Shared Memory - `shmget` / `mmap`, because data is not copied between user and kernel space).
3. **Pointers to Functions:**
   ```c
   void (*func_ptr)(int, int); // Pointer to function taking two ints and returning void
   ```
