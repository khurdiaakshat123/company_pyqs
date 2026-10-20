# Microsoft Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🪟

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Codility** (Primary) / Mettl
- **Duration:** 75 to 90 minutes (3 Coding Questions)
- **Scoring Mechanism:** 
  - Codility separates score into **Correctness (50%)** and **Performance/Scalability (50%)**.
  - A solution passing all example tests will score ~50% if its time complexity is $O(N^2)$ when $O(N)$ or $O(N \log N)$ was expected.
  - Typical Cutoff: Total score $\ge 85\% - 90\%$ is generally required for shortlisting into interview rounds.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Strings & Frequency Maps:** Minimum deletions, unique character frequencies, palindrome partitions.
- **Prefix Sums & Balance Points:** Fair indices, partition sums, chunk sorting.
- **Intervals & Greedy Reductions:** Meeting rooms, adjacent swap reductions, equal pile heights.
- **Trees & Linked Lists:** Good nodes in tree, reverse nodes in $k$-group, cycle detection.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Minimum Deletions to Make Character Frequencies Unique
- **College/Drive:** IIT Roorkee / BITS Pilani 2024
- **Problem Statement:** Given a string $s$, return the minimum number of characters you need to delete to make the frequency of each character in $s$ unique.
- **LeetCode Equivalent:** [1647. Minimum Deletions to Make Character Frequencies Unique](https://leetcode.com/problems/minimum-deletions-to-make-character-frequencies-unique/)
- **Approach:** Count frequencies, insert into a Hash Set of seen frequencies. Decrement frequency until it is unused or reaches 0.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space (26 letters).

#### 2. Max Chunks to Make Sorted II (Codility Performance Classic)
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Statement:** Given an array that may contain duplicates, split it into the maximum number of contiguous chunks such that sorting each chunk individually sorts the entire array.
- **LeetCode Equivalent:** [768. Max Chunks To Make Sorted II](https://leetcode.com/problems/max-chunks-to-make-sorted-ii/)
- **Approach:** Maintain `prefix_max` from left and `suffix_min` from right. A partition is valid at index $i$ if $\max_{0 \dots i} \le \min_{i+1 \dots N-1}$.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 3. Min Steps to Make Piles Equal Height
- **College/Drive:** IIIT Allahabad 2024
- **Problem Statement:** You have $N$ boxes of different heights. In each step, you can reduce the tallest box to the height of the next tallest. Find the minimum steps to make all boxes the same height.
- **Approach:** Sort descending; for each distinct element, all previous taller elements require 1 step.
- **Complexity:** $O(N \log N)$ Time.

#### 4. Minimum Adjacent Swaps to Make Palindrome
- **College/Drive:** Microsoft Engage / Campus 2024
- **Problem Statement:** Given a string, find the minimum number of adjacent character swaps needed to make it a palindrome. If impossible, return -1.
- **LeetCode Equivalent:** [2193. Minimum Number of Moves to Make Palindrome](https://leetcode.com/problems/minimum-number-of-moves-to-make-palindrome/)
- **Approach:** Greedy Two Pointers: For each character from left, find matching character from right, compute adjacent swap distance.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Extra Space.

#### 5. Count Good Nodes in Binary Tree (Tree DFS)
- **College/Drive:** Off-Campus Drive 2024
- **Problem Statement:** Given a binary tree root, return the number of nodes where the path from the root contains no node with a value greater than that node's value.
- **LeetCode Equivalent:** [1448. Count Good Nodes in Binary Tree](https://leetcode.com/problems/count-good-nodes-in-binary-tree/)
- **Approach:** Pre-order DFS tracking `max_so_far` from root to current node.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Sign of the Product of an Array (Warm-up Codility)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Return sign of product without integer overflow.
- **LeetCode Equivalent:** [1822. Sign of the Product of an Array](https://leetcode.com/problems/sign-of-the-product-of-an-array/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Reverse Words in a String (In-Place)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Reverse word order with clean single spacing.
- **LeetCode Equivalent:** [151. Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/)
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 8. Meeting Rooms II (Intervals)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Minimum conference rooms required for overlapping meeting intervals.
- **LeetCode Equivalent:** [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 9. Spiral Matrix Traversal
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Output $M \times N$ matrix in clockwise spiral order.
- **LeetCode Equivalent:** [54. Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
- **Complexity:** $O(M \times N)$ Time.

#### 10. Largest K such that both K and -K exist
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Find maximum integer $K$ where $-K$ is also present in array.
- **Approach:** Unordered set lookup.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.
