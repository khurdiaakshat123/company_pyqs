# Intel Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 💻

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Coding Section:** 2 Coding Challenges (Medium difficulty, 45 mins) – Focuses on Bit Manipulation, Arrays, Matrix Traversals, and Linked Lists.
  2. **Core CS, Hardware & Embedded MCQs:** 20 to 25 MCQs (45 mins) – Computer Architecture (Cache memory, Pipelining, Instruction cycles), C/C++ Low-level Internals, Microprocessors (8086 / ARM registers), and Operating Systems (Interrupt Service Routines, Virtual Memory).
- **Evaluation Criteria:** High score in the technical/hardware architecture MCQs is mandatory; candidates who ace the coding section but fail the hardware/architecture MCQs are systematically filtered out.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Bit Manipulation & Bitwise Operations | Medium | Bitmasking, reversing bits, counting set bits, bitwise parity |
| **Very High** | Computer Architecture & Caching | Medium | Direct-mapped vs Set-associative caches, cache hit/miss latency, pipeline hazards |
| **High** | C / C++ Pointers & Memory | Medium | Memory alignment, pointer casting, `volatile`, inline assembly |
| **High** | Arrays & Matrix Manipulations | Easy - Medium | In-place rotations, spiral matrix, prefix sums |
| **Medium** | Linked Lists & Trees | Medium | Reversal, cycle detection, lowest common ancestor |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Count Total Set Bits from 1 to N
- **Problem Summary:** Given a positive integer $N$, count the total number of set bits (1s) in the binary representations of all integers from $1$ to $N$.
- **Approach:** Mathematical pattern by power of 2: In each bit position $k$ ($2^k$), bits alternate between 0 and 1 in blocks of $2^k$.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

### 2. Cache Replacement Simulation (LRU Cache)
- **Problem Summary:** Implement an LRU (Least Recently Used) cache with `get(key)` and `put(key, value)` operations running in $O(1)$ average time.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Hash Map mapping `key -> Node*` in a Doubly Linked List.
- **Complexity:** $O(1)$ Time per operation, $O(\text{Capacity})$ Space.

### 3. Bitwise AND of Numbers Range
- **Problem Summary:** Given two integers `left` and `right`, return the bitwise AND of all numbers in this inclusive range `[left, right]`.
- **LeetCode Equivalent:** [201. Bitwise AND of Numbers Range](https://leetcode.com/problems/bitwise-and-of-numbers-range/)
- **Approach:** Find the common binary prefix of `left` and `right` by right-shifting both until they are equal, then shift back left.
- **Complexity:** $O(\log(\text{Range}))$ Time, $O(1)$ Space.

### 4. Matrix Boundary Traversal & Diagonals
- **Problem Summary:** Given an $N \times N$ matrix, calculate the sum of its boundary elements and both major and minor diagonals without double-counting intersections.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent Computer Architecture & Embedded MCQs in Intel OA
1. **Cache Miss Types (3 Cs):**
   - *Compulsory:* First access to a block (cold start).
   - *Capacity:* Cache cannot contain all blocks needed during execution.
   - *Conflict:* Multiple memory blocks map to the same set (in direct-mapped or set-associative caches).
2. **Pipeline Hazards:** What are the three types of pipeline hazards? (Structural, Data [RAW, WAR, WAW], and Control/Branch hazards).
3. **Interrupt Service Routine (ISR):** Why cannot an ISR accept parameters or return a value? (Because it is triggered asynchronously by hardware signals rather than software function calls).
