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
- **Bit Manipulation & Bitwise Operations:** Bitmasking, reversing bits, counting set bits, bitwise parity, single number variations.
- **Computer Architecture & Caching:** Direct-mapped vs Set-associative caches, cache hit/miss latency, pipeline hazards.
- **C / C++ Pointers & Memory:** Memory alignment, pointer casting, `volatile`, inline assembly, LRU cache simulation.
- **Arrays & Matrix Manipulations:** In-place rotations, spiral matrix, boundary sums, prefix products.
- **Dynamic Programming & Search:** Kadane's algorithm, search in rotated sorted arrays, coin change.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Count Total Set Bits from 1 to N (Mathematical Bit Counting)
- **College/Drive:** IIT Roorkee / BITS Pilani 2024–2025
- **Problem Summary:** Given a positive integer $N$, count the total number of set bits (1s) in the binary representations of all integers from $1$ to $N$.
- **Constraints:** $1 \le N \le 10^9$.
- **Approach:** Mathematical pattern by power of 2: In each bit position $k$ ($2^k$), bits alternate between 0 and 1 in blocks of $2^k$. Full blocks contribute $\lfloor \frac{N+1}{2^{k+1}} \rfloor \times 2^k$, plus remainder contribution.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 2. Cache Replacement Simulation (LRU Cache in C++)
- **College/Drive:** NIT Trichy / DTU 2024–2025
- **Problem Summary:** Implement an LRU (Least Recently Used) cache with `get(key)` and `put(key, value)` operations running in $O(1)$ average time.
- **Constraints:** Capacity up to $3000$, operations up to $10^5$.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Hash Map mapping `key -> Node*` in a Doubly Linked List.
- **Complexity:** $O(1)$ Time per operation, $O(\text{Capacity})$ Space.

