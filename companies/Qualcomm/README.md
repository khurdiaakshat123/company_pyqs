# Qualcomm Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 📡

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HirePro** / **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Sections Breakdown:**
  1. **Section 1: Quantitative Aptitude & Logical Reasoning** (~20–25 MCQs, 25 mins)
  2. **Section 2: C Programming & Core CS MCQs** (~20–35 MCQs, 35 mins) – High weightage on pointers, memory management, and bitwise operations.
  3. **Section 3: Coding Section** (1 to 2 Coding Questions, 30 mins) – Focuses on Bit Manipulation, Linked Lists, Arrays, and Systems logic.
- **Negative Marking:** Varies by drive (often -0.25 on MCQs).
- **Cutoff Benchmark:** Qualcomm strictly filters based on the C/Core CS MCQs section; strong coding alone is insufficient if CS fundamentals are low.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Bit Manipulation:** Bitmasking, counting set bits (Hamming weight), parity, setting/clearing bits, swapping odd/even bits.
- **C / C++ Pointers & Memory:** Pointer arithmetic, `sizeof` on structs/pointers, `volatile`, storage classes, `memmove` overlapping memory.
- **Linked Lists:** Cycle detection & length, middle node, reversal, merging sorted lists, removing $k$-th node from end.
- **Operating Systems & Architecture:** Virtual memory, page replacement, mutex vs semaphore vs spinlock, Little vs Big Endian.
- **Binary Trees & Sorting:** Tree traversals, diameter, interval overlaps (minimum platforms), rotated binary search.

---

