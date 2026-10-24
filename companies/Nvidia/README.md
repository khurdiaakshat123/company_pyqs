# Nvidia Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🟢

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Core CS & C/C++ MCQs** (15 to 25 Questions, 30 mins) – Heavy emphasis on C/C++ Pointers, Memory Alignment, Bitwise Operators, OS (Concurrency, Paging, TLB), and Computer Organization & Architecture (Cache hierarchy, Endianness, Pipelining).
  2. **Section 2: Coding Assessment** (2 to 3 Coding Problems, 45–60 mins) – Medium to Hard difficulty, often featuring Bit Manipulation, Matrix/Grid traversals, and Memory Alignment logic.
- **Cutoff Benchmark:** Nvidia evaluates the low-level systems & C/C++ MCQs with equal (and sometimes higher) priority than algorithmic coding.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Bit Manipulation & Memory Alignment:** Bitmasks, bitwise intervals, memory word alignment, count set bits, prefix XOR.
- **C / C++ Internals & Pointers:** Pointer arithmetic, virtual tables (vptr/vtable), memory layout, `volatile`, operator evaluation.
- **Operating Systems & Architecture:** TLB hits/misses, page replacement, thread synchronization, pipeline hazards, Little vs Big Endian.
- **Arrays, Matrices & Grid Search:** 2D matrix rotations, connected components, sliding window, prefix XOR arrays.
- **Advanced Trees & Trie:** Tree serialization, duplicate folder pruning, binary prefix tries.

---

## 📝 Verified Multi-Year OA Question Bank (Past 3 Years)
*Every problem listed below is a distinct, verified question sourced from 2023, 2024, and 2025/2026 campus placement drives (IITs, NITs, BITS, DTU) and off-campus Nvidia technical assessments. Duplicates across college slots have been strictly merged.*

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Memory Address Alignment & Padding Calculation (Nvidia Classic)
- **College/Drive:** IIT Bombay / IIT Madras 2024
- **Problem Summary:** Given a stream of memory allocation requests with specified byte sizes and alignment constraints (e.g., 4-byte, 8-byte, 16-byte boundaries), compute the total padded memory consumed and final memory layout.
- **Approach:** Bitwise alignment formula: $\text{aligned\_addr} = (addr + align - 1) \& \sim(align - 1)$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Maximum Subarray XOR with Bounded Length (Trie)
- **College/Drive:** BITS Pilani / IIT Roorkee 2024
- **Problem Summary:** Given an array of integers $A$ and an integer $K$, find the maximum XOR sum of any contiguous subarray of length at most $K$.
- **Approach:** Prefix XOR array inserted into a **Trie with sliding window** (insert prefix XOR $i$, query maximum XOR, evict prefix XOR $i-K$ from Trie).
- **Complexity:** $O(N \times 32)$ Time, $O(N \times 32)$ Space.

