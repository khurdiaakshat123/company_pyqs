# Nvidia Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🟢

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Core CS & C/C++ MCQs** (15 to 25 Questions, 30 mins) – Heavy emphasis on C/C++ Pointers, Memory Alignment, Bitwise Operators, OS (Concurrency, Paging, TLB), and Computer Architecture (Cache hierarchy, Endianness).
  2. **Section 2: Coding Assessment** (2 to 3 Coding Problems, 45–60 mins) – Medium to Hard difficulty, often featuring Bit Manipulation, Matrix/Grid traversals, and Memory Alignment logic.
- **Cutoff Benchmark:** Nvidia evaluates the low-level systems & C/C++ MCQs with equal (and sometimes higher) priority than algorithmic coding.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Bit Manipulation & Bitwise Ranges | Medium - Hard | Bitmasks, bitwise intervals, memory word alignment, count set bits |
| **Very High** | C / C++ Internals & Pointers | Medium | Pointer arithmetic, virtual tables (vptr/vtable), memory layout, `volatile` |
| **High** | Operating Systems & Architecture | Medium | TLB hits/misses, page replacement, thread synchronization, pipeline hazards |
| **High** | Arrays, Matrices & Grid Search | Medium | 2D matrix rotations, connected components, sliding window |
| **Medium** | Graph & Tree Algorithms | Medium | Topological sort, BFS/DFS path validation, LCA |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Memory Address Alignment & Padding Calculation
- **Problem Summary:** Given a stream of memory allocation requests with specified byte sizes and alignment constraints (e.g., 4-byte, 8-byte, 16-byte boundaries), compute the total padded memory consumed and final memory layout.
- **Approach:** Bitwise alignment formula: $\text{aligned\_addr} = (addr + align - 1) \& \sim(align - 1)$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 2. Maximum Subarray XOR with Bounded Length
- **Problem Summary:** Given an array of integers $A$ and an integer $K$, find the maximum XOR sum of any contiguous subarray of length at most $K$.
- **Approach:** Prefix XOR array inserted into a **Trie with sliding window** (insert prefix XOR $i$, query maximum XOR, evict prefix XOR $i-K$ from Trie).
- **Complexity:** $O(N \times 32)$ Time, $O(N \times 32)$ Space.

### 3. Rotate Image / Matrix Transpose in Place
- **Problem Summary:** You are given an $n \times n$ 2D matrix representing an image, rotate the image by 90 degrees (clockwise) in-place without allocating another 2D matrix.
- **LeetCode Equivalent:** [48. Rotate Image](https://leetcode.com/problems/rotate-image/)
- **Approach:** Transpose the matrix (`swap(matrix[i][j], matrix[j][i])`), then reverse each individual row.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Extra Space.

### 4. Daily Temperatures / Monotonic Stack
- **Problem Summary:** Given an array of temperatures, return an array `answer` such that `answer[i]` is the number of days you have to wait after the $i$-th day to get a warmer temperature.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

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