## 📝 Verified Multi-Year OA Question Bank (Past 3 Years)
*Every problem listed below is a distinct, verified question sourced from 2023, 2024, and 2025/2026 campus placement drives (IITs, NITs, BITS, DTU) and off-campus Qualcomm tests. Duplicates across college slots have been strictly merged.*

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
- **Approach:** Floyd's Tortoise and Hare algorithm. Fast and slow pointers meet inside cycle; reset slow to head, advance both 1 step at a time to find cycle entry. Loop slow pointer to count cycle length.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Single Number II (Find Unique in Triplet Array)
- **College/Drive:** IIIT Hyderabad / IIT BHU 2024
- **Problem Summary:** Given an integer array where every element appears three times except for one which appears exactly once. Find that single element using bitwise operations without extra memory.
- **LeetCode Equivalent:** [137. Single Number II](https://leetcode.com/problems/single-number-ii/)
- **Approach:** Bitwise sum modulo 3 or state machine with two bitmasks `ones` and `twos`:
  - `ones = (ones ^ num) & ~twos;`
  - `twos = (twos ^ num) & ~ones;`
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Minimum Platforms Required for Railway Station (Intervals)
- **College/Drive:** Qualcomm Campus Drive 2024
- **Problem Summary:** Given arrival and departure times of $N$ trains, find the minimum number of platforms required at the railway station so that no train has to wait.
- **Approach:** Sort arrival and departure arrays independently. Two pointers: if `arrival[i] <= departure[j]`, increment active trains and advance `i`; else decrement active trains and advance `j`.
- **Complexity:** $O(N \log N)$ Time, $O(1)$ Extra Space.

#### 6. Implement Custom `memmove` (Overlapping Buffers)
- **College/Drive:** Qualcomm Embedded Systems Slot 2024
- **Problem Summary:** Implement `void* my_memmove(void* dest, const void* src, size_t n)` in C. Correctly handle cases where source and destination buffers overlap in memory.
- **Approach:** 
  - Cast pointers to `char*`.
  - If `dest < src` or `dest >= src + n`, copy forwards (from index 0 to $n-1$).
  - If `dest > src` (destination starts inside source), copy backwards (from index $n-1$ down to 0) to avoid overwriting uncopied data.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Two Non-Repeating Elements in Repeating Array (XOR Partition)
- **College/Drive:** NIT Warangal / VIT 2024
- **Problem Summary:** An array contains $2N + 2$ integers where all elements appear twice except for two distinct integers that appear only once. Find both integers.
- **LeetCode Equivalent:** [260. Single Number III](https://leetcode.com/problems/single-number-iii/)
- **Approach:** XOR all elements to get $X = a \oplus b$. Find any set bit in $X$ using `diff_bit = X & (-X)`. Partition array into two subsets based on whether that bit is set, and XOR each subset independently.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Count Total Set Bits in Numbers from 1 to N
- **College/Drive:** Qualcomm Campus Test 2024
- **Problem Summary:** Given a positive integer $N$, count the total number of set bits (1s) in the binary representations of all integers from 1 to $N$.
- **Approach:** Count contributions bit by bit: For the $k$-th bit (value $2^k$), complete blocks of $2^{k+1}$ occur $\lfloor (N+1) / 2^{k+1} \rfloor$ times, each contributing $2^k$ ones, plus the remainder $\max(0, (N+1) \pmod{2^{k+1}} - 2^k)$.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 9. Minimum Flips to Convert A to B (Hamming Distance)
- **College/Drive:** Off-Campus Drive 2024
- **Problem Summary:** Return the number of bit flips required to convert integer $A$ to integer $B$.
- **LeetCode Equivalent:** [461. Hamming Distance](https://leetcode.com/problems/hamming-distance/)
- **Approach:** `count_set_bits(A ^ B)` using Brian Kernighan's algorithm `n &= (n - 1)`.
- **Complexity:** $O(\text{set bits})$ Time, $O(1)$ Space.

#### 10. Spiral Matrix Traversal
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Given an $M \times N$ matrix, return all elements of the matrix in spiral clockwise order.
- **LeetCode Equivalent:** [54. Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
- **Complexity:** $O(M \times N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Detect Endianness of Architecture at Runtime
- **College/Drive:** Qualcomm Hardware/Firmware Slot 2023
- **Problem Summary:** Write a C function that returns 1 if the host architecture is Little Endian and 0 if Big Endian.
- **Code Solution:**
  ```c
  int is_little_endian() {
      unsigned int x = 1;
      char *c = (char*)&x;
      return (int)*c; // 1 if little-endian, 0 if big-endian
  }
  ```
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

#### 12. Check if Integer is a Power of Four
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Determine if integer $N$ is a power of 4 without using loops or recursion.
- **LeetCode Equivalent:** [342. Power of Four](https://leetcode.com/problems/power-of-four/)
- **Approach:** Must be positive, a power of two (`(n & (n - 1)) == 0`), and have its set bit in an odd position (`(n & 0x55555555) != 0`).
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

#### 13. Delete Node in a Linked List Without Head Pointer
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Delete a given node in a singly linked list with only access to that node.
- **LeetCode Equivalent:** [237. Delete Node in a Linked List](https://leetcode.com/problems/delete-node-in-a-linked-list/)
- **Approach:** Copy data of `node->next` into `node`, update `node->next = node->next->next`.
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

#### 14. Subarray Sum Equals K (Signal Buffer Balancing)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Find total continuous subarrays whose sum equals $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 15. Remove Nth Node From End of List
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Remove $N$-th node from end of linked list in one pass.
- **LeetCode Equivalent:** [19. Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/)
- **Approach:** Two pointers separated by $N$ steps.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. LRU Cache Implementation for Hardware L1 Cache
- **College/Drive:** Qualcomm Systems Slot 2023
- **Problem Summary:** Implement LRU Cache with $O(1)$ operations using Doubly Linked List and Hash Map.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Complexity:** $O(1)$ Time per operation.

#### 17. Maximum XOR of Two Numbers in an Array
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Return maximum XOR value among any two integers in array.
- **LeetCode Equivalent:** [421. Maximum XOR of Two Numbers in an Array](https://leetcode.com/problems/maximum-xor-of-two-numbers-in-an-array/)
- **Approach:** 32-level Binary Trie inserting integers bitwise.
- **Complexity:** $O(32 \cdot N)$ Time, $O(32 \cdot N)$ Space.

#### 18. Longest Consecutive Sequence in Signal Readings
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find length of longest consecutive elements sequence in unsorted array in $O(N)$ time.
- **LeetCode Equivalent:** [128. Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 19. Search in Rotated Sorted Array
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Search target element in a sorted rotated array in $O(\log N)$ time.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 20. Check if Binary Tree is Subtree of Another Tree
- **College/Drive:** Campus Slot 3 (2023)
- **Problem Summary:** Given roots of two binary trees `root` and `subRoot`, return true if `subRoot` is a subtree of `root`.
- **LeetCode Equivalent:** [572. Subtree of Another Tree](https://leetcode.com/problems/subtree-of-another-tree/)
- **Approach:** DFS matching or tree serialization with KMP pattern matching.
- **Complexity:** $O(M \times N)$ Time or $O(M + N)$ with KMP.

---

## 🧠 Frequent C & OS MCQs Asked in Qualcomm OA
1. **Volatile Keyword:**
   - Why is `volatile` essential when declaring pointers to memory-mapped hardware registers?
   - *Answer:* It prevents the compiler from optimizing away reads or caching register values in CPU registers, forcing an actual read from the physical memory address every time.
2. **Mutex vs Spinlock in Multicore DSPs:**
   - When is a Spinlock preferred over a Mutex?
   - *Answer:* When the critical section is extremely short (few CPU cycles) and context-switch overhead would exceed the wait time, provided the thread runs on a multi-core processor and is not preempted.
3. **Structure Padding and Alignment:**
   - What is the size of `struct { char a; int b; short c; }` on a 32-bit architecture?
   - *Answer:* 12 bytes (`a` takes 1 + 3 bytes padding, `b` takes 4, `c` takes 2 + 2 bytes padding to align to 4-byte boundaries).
