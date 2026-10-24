# Dell Technologies Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💻

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerEarth** / **AMCAT**
- **Test Duration:** 90 to 105 minutes
- **Structure Breakdown:**
  1. **Cognitive Aptitude Section (30 mins):** Quantitative Ability (15 Q), Logical Reasoning (15 Q), Verbal Ability (15 Q).
  2. **Technical MCQs Section (30 mins):** 20 to 25 MCQs covering Operating Systems (Storage systems, RAID levels, Paging, Inodes), Computer Networks, C++/Java OOPs, and Cloud Infrastructure basics.
  3. **Hands-On Coding Assessment (45 mins, 2 Questions):** LeetCode Easy to Medium difficulty.
- **Passing Cutoff:** Balanced score across Technical MCQs (>70%) and Coding (both questions passing all test cases) is required for interview shortlisting.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Operating Systems & Storage MCQs:** RAID levels (0, 1, 5, 6, 10), Disk scheduling (SCAN, C-SCAN, SSTF), Inodes, File systems, Virtual Memory.
- **Arrays & Two Pointers:** Subarray sums, in-place element removals, pair sum target, Kadane's maximum subarray.
- **Strings & Character Counting:** Anagram verification, palindrome construction, substring counts, longest common prefix.
- **Linked Lists & Stacks:** Middle element, detect cycle, reverse linked list, merge two sorted lists, valid syntax checking.
- **Trees & Graphs:** Level-order traversal, tree mirroring, connected components (server clusters), multi-source BFS.
- **Basic Dynamic Programming & Greedy:** Climbing stairs, house robber, coin change, interval merging.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. RAID Disk Redundancy & Usable Capacity Calculator
- **College/Drive:** Dell Campus Drive 2024 / VIT Vellore
- **Problem Summary:** Given $N$ physical storage disks each of capacity $C$ GB, calculate usable storage capacity and fault tolerance (maximum disk failures without data loss) under RAID 0, RAID 1, RAID 5, and RAID 6 configurations.
- **Formulas & Approach:**
  - RAID 0: Capacity = $N \times C$, Fault Tolerance = 0 disks.
  - RAID 1: Capacity = $C$, Fault Tolerance = $N - 1$ disks.
  - RAID 5: Capacity = $(N - 1) \times C$, Fault Tolerance = 1 disk ($N \ge 3$).
  - RAID 6: Capacity = $(N - 2) \times C$, Fault Tolerance = 2 disks ($N \ge 4$).
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

