# Qualcomm Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 📡

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

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Bit Manipulation:** Bitmasking, counting set bits (Hamming weight), parity, setting/clearing bits.
- **C / C++ Pointers & Memory:** Pointer arithmetic, `sizeof` on structs/pointers, `volatile`, storage classes.
- **Linked Lists:** Cycle detection & length, middle node, reversal, merging sorted lists.
- **Operating Systems & Architecture:** Virtual memory, page replacement, mutex vs semaphore, Little vs Big Endian.
- **Binary Trees & Graphs:** Tree traversals, diameter, topological sort for hardware dependencies.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Reverse Bits in 32-bit Unsigned Integer
- **College/Drive:** IIT Madras / NIT Trichy 2024
- **Problem Summary:** Reverse the bits of a given 32-bit unsigned integer and return the resulting numerical value.
- **LeetCode Equivalent:** [190. Reverse Bits](https://leetcode.com/problems/reverse-bits/)
- **Approach:** Iterate 32 times, shift result left, extract lowest bit with `n & 1`, append with bitwise OR, right shift `n`.
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

#### 2. Swap Odd and Even Bits in Hardware Register
- **College/Drive:** BITS Pilani / NIT Surathkal 2024
- **Problem Summary:** Given an unsigned 32-bit integer, swap all odd bits with adjacent even bits (e.g., bit 0 with bit 1, bit 2 with bit 3).
- **Approach:**
  - Mask even bits with `0xAAAAAAAA` and shift right by 1.
  - Mask odd bits with `0x55555555` and shift left by 1.
  - Bitwise OR both results: `((n & 0xAAAAAAAA) >> 1) | ((n & 0x55555555) << 1)`.
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

#### 3. Linked List Cycle Length & Start Node
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** Given head of a linked list, determine if a cycle exists. If yes, find the length of the cycle and the node where the cycle begins.
- **LeetCode Equivalent:** [142. Linked List Cycle II](https://leetcode.com/problems/linked-list-cycle-ii/)
- **Approach:** Floyd's Tortoise and Hare algorithm.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Spiral Matrix Order Traversal
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Summary:** Given an $m \times n$ matrix, return all elements of the matrix in spiral order.
- **LeetCode Equivalent:** [54. Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
- **Complexity:** $O(M \times N)$ Time, $O(1)$ Extra Space.

#### 5. Power of Two Verification without Loops
- **College/Drive:** College Pool Campus 2024
- **Problem Summary:** Given integer $N$, return `true` if it is a power of two using a single bitwise operation.
- **LeetCode Equivalent:** [231. Power of Two](https://leetcode.com/problems/power-of-two/)
- **Approach:** `return n > 0 && (n & (n - 1)) == 0`.
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Single Number (Find Non-Duplicate)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Every element appears twice except for one. Find that single one in linear time and $O(1)$ space.
- **LeetCode Equivalent:** [136. Single Number](https://leetcode.com/problems/single-number/)
- **Approach:** Bitwise XOR all elements.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Diameter of Binary Tree
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Find length of longest path between any two nodes in a tree.
- **LeetCode Equivalent:** [543. Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 8. Sort Colors / Dutch National Flag (3 State Registers)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Sort array of 0s, 1s, and 2s in-place in one pass.
- **LeetCode Equivalent:** [75. Sort Colors](https://leetcode.com/problems/sort-colors/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Merge Two Sorted Lists (Embedded Memory Blocks)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Merge two sorted linked lists into one.
- **LeetCode Equivalent:** [21. Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
- **Complexity:** $O(N + M)$ Time.

#### 10. Number of 1 Bits (Hamming Weight)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Write a function that takes the binary representation of a positive integer and returns the number of set bits.
- **LeetCode Equivalent:** [191. Number of 1 Bits](https://leetcode.com/problems/number-of-1-bits/)
- **Approach:** Brian Kernighan's algorithm `n = n & (n - 1)`.
- **Complexity:** $O(\text{set bits})$ Time.

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