#### 3. Rotate Image / Matrix Transpose in Place
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Summary:** You are given an $n \times n$ 2D matrix representing an image, rotate the image by 90 degrees (clockwise) in-place without allocating another 2D matrix.
- **LeetCode Equivalent:** [48. Rotate Image](https://leetcode.com/problems/rotate-image/)
- **Approach:** Transpose the matrix (`swap(matrix[i][j], matrix[j][i])`), then reverse each individual row.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Extra Space.

#### 4. Find the Original Array of Prefix XOR
- **College/Drive:** Nvidia SDE Campus Drive 2024
- **Problem Summary:** You are given an integer array `pref` of size $n$ where `pref[i] = arr[0] ^ arr[1] ^ ... ^ arr[i]`. Find and return the original array `arr`.
- **LeetCode Equivalent:** [2433. Find The Original Array of Prefix Xor](https://leetcode.com/problems/find-the-original-array-of-prefix-xor/)
- **Approach:** Since $P_i = P_{i-1} \oplus A_i$, by XOR properties $A_i = P_{i-1} \oplus P_i$ for $i > 0$, and $A_0 = P_0$.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 5. Daily Temperatures / Monotonic Stack
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Summary:** Given an array of temperatures, return an array `answer` such that `answer[i]` is the number of days you have to wait after the $i$-th day to get a warmer temperature.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 6. Range Bit-Flipping / Range Inversion
- **College/Drive:** Nvidia GPU Firmware Slot 2024
- **Problem Summary:** Given an unsigned 32-bit integer $N$ and two bit indices $L$ and $R$ ($0 \le L \le R \le 31$), invert (flip) all bits between positions $L$ and $R$ inclusive while leaving all other bits unchanged.
- **Approach:** Create a bitmask with 1s from position $L$ to $R$: `mask = ((1ULL << (R - L + 1)) - 1) << L`. Bitwise XOR with $N$: `N ^ mask`.
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

#### 7. Partition Array Into Two Arrays to Minimize Sum Difference
- **College/Drive:** IIT Delhi / BITS Pilani 2024
- **Problem Summary:** Given an array `nums` of $2N$ integers ($N \le 15$), split it into two arrays of length $N$ such that the absolute difference between their sums is minimized.
- **LeetCode Equivalent:** [2035. Partition Array Into Two Arrays to Minimize Sum Difference](https://leetcode.com/problems/partition-array-into-two-arrays-to-minimize-sum-difference/)
- **Approach:** Meet-in-the-middle: split into two halves of size $N$. For each half, generate subset sums grouped by number of elements chosen. Use binary search (`std::lower_bound`) to find closest matching sum in the second half.
- **Complexity:** $O(N \cdot 2^N)$ Time, $O(2^N)$ Space.

#### 8. Delete Duplicate Folders in System (Tree Serialization)
- **College/Drive:** Nvidia Advanced Software Slot 2024
- **Problem Summary:** Given a 2D array `paths` representing a file system hierarchy, delete all duplicate sub-trees (folders that have identical subfolder structures and names). Return the remaining valid paths.
- **LeetCode Equivalent:** [1948. Delete Duplicate Folders in System](https://leetcode.com/problems/delete-duplicate-folders-in-system/)
- **Approach:** Construct a Trie representing folder hierarchy. Perform post-order traversal to compute serialized representation of each subtree. Store counts in a Hash Map. Mark folders with count $> 1$ for deletion.
- **Complexity:** $O(N \cdot L)$ Time where $N$ is total paths and $L$ is max path length.

#### 9. Check if Number is Power of Two
- **College/Drive:** Nvidia Screening 2024
- **Problem Summary:** Return true if integer $N$ is a power of two without loops or floating-point conversions.
- **LeetCode Equivalent:** [231. Power of Two](https://leetcode.com/problems/power-of-two/)
- **Approach:** `n > 0 && (n & (n - 1)) == 0`.
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

#### 10. Search in Rotated Sorted Array
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Search target element in a sorted rotated array in $O(\log N)$ time.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search determining which half of the array is sorted.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. LRU Cache Implementation for Hardware Cache
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Implement $O(1)$ LRU Cache eviction with hash map and doubly linked list.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Complexity:** $O(1)$ Time per op.

#### 12. Number of Islands (2D Grid BFS/DFS)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Count connected components of land in binary matrix.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 13. Detect Architecture Endianness at Runtime
- **College/Drive:** Systems Round 2023
- **Problem Summary:** Write a C function checking if the current system architecture is Little Endian or Big Endian.
- **Code Solution:**
  ```c
  int check_endianness() {
      unsigned int x = 0x76543210;
      char *c = (char*)&x;
      return (*c == 0x10); // True if Little Endian
  }
  ```
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

#### 14. Course Schedule II (Hardware Dependency DAG)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find valid execution order for hardware module initialization.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Complexity:** $O(V + E)$ Time.

#### 15. Maximum XOR of Two Numbers in an Array
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Find maximum XOR pair among array elements in $O(32 \cdot N)$ time.
- **LeetCode Equivalent:** [421. Maximum XOR of Two Numbers in an Array](https://leetcode.com/problems/maximum-xor-of-two-numbers-in-an-array/)
- **Complexity:** $O(32 \cdot N)$ Time, $O(32 \cdot N)$ Space.

#### 16. Lowest Common Ancestor of a Binary Tree
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Find lowest common ancestor node in binary tree.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 17. Trapping Rain Water
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Compute amount of trapped water between elevation map bars after rain.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 18. Word Search II (Trie + 2D Backtracking)
- **College/Drive:** Advanced SWE Slot 2023
- **Problem Summary:** Find all words from dictionary present in 2D character board.
- **LeetCode Equivalent:** [212. Word Search II](https://leetcode.com/problems/word-search-ii/)
- **Approach:** Prefix Trie built from dictionary words + DFS with visited backtracking.
- **Complexity:** $O(M \times N \times 4^L)$ Time.

#### 19. Two Sum (Hardware Hash Table Lookup)
- **College/Drive:** Campus Slot 3 (2023)
- **Problem Summary:** Return indices of two numbers adding to target in single pass.
- **LeetCode Equivalent:** [1. Two Sum](https://leetcode.com/problems/two-sum/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 20. Struct Padding & Memory Alignment Calculator
- **College/Drive:** Nvidia Embedded OA 2023
- **Problem Summary:** Calculate memory layout and size in bytes for complex nested structures with 32-bit and 64-bit alignment constraints.
- **Complexity:** $O(1)$ Time.

---

## 🧠 Frequent C++ & Systems MCQs in Nvidia OA
1. **Cache Coherence Protocols (MESI):**
   - What are the four states of the MESI cache coherence protocol?
   - *Answer:* Modified (cache line present only in this cache and dirty), Exclusive (present only in this cache and clean), Shared (present in multiple caches and clean), Invalid (data in cache line is stale).
2. **Translation Lookaside Buffer (TLB) Reach:**
   - What is TLB reach and how do Huge Pages increase it?
   - *Answer:* TLB reach is the total amount of memory that can be accessed without incurring a TLB miss: $\text{TLB Reach} = \text{Number of TLB Entries} \times \text{Page Size}$. Huge pages (e.g., 2MB or 1GB instead of standard 4KB) dramatically expand TLB reach, reducing TLB miss latency in compute-intensive GPU workloads.
3. **Pointers to Multi-Dimensional Arrays in C:**
   - How does `int (*arr)[10]` differ from `int *arr[10]`?
   - *Answer:* `int (*arr)[10]` is a pointer to an array of 10 integers (takes 4 or 8 bytes for one pointer). `int *arr[10]` is an array of 10 integer pointers (takes $10 \times 4$ or $10 \times 8$ bytes).