#### 2. Disk Track Seeking Order (SCAN / Elevator Simulation)
- **College/Drive:** Manipal Institute of Technology / RVCE 2024
- **Problem Summary:** Given an array of disk track requests and initial head position moving towards high cylinders, simulate the SCAN disk scheduling algorithm and output total head movement distance.
- **Approach:** Separate requests into tracks $\ge \text{initial}$ and $<\text{initial}$. Sort both arrays. Move to end of disk, reverse direction and service lower tracks. Sum absolute differences.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 3. Reverse Singly Linked List In-Place
- **College/Drive:** PES University / Thapar 2024
- **Problem Summary:** Given the head of a singly linked list, reverse the list in-place and return the new head.
- **LeetCode Equivalent:** [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
- **Approach:** Three pointers (`prev = nullptr`, `curr = head`, `next_node = nullptr`). Reorient pointers iteratively.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** SRM University / Campus Hiring 2024
- **Problem Summary:** Given an integer array `nums`, find the contiguous subarray with the largest sum and return its sum.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Approach:** Kadane's single-pass running sum: `current_sum = max(nums[i], current_sum + nums[i])`, update `max_so_far`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. LRU Cache Page Replacement Simulator
- **College/Drive:** Dell Technologies Off-Campus 2024
- **Problem Summary:** Simulate an OS page replacement mechanism of capacity $C$ processing page reference stream. Return total page faults.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Hash Map combined with a Doubly Linked List to maintain access order.
- **Complexity:** $O(N)$ Time where $N$ is number of page references, $O(C)$ Space.

#### 6. Merge Overlapping Memory / Backup Intervals
- **College/Drive:** Dell Campus Hiring 2025 / BITS Pilani
- **Problem Summary:** Given an array of interval intervals where `intervals[i] = [start_i, end_i]`, merge all overlapping intervals representing continuous disk snapshot time windows.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort intervals by start time. Iterate through intervals; if current interval overlaps with previous merged interval (`curr.start <= prev.end`), merge by `prev.end = max(prev.end, curr.end)`. Otherwise, push new interval.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 7. Active Storage Cluster Count (Number of Islands)
- **College/Drive:** Dell Campus Drive 2024 / VIT Chennai
- **Problem Summary:** Given an $M \times N$ grid of `'1'`s (online server nodes) and `'0'`s (offline nodes), return the number of isolated operational cluster islands.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Approach:** Standard BFS or DFS grid traversal. When finding an unvisited `'1'`, increment cluster count and sink all 4-directionally reachable `'1'`s to `'0'`.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space recursion/queue.

#### 8. Longest Substring Without Repeating Characters
- **College/Drive:** RVCE / BMSCE Bengaluru 2024
- **Problem Summary:** Given a telemetry data string `s`, find the length of the longest substring without repeating characters.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with a hash map storing last seen index of each character: `left = max(left, last_idx[char] + 1)`.
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

#### 9. Coin Change (Minimal Server Power Units)
- **College/Drive:** Dell Off-Campus Graduate Drive 2024
- **Problem Summary:** Given an array of integers `coins` representing available power pack wattages and an integer `amount`, return the fewest number of power packs needed to make up that amount. If impossible, return `-1`.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP array of size `amount + 1` initialized to infinity. `dp[i] = min(dp[i], dp[i - coin] + 1)`.
- **Complexity:** $O(\text{amount} \times N)$ Time, $O(\text{amount})$ Space.

#### 10. Server Hierarchy Level-Order Traversal
- **College/Drive:** Thapar Institute of Engineering & Technology 2024
- **Problem Summary:** Given the root of a binary tree representing a corporate rack-to-server hierarchy, return the level order traversal of its nodes' values (i.e., from left to right, level by level).
- **LeetCode Equivalent:** [102. Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/)
- **Approach:** BFS using a queue. Track queue size at the beginning of each level to process each tier in batches.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Subarray Sum Equals K
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Find total number of continuous subarrays whose sum equals $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency tracking: maintain running cumulative sum and check if `prefix_sum - K` exists in map.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 12. Valid Palindrome II (At Most One Deletion)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Given string `s`, return `true` if it can be a palindrome after deleting at most one character.
- **LeetCode Equivalent:** [680. Valid Palindrome II](https://leetcode.com/problems/valid-palindrome-ii/)
- **Approach:** Two pointers from outside in. On mismatch, check if skipping left or right yields a valid palindrome.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 13. Search in a 2D Matrix
- **College/Drive:** Off-Campus Drive 2023
- **Problem Summary:** Search target in $M \times N$ matrix sorted row-wise and column-wise.
- **LeetCode Equivalent:** [74. Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/)
- **Approach:** Binary search on flattened virtual array index: `row = mid / cols`, `col = mid % cols`.
- **Complexity:** $O(\log(M \times N))$ Time, $O(1)$ Space.

#### 14. Minimum Cost Climbing Stairs
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Minimum cost to reach top of floor stepping 1 or 2 steps.
- **LeetCode Equivalent:** [746. Min Cost Climbing Stairs](https://leetcode.com/problems/min-cost-climbing-stairs/)
- **Approach:** Space-optimized DP: `dp = cost[i] + min(prev1, prev2)`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 15. Longest Common Prefix
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Find longest common prefix string amongst an array of strings.
- **LeetCode Equivalent:** [14. Longest Common Prefix](https://leetcode.com/problems/longest-common-prefix/)
- **Approach:** Vertical scanning or sorting and comparing first and last string.
- **Complexity:** $O(S)$ Time where $S$ is sum of all characters.

#### 16. Infection Spread in Server Rack (Rotting Oranges)
- **College/Drive:** PES University / Dell Hackathon Hiring 2023
- **Problem Summary:** You are given an $M \times N$ grid where $0$ represents empty server slot, $1$ is a healthy server, and $2$ is an infected server. Every minute, any fresh server 4-directionally adjacent to an infected server becomes infected. Return minimum minutes until no fresh server remains, or $-1$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS starting with all initial cells containing $2$. Track time steps using level-based queue traversal.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 17. Mirror Directory Hierarchy (Invert Binary Tree)
- **College/Drive:** Dell Campus Hiring 2023
- **Problem Summary:** Given the root of a binary tree representing a file storage hierarchy, invert the tree and return its root.
- **LeetCode Equivalent:** [226. Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/)
- **Approach:** Recursive DFS swap `swap(root->left, root->right)` or iterative queue BFS.
- **Complexity:** $O(N)$ Time, $O(H)$ recursion stack depth.

#### 18. Storage Configuration Syntax Verification (Valid Parentheses)
- **College/Drive:** Dell Off-Campus Test 2023
- **Problem Summary:** Given a configuration string containing just `'('`, `')'`, `'{'`, `'}'`, `'['` and `']'`, determine if the input string is valid.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Push opening brackets onto a stack. When encountering closing bracket, verify top matches; pop or return false if mismatched/empty.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 19. First Unique Character in Data Stream
- **College/Drive:** Dell University Hiring 2023
- **Problem Summary:** Given a telemetry data string `s`, find the first non-repeating character in it and return its index. If it does not exist, return `-1`.
- **LeetCode Equivalent:** [387. First Unique Character in a String](https://leetcode.com/problems/first-unique-character-in-a-string/)
- **Approach:** Single frequency array of size 26 or hash map. First pass records frequency, second pass finds first index with frequency 1.
- **Complexity:** $O(N)$ Time, $O(1)$ Space (alphabet size bounded).

#### 20. Kth Largest Telemetry Metric (Quickselect / Min-Heap)
- **College/Drive:** Dell Tech Placement 2023
- **Problem Summary:** Given an integer array `nums` of system load metrics and an integer `k`, return the $k$-th largest element in the array.
- **LeetCode Equivalent:** [215. Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/)
- **Approach:** Min-heap of size $K$ to maintain $K$ largest elements in $O(N \log K)$ time, or Quickselect partition for expected $O(N)$ time.
- **Complexity:** $O(N \log K)$ Time, $O(K)$ Space.

---

## 🧠 Frequent Operating Systems & Storage MCQs Asked in Dell OA
1. **RAID 5 Parity Mechanics:**
   - Why does RAID 5 require at least 3 disks, and how is parity calculated?
   - *Answer:* Parity is computed using the XOR operation across data blocks and distributed cyclically across all disks. With 3 disks, 2 carry data and 1 carries parity for each stripe.
2. **Inodes in Unix File Systems:**
   - What information is stored in an Inode, and what is notably NOT stored in it?
   - *Answer:* An Inode stores file metadata (size, permissions, owner, timestamps, block pointers). The file name and directory hierarchy are NOT stored in the Inode (they are stored in the directory entry).
3. **Thrashing in Virtual Memory:**
   - What causes system thrashing?
   - *Answer:* When the sum of active processes' working sets exceeds total physical RAM, causing the CPU to spend more time swapping pages between disk and RAM than executing user instructions.
4. **SSTF vs SCAN Disk Scheduling:**
   - What is the primary drawback of Shortest Seek Time First (SSTF) disk scheduling compared to SCAN (Elevator)?
   - *Answer:* SSTF suffers from potential starvation of requests located far from the current head position if continuous closer requests arrive, whereas SCAN guarantees bounded wait times by sweeping unidirectionally.