#### 3. Bitwise AND of Numbers Range
- **College/Drive:** IIIT Hyderabad 2024–2025
- **Problem Summary:** Given two integers `left` and `right`, return the bitwise AND of all numbers in this inclusive range `[left, right]`.
- **Constraints:** $0 \le left \le right \le 2^{31} - 1$.
- **LeetCode Equivalent:** [201. Bitwise AND of Numbers Range](https://leetcode.com/problems/bitwise-and-of-numbers-range/)
- **Approach:** Find the common binary prefix of `left` and `right` by right-shifting both until they are equal, then shift back left.
- **Complexity:** $O(\log(\text{Range}))$ Time, $O(1)$ Space.

#### 4. Matrix Boundary Traversal & Diagonals
- **College/Drive:** College Campus Drive 2024–2025
- **Problem Summary:** Given an $N \times N$ matrix, calculate the sum of its boundary elements and both major and minor diagonals without double-counting intersections.
- **Constraints:** $1 \le N \le 500$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Reverse Bits of 32-bit Hardware Word
- **College/Drive:** Intel Software Drive 2024–2025
- **Problem Summary:** Reverse bits of a 32-bit unsigned integer.
- **Constraints:** 32-bit integer.
- **LeetCode Equivalent:** [190. Reverse Bits](https://leetcode.com/problems/reverse-bits/)
- **Approach:** Bitwise shifting: `result = (result << 1) | (n & 1); n >>= 1;` for 32 iterations.
- **Complexity:** $O(1)$ Time.

#### 6. Single Number (Bitwise XOR)
- **College/Drive:** Campus Slot 1 (2024)
- **Problem Summary:** Find element appearing once while others appear twice.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [136. Single Number](https://leetcode.com/problems/single-number/)
- **Approach:** XOR all elements together: $x \oplus x = 0$ and $x \oplus 0 = x$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Reverse Linked List
- **College/Drive:** Campus Slot 2 (2024)
- **Problem Summary:** In-place pointer reversal of linked list.
- **Constraints:** Nodes $\le 5000$.
- **LeetCode Equivalent:** [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
- **Approach:** Iterative 3-pointer reversal (`prev`, `curr`, `next`).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Power of Two Verification
- **College/Drive:** Off-Campus 2024
- **Problem Summary:** Check if integer is power of two using bitwise operators.
- **Constraints:** $-2^{31} \le n \le 2^{31} - 1$.
- **LeetCode Equivalent:** [231. Power of Two](https://leetcode.com/problems/power-of-two/)
- **Approach:** `return n > 0 && (n & (n - 1)) == 0;`.
- **Complexity:** $O(1)$ Time.

#### 9. Spiral Matrix Traversal
- **College/Drive:** Campus Hiring 2024
- **Problem Summary:** Clockwise boundary traversal of $M \times N$ matrix.
- **Constraints:** $1 \le M, N \le 100$.
- **LeetCode Equivalent:** [54. Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
- **Approach:** Four boundary pointers (`top`, `bottom`, `left`, `right`) shifting inward.
- **Complexity:** $O(M \times N)$ Time.

#### 10. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Contiguous subarray with largest sum.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Approach:** Kadane's algorithm.
- **Complexity:** $O(N)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Single Number II (Elements Appear Three Times)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Given an integer array `nums` where every element appears three times except for one, find that single element in $O(N)$ time and $O(1)$ space.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [137. Single Number II](https://leetcode.com/problems/single-number-ii/)
- **Approach:** Bitwise sum of bits modulo 3 across all 32 positions or bit-counter state machine (`ones`, `twos`).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Single Number III (Two Elements Appear Once)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Every element appears twice except for two elements which appear once. Find the two elements.
- **Constraints:** $2 \le nums.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [260. Single Number III](https://leetcode.com/problems/single-number-iii/)
- **Approach:** Compute overall XOR sum $X = A \oplus B$. Find lowest set bit in $X$ (`diff = X & (-X)`). Partition elements into two groups based on that bit and XOR independently.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 13. Rotate Image (Matrix 90 Degree Rotation)
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** In-place clockwise 90 degree matrix rotation.
- **Constraints:** $1 \le N \le 100$.
- **LeetCode Equivalent:** [48. Rotate Image](https://leetcode.com/problems/rotate-image/)
- **Approach:** Transpose matrix along diagonal, then reverse rows horizontally.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Space.

#### 14. Search in Rotated Sorted Array
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Find target in rotated sorted array in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 5000$.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking which half is sorted.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 15. Trapping Rain Water
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. Product of Array Except Self without Division
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 17. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Sliding window with hash map storing last seen indices.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

#### 18. House Robber (1D Dynamic Programming)
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Maximize stolen value without robbing two adjacent houses.
- **Constraints:** $1 \le nums.length \le 100$.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** DP: `dp[i] = max(dp[i-1], dp[i-2] + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 19. Coin Change (Fewest Coins)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Minimum coins needed to make change.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 20. Container With Most Water
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Two pointers inward maximizing area between vertical lines.
- **Constraints:** $2 \le heights.length \le 10^5$.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent Computer Architecture & Embedded MCQs in Intel OA
1. **Cache Miss Types (3 Cs):**
   - **Compulsory (Cold start):** First reference to a block.
   - **Capacity:** Cache cannot contain all blocks needed for program execution.
   - **Conflict (Collision):** Multiple blocks compete for the same set in set-associative or direct-mapped caches.
2. **Pipeline Hazards:**
   - **Structural:** Hardware resource conflicts (e.g., single memory port for data and instruction).
   - **Data (RAW, WAR, WAW):** Read-After-Write, Write-After-Read, Write-After-Write data dependencies.
   - **Control:** Branch and jump instructions altering PC before branch outcome is known.
3. **Interrupt Service Routine (ISR):**
   - Why cannot an ISR accept parameters or return a value?
   - *Answer:* Because an ISR is invoked asynchronously by hardware interrupt signals from the CPU interrupt vector table, not by a synchronous software call stack with argument push/pop frames.
4. **`volatile` Keyword in Embedded C:**
   - Why is `volatile` required when reading hardware memory-mapped registers?
   - *Answer:* It informs the compiler that the register value can change asynchronously outside the program's control (e.g., by hardware peripherals), preventing compiler optimizations from caching the register in a CPU register or deleting repeated reads.
