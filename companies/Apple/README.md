# Apple Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🍎

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **CodeSignal** / **CoderPad**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  - **Coding Section:** 2 to 3 Coding Problems (Easy-Medium to Medium-Hard).
  - **Core CS Section:** 10 to 15 MCQs covering Operating Systems (Processes, Threads, Semaphores), Computer Networks (TCP/UDP, DNS), and C++ / Swift memory management (Automatic Reference Counting - ARC).
- **Evaluation Criteria:** Apple places extreme emphasis on clean, idiomatic code, handling edge cases, and algorithmic efficiency. On CodeSignal, strict test-case coverage determines the candidate's invitation to team interviews.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Strings & Text Parsing:** Substring matching, custom compression, balanced delimiters, log reordering.
- **Arrays & Sliding Window:** Minimum operations to reduce $X$ to 0, product of array except self, two pointers.
- **Trees & Graph Traversal:** BFS / DFS, Tree vertical order/level sums, connected components, peak element search.
- **Dynamic Programming:** Knapsack variants, word break, matrix minimum path sums.
- **System & Low-Level Concepts:** Memory layouts, reference counting / ARC (Automatic Reference Counting), concurrency locks.

---

## 📝 Verified Multi-Year OA Question Bank (Past 3 Years)
*Every problem listed below is a distinct, verified question sourced from 2023, 2024, and 2025/2026 campus placement drives (IITs, NITs, BITS, DTU) and off-campus Apple screening assessments. Duplicates across college slots have been strictly merged.*

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Minimum Operations to Reduce X to Zero (Longest Subarray Inversion)
- **College/Drive:** IIT Roorkee / IIT Madras 2024
- **Problem Summary:** Given an array of integers `nums` and an integer `x`. In one operation, you can remove either the leftmost or the rightmost element from the array and subtract its value from `x`. Return the minimum number of operations to reduce `x` to exactly `0`, or `-1` if impossible.
- **LeetCode Equivalent:** [1658. Minimum Operations to Reduce X to Zero](https://leetcode.com/problems/minimum-operations-to-reduce-x-to-zero/)
- **Approach:** Invert the problem: Find the longest contiguous subarray whose sum equals $\sum nums - x$ using a sliding window.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Word Break & Dictionary Segment Matching
- **College/Drive:** BITS Pilani / NIT Trichy 2024
- **Problem Summary:** Given a string $s$ and a dictionary of strings `wordDict`, return `true` if $s$ can be segmented into a space-separated sequence of one or more dictionary words.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Approach:** 1D Dynamic Programming: `dp[i]` is true if a valid prefix exists such that `dp[j]` is true and $s[j \dots i]$ is in the dictionary (or using a Trie).
- **Complexity:** $O(N^2)$ Time, $O(N)$ Space.

#### 3. Maximum Number of Events That Can Be Attended (Min-Heap)
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** You are given an array of `events` where `events[i] = [startDay, endDay]`. You can attend at most one event on any given day. Return the maximum number of events you can attend.
- **LeetCode Equivalent:** [1353. Maximum Number of Events That Can Be Attended](https://leetcode.com/problems/maximum-number-of-events-that-can-be-attended/)
- **Approach:** Sort events by start day, maintain a Min-Heap of end days for active events, and greedily attend the event ending earliest each day.
- **Complexity:** $O(D + N \log N)$ where $D$ is max days.

#### 4. Tree Vertical Level Sum
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Summary:** Given a binary tree, return the vertical sum of all nodes lying on the same vertical line (assigning root coordinate 0, left child -1, right child +1).
- **Approach:** BFS or DFS tracking horizontal distance `hd`. Accumulate node values in a Hash Map `map[hd] += node->val`.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 5. 2D Coordinate Grid Path Following / Maze Simulation
- **College/Drive:** Apple IS&T Software OA 2024
- **Problem Summary:** A robot traverses a 2D coordinate grid with directional instruction arrows (`'^'`, `'v'`, `'<'`, `'>'`). Simulate path execution until the robot either exits the grid boundary or enters an infinite periodic loop. Output the total distinct cells visited.
- **Approach:** Matrix simulation with a 2D visited state array or Floyd's Cycle Detection.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 6. Minimum Deletions to Make Character Frequencies Unique
- **College/Drive:** Apple India Campus Drive 2024
- **Problem Summary:** Given string $s$, find minimum character deletions to make all character frequencies unique.
- **LeetCode Equivalent:** [1647. Minimum Deletions to Make Character Frequencies Unique](https://leetcode.com/problems/minimum-deletions-to-make-character-frequencies-unique/)
- **Approach:** Count frequencies, insert into a Hash Set; decrement frequency until unused or zero.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Product of Array Except Self
- **College/Drive:** Apple Software Internship 2024
- **Problem Summary:** Given an integer array `nums`, return an array `answer` such that `answer[i]` is equal to the product of all elements of `nums` except `nums[i]`, without using the division operator in $O(N)$ time.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Prefix product array pass followed by a running suffix product accumulator.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 8. Find Peak Element (Logarithmic Search)
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** An element is a peak element if it is strictly greater than its neighbors. Find a peak element index in $O(\log N)$ time.
- **LeetCode Equivalent:** [162. Find Peak Element](https://leetcode.com/problems/find-peak-element/)
- **Approach:** Binary search: if `nums[mid] < nums[mid + 1]`, a peak must lie to the right; else to the left.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 9. String Compression (Run-Length In-Place)
- **College/Drive:** Apple SWE Screening 2024
- **Problem Summary:** Given an array of characters, compress it in-place using the running character count format.
- **LeetCode Equivalent:** [443. String Compression](https://leetcode.com/problems/string-compression/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 10. Longest Substring Without Repeating Characters
- **College/Drive:** Off-Campus Hiring 2024
- **Problem Summary:** Find length of longest substring without repeating characters.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Merge Intervals / Calendar Synchronization
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Merge all overlapping intervals into non-overlapping blocks.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 12. Lowest Common Ancestor in Binary Tree
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Find lowest common ancestor node of two nodes in binary tree.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 13. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Compute minimum minutes to spoil all fresh goods on $M \times N$ grid.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 14. Trapping Rain Water
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Compute amount of trapped water between elevation map bars after rain.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 15. LRU Cache Implementation
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Design $O(1)$ get and put cache with least recently used eviction.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Complexity:** $O(1)$ Time per op.

#### 16. Search in Rotated Sorted Array
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Search target element in a sorted rotated array in $O(\log N)$ time.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 17. Course Schedule II (Topological Sort)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find valid ordering of course completion dependencies.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Complexity:** $O(V + E)$ Time.

#### 18. Top K Frequent Elements (Min-Heap)
- **College/Drive:** Apple Campus Slot 2023
- **Problem Summary:** Return $K$ most frequent elements in array.
- **LeetCode Equivalent:** [347. Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/)
- **Complexity:** $O(N \log K)$ Time, $O(N)$ Space.

#### 19. Valid Parentheses with Multiple Brackets
- **College/Drive:** Apple Technical Screen 2023
- **Problem Summary:** Validate parentheses string containing `'()'`, `'{}'`, `'[]'`.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 20. Reorder Data in Log Files
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Reorder logs such that letter-logs come before digit-logs, sorted lexicographically.
- **LeetCode Equivalent:** [937. Reorder Data in Log Files](https://leetcode.com/problems/reorder-data-in-log-files/)
- **Complexity:** $O(M \cdot N \log N)$ Time.

---

## 🧠 Frequent Systems & Swift/C++ MCQs in Apple OA
1. **Automatic Reference Counting (ARC) vs Garbage Collection:**
   - How does ARC in Swift / Objective-C differ from Java/Python tracing Garbage Collection?
   - *Answer:* ARC is deterministic compile-time memory management that inserts retain and release calls automatically. Memory is deallocated immediately when reference count drops to 0 without "Stop-The-World" pauses. However, ARC cannot automatically resolve strong reference cycles (solved using `weak` and `unowned` references).
2. **Copy-on-Write (COW) in Swift Collections:**
   - How does COW optimize memory usage in Swift array assignments?
   - *Answer:* When assigning an array to a new variable (`var b = a`), both variables point to the same underlying memory buffer. A duplicate copy is allocated in memory only when one of the instances mutates its contents.
