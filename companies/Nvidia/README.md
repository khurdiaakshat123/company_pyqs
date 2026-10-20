# Nvidia Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🟢

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Core CS & C/C++ MCQs** (15 to 25 Questions, 30 mins) – Heavy emphasis on C/C++ Pointers, Memory Alignment, Bitwise Operators, OS (Concurrency, Paging, TLB), and Computer Organization & Architecture (Cache hierarchy, Endianness).
  2. **Section 2: Coding Assessment** (2 to 3 Coding Problems, 45–60 mins) – Medium to Hard difficulty, often featuring Bit Manipulation, Matrix/Grid traversals, and Memory Alignment logic.
- **Cutoff Benchmark:** Nvidia evaluates the low-level systems & C/C++ MCQs with equal (and sometimes higher) priority than algorithmic coding.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Bit Manipulation & Memory Alignment:** Bitmasks, bitwise intervals, memory word alignment, count set bits.
- **C / C++ Internals & Pointers:** Pointer arithmetic, virtual tables (vptr/vtable), memory layout, `volatile`.
- **Operating Systems & Architecture:** TLB hits/misses, page replacement, thread synchronization, pipeline hazards.
- **Arrays, Matrices & Grid Search:** 2D matrix rotations, connected components, sliding window.
- **Graph & Tree Algorithms:** Topological sort, BFS/DFS path validation, LCA.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

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

#### 4. Daily Temperatures / Monotonic Stack
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Summary:** Given an array of temperatures, return an array `answer` such that `answer[i]` is the number of days you have to wait after the $i$-th day to get a warmer temperature.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 5. Search in Rotated Sorted Array
- **College/Drive:** Nvidia Ignite Drive 2024
- **Problem Summary:** Search for target value in circularly shifted sorted array in $O(\log N)$ time.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking which half is strictly sorted.
- **Complexity:** $O(\log N)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Power of Two (Hardware Register Flag)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Check if number is power of two using bitwise arithmetic.
- **LeetCode Equivalent:** [231. Power of Two](https://leetcode.com/problems/power-of-two/)
- **Complexity:** $O(1)$ Time.

#### 7. Number of Islands / GPU Grid Processing
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Count connected components of 1s in binary matrix.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Complexity:** $O(M \times N)$ Time.

#### 8. Binary Tree Right Side View
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Node values visible from right side of tree.
- **LeetCode Equivalent:** [199. Binary Tree Right Side View](https://leetcode.com/problems/binary-tree-right-side-view/)
- **Complexity:** $O(N)$ Time.

#### 9. LRU Cache Implementation (Hardware Cache Simulation)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Design $O(1)$ LRU Cache.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Complexity:** $O(1)$ Time.

#### 10. Trapping Rain Water
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Two pointers water trapping between elevation bars.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time.

---

## 🧠 Frequent C/C++ Systems Questions Asked in Nvidia OA
1. **Structure Padding & Memory Alignment:**
   ```c
   struct Example {
       char a;     // 1 byte + 3 bytes padding
       int b;      // 4 bytes
       short c;    // 2 bytes + 2 bytes padding
   };
   // sizeof(struct Example) == 12 bytes on 32/64-bit systems
   ```
2. **Translation Lookaside Buffer (TLB):** What happens on a TLB miss during virtual-to-physical address translation? (Hardware/Software page table walk, loads translation into TLB, restarts instruction).
3. **Macro Side Effects:**
   ```c
   #define SQUARE(x) (x * x)
   int a = 3;
   int res = SQUARE(a++); // Expands to (a++ * a++), undefined behavior / unexpected output
   ```
