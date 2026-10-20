# Intel Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💻

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Coding Section:** 2 Coding Challenges (Medium difficulty, 45 mins) – Focuses on Bit Manipulation, Arrays, Matrix Traversals, and Linked Lists.
  2. **Core CS, Hardware & Embedded MCQs:** 20 to 25 MCQs (45 mins) – Computer Architecture (Cache memory, Pipelining, Instruction cycles), C/C++ Low-level Internals, Microprocessors (8086 / ARM registers), and Operating Systems (Interrupt Service Routines, Virtual Memory).
- **Evaluation Criteria:** High score in the technical/hardware architecture MCQs is mandatory; candidates who ace the coding section but fail the hardware/architecture MCQs are systematically filtered out.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Bit Manipulation & Bitwise Operations:** Bitmasking, reversing bits, counting set bits, bitwise parity.
- **Computer Architecture & Caching:** Direct-mapped vs Set-associative caches, cache hit/miss latency, pipeline hazards.
- **C / C++ Pointers & Memory:** Memory alignment, pointer casting, `volatile`, inline assembly.
- **Arrays & Matrix Manipulations:** In-place rotations, spiral matrix, prefix sums.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Count Total Set Bits from 1 to N (Mathematical Bit Counting)
- **College/Drive:** IIT Roorkee / BITS Pilani 2024
- **Problem Summary:** Given a positive integer $N$, count the total number of set bits (1s) in the binary representations of all integers from $1$ to $N$.
- **Approach:** Mathematical pattern by power of 2: In each bit position $k$ ($2^k$), bits alternate between 0 and 1 in blocks of $2^k$.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 2. Cache Replacement Simulation (LRU Cache in C++)
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Summary:** Implement an LRU (Least Recently Used) cache with `get(key)` and `put(key, value)` operations running in $O(1)$ average time.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Hash Map mapping `key -> Node*` in a Doubly Linked List.
- **Complexity:** $O(1)$ Time per operation, $O(\text{Capacity})$ Space.

#### 3. Bitwise AND of Numbers Range
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Summary:** Given two integers `left` and `right`, return the bitwise AND of all numbers in this inclusive range `[left, right]`.
- **LeetCode Equivalent:** [201. Bitwise AND of Numbers Range](https://leetcode.com/problems/bitwise-and-of-numbers-range/)
- **Approach:** Find the common binary prefix of `left` and `right` by right-shifting both until they are equal, then shift back left.
- **Complexity:** $O(\log(\text{Range}))$ Time, $O(1)$ Space.

#### 4. Matrix Boundary Traversal & Diagonals
- **College/Drive:** College Campus Drive 2024
- **Problem Summary:** Given an $N \times N$ matrix, calculate the sum of its boundary elements and both major and minor diagonals without double-counting intersections.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Reverse Bits of 32-bit Hardware Word
- **College/Drive:** Intel Software Drive 2024
- **Problem Summary:** Reverse bits of a 32-bit unsigned integer.
- **LeetCode Equivalent:** [190. Reverse Bits](https://leetcode.com/problems/reverse-bits/)
- **Complexity:** $O(1)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Single Number (Bitwise XOR)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Find element appearing once while others appear twice.
- **LeetCode Equivalent:** [136. Single Number](https://leetcode.com/problems/single-number/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Reverse Linked List
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** In-place pointer reversal of linked list.
- **LeetCode Equivalent:** [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
- **Complexity:** $O(N)$ Time.

#### 8. Power of Two Verification
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** `return n > 0 && (n & (n - 1)) == 0`.
- **LeetCode Equivalent:** [231. Power of Two](https://leetcode.com/problems/power-of-two/)
- **Complexity:** $O(1)$ Time.

#### 9. Spiral Matrix Traversal
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Clockwise boundary traversal of $M \times N$ matrix.
- **LeetCode Equivalent:** [54. Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
- **Complexity:** $O(M \times N)$ Time.

#### 10. Maximum Subarray Sum (Kadane's)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Contiguous subarray with largest sum.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time.

---

## 🧠 Frequent Computer Architecture & Embedded MCQs in Intel OA
1. **Cache Miss Types (3 Cs):** Compulsory (cold start), Capacity, Conflict.
2. **Pipeline Hazards:** Structural, Data (RAW, WAR, WAW), Control/Branch.
3. **Interrupt Service Routine (ISR):** Why cannot an ISR accept parameters or return a value? (Because it is triggered asynchronously by hardware signals rather than software function calls).
