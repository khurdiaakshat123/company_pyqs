# Qualcomm Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 📡

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HirePro** / **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Sections Breakdown:**
  1. **Section 1: Quantitative Aptitude & Logical Reasoning** (~20–25 MCQs, 25 mins)
  2. **Section 2: C Programming & Core CS MCQs** (~20–35 MCQs, 35 mins) – High weightage on pointers, memory management, and bitwise operations.
  3. **Section 3: Coding Section** (1 to 2 Coding Questions, 30 mins) – Focuses on Bit Manipulation, Linked Lists, and Arrays.
- **Negative Marking:** Varies by drive (often -0.25 on MCQs).
- **Cutoff Benchmark:** Qualcomm strictly filters based on the C/Core CS MCQs section; strong coding alone is insufficient if CS fundamentals are low.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Bit Manipulation | Easy - Medium | Bitmasking, counting set bits (Hamming weight), parity, setting/clearing bits |
| **Very High** | C / C++ Pointers & Memory | Medium | Pointer arithmetic, `sizeof` on structs/pointers, `volatile`, storage classes |
| **High** | Linked Lists | Easy - Medium | Cycle detection & length, middle node, reversal, merging sorted lists |
| **High** | Operating Systems & Arch | Medium | Virtual memory, page replacement, mutex vs semaphore, Little vs Big Endian |
| **Medium** | Binary Trees & Graphs | Medium | Tree traversals, diameter, topological sort for hardware dependencies |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Reverse Bits in 32-bit Unsigned Integer
- **Problem Summary:** Reverse the bits of a given 32-bit unsigned integer and return the resulting numerical value.
- **Approach:** Iterate 32 times, shift result left, extract lowest bit with `n & 1`, append with bitwise OR, right shift `n`.
- **LeetCode Equivalent:** [190. Reverse Bits](https://leetcode.com/problems/reverse-bits/)
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

### 2. Swap Odd and Even Bits
- **Problem Summary:** Given an unsigned 32-bit integer, swap all odd bits with adjacent even bits (e.g., bit 0 with bit 1, bit 2 with bit 3).
- **Approach:**
  - Mask even bits with `0xAAAAAAAA` and shift right by 1.
  - Mask odd bits with `0x55555555` and shift left by 1.
  - Bitwise OR both results: `((n & 0xAAAAAAAA) >> 1) | ((n & 0x55555555) << 1)`.
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

### 3. Linked List Cycle Length & Start Node
- **Problem Summary:** Given head of a linked list, determine if a cycle exists. If yes, find the length of the cycle and the node where the cycle begins.
- **LeetCode Equivalent:** [142. Linked List Cycle II](https://leetcode.com/problems/linked-list-cycle-ii/)
- **Approach:** Floyd's Tortoise and Hare algorithm.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 4. Spiral Matrix Order Traversal
- **Problem Summary:** Given an $m \times n$ matrix, return all elements of the matrix in spiral order.
- **LeetCode Equivalent:** [54. Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
- **Complexity:** $O(M \times N)$ Time, $O(1)$ Extra Space.

---

## 🧠 Frequent C & Core CS MCQ Snippets
1. **Pointer Arithmetic Output:**
   ```c
   int arr[] = {10, 20, 30, 40};
   int *p = arr;
   printf("%d\n", *(p++) + *(++p)); // Tests sequence point and precedence
   ```
2. **Volatile Keyword:** Why is `volatile` used in embedded systems?
   - *Answer:* Prevents compiler optimization for memory-mapped I/O registers whose values can change outside the compiler's control (e.g. hardware interrupt).
3. **Endianness:** How to detect system endianness using a C character pointer?
   ```c
   unsigned int x = 1;
   char *c = (char*)&x;
   if (*c) printf("Little Endian");
   else printf("Big Endian");
   ```
