# Microsoft Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🪟

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Codility** (Primary) / Mettl
- **Duration:** 75 to 110 minutes (Typically 2 to 3 Coding Questions)
- **Scoring Mechanism:** 
  - Codility separates score into **Correctness (50%)** and **Performance/Scalability (50%)**.
  - A solution passing all example tests will score ~50% if its time complexity is $O(N^2)$ when $O(N)$ or $O(N \log N)$ was expected.
  - Typical Cutoff: Total score $\ge 85\% - 90\%$ is generally required for shortlisting into interview rounds.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Strings & Frequency Maps:** Minimum deletions, unique character frequencies, palindrome partitions, balanced strings.
- **Prefix Sums & Balance Points:** Fair indices, partition sums, chunk sorting, inventory balance.
- **Intervals & Greedy Reductions:** Meeting rooms, adjacent swap reductions, equal pile heights, pollution filter halves.
- **Trees & Linked Lists:** Good nodes in tree, reverse nodes in $k$-group, cycle detection, longest zigzag path.
- **Simulation & Edge-Case Handling:** Airplane seat reservation, inserting digit 5 into positive/negative numbers.

---

## 📝 Verified Multi-Year OA Question Bank (Past 3 Years)
*Every problem listed below is a distinct, verified question sourced from 2023, 2024, and 2025/2026 campus placement drives (IITs, NITs, BITS, DTU) and off-campus Codility assessments. Duplicates across college slots have been strictly merged.*

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Minimum Deletions to Make Character Frequencies Unique
- **College/Drive:** IIT Roorkee / BITS Pilani 2024
- **Problem Summary:** Given a string $s$, return the minimum number of characters you need to delete to make the frequency of each character in $s$ unique.
- **LeetCode Equivalent:** [1647. Minimum Deletions to Make Character Frequencies Unique](https://leetcode.com/problems/minimum-deletions-to-make-character-frequencies-unique/)
- **Approach:** Count frequencies, insert into a Hash Set of seen frequencies. Decrement frequency until it is unused or reaches 0.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space (26 letters).

#### 2. Max Chunks to Make Sorted II (Codility Performance Classic)
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Summary:** Given an array that may contain duplicates, split it into the maximum number of contiguous chunks such that sorting each chunk individually sorts the entire array.
- **LeetCode Equivalent:** [768. Max Chunks To Make Sorted II](https://leetcode.com/problems/max-chunks-to-make-sorted-ii/)
- **Approach:** Maintain `prefix_max` from left and `suffix_min` from right. A partition is valid at index $i$ if $\max_{0 \dots i} \le \min_{i+1 \dots N-1}$.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 3. Min Steps to Make Piles Equal Height
- **College/Drive:** IIIT Allahabad 2024
- **Problem Summary:** You have $N$ boxes of different heights. In each step, you can reduce the tallest box to the height of the next tallest. Find the minimum steps to make all boxes the same height.
- **Approach:** Sort descending; for each distinct element, all previous taller elements require 1 step.
- **Complexity:** $O(N \log N)$ Time, $O(1)$ Space.

#### 4. Minimum Adjacent Swaps to Make Palindrome
- **College/Drive:** Microsoft Engage / Campus 2024
- **Problem Summary:** Given a string, find the minimum number of adjacent character swaps needed to make it a palindrome. If impossible, return -1.
- **LeetCode Equivalent:** [2193. Minimum Number of Moves to Make Palindrome](https://leetcode.com/problems/minimum-number-of-moves-to-make-palindrome/)
- **Approach:** Greedy Two Pointers: For each character from left, find matching character from right, compute adjacent swap distance.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Extra Space.

#### 5. Count Good Nodes in Binary Tree (Tree DFS)
- **College/Drive:** Off-Campus Drive 2024
- **Problem Summary:** Given a binary tree root, return the number of nodes where the path from the root contains no node with a value greater than that node's value.
- **LeetCode Equivalent:** [1448. Count Good Nodes in Binary Tree](https://leetcode.com/problems/count-good-nodes-in-binary-tree/)
- **Approach:** Pre-order DFS tracking `max_so_far` from root to current node.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 6. Minimum Filters to Halve Factory Pollution (Codility Signature)
- **College/Drive:** Microsoft Campus Drive 2024
- **Problem Summary:** Given an array $A$ of pollution amounts emitted by $N$ factories. Installing a filter on a factory reduces its emissions by half. Return the minimum number of filters needed to reduce the total pollution across all factories by at least 50%.
- **LeetCode Equivalent:** [2208. Minimum Operations to Halve Array Sum](https://leetcode.com/problems/minimum-operations-to-halve-array-sum/)
- **Approach:** Max-Heap (`std::priority_queue<double>`). Calculate total pollution and target reduction. Repeatedly pop the largest emitting factory, halve its emission, push back into the heap, and accumulate reduction until target is reached.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 7. Fair Indices in Two Arrays (Codility Classic)
- **College/Drive:** BITS Pilani / NIT Warangal 2024
- **Problem Summary:** You are given two arrays $A$ and $B$ of equal length $N$. An index $K$ ($1 \le K < N$) is "fair" if splitting both arrays at index $K$ results in four subarrays having identical sums: $\sum A[0 \dots K-1] = \sum A[K \dots N-1] = \sum B[0 \dots K-1] = \sum B[K \dots N-1]$. Count total fair indices.
- **Approach:** 
  - Compute total sums $S_A$ and $S_B$.
  - If $S_A \ne S_B$ or $S_A$ is odd, no fair index can exist.
  - Linear scan keeping running prefix sums $P_A$ and $P_B$. Index $K$ is fair if $P_A = P_B = S_A / 2$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Lexicographically Smallest String After Removing One Character
- **College/Drive:** Microsoft Codility Slot 2024
- **Problem Summary:** Given a lowercase string $S$, return the lexicographically smallest string that can be formed by deleting exactly one character from $S$.
- **Approach:** Linear scan from left to right. Find the first index $i$ such that $S[i] > S[i+1]$. Remove $S[i]$. If no such character exists (string is sorted ascending), remove the last character.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 9. Plane Seat Reservation (Families of 4)
- **College/Drive:** Microsoft On-Campus 2024
- **Problem Summary:** An airplane has $N$ rows of 10 seats labeled A through K (excluding I: A B C | D E F G | H J K). Given a list of already reserved seats, find the maximum number of 4-person families that can sit together in adjacent seats within the same aisle section.
- **Approach:** Hash Map storing bitmask of reserved seats per row. For each row, check availability of blocks `[D, E, F, G]`, `[B, C, D, E]`, or `[F, G, H, J]`.
- **Complexity:** $O(N + R)$ Time where $R$ is reserved seats count.

#### 10. Minimum Deletions to Make String Balanced
- **College/Drive:** Microsoft India SWE 2024
- **Problem Summary:** You are given a string $s$ consisting only of characters `'a'` and `'b'`. Return the minimum number of deletions needed to make $s$ balanced (no `'b'` appears before an `'a'`).
- **LeetCode Equivalent:** [1653. Minimum Deletions to Make String Balanced](https://leetcode.com/problems/minimum-deletions-to-make-string-balanced/)
- **Approach:** Stack or Dynamic Programming counting running `'b'` characters. When seeing an `'a'` after `'b'`, increment deletions and decrement `'b'` count.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Sign of the Product of an Array (Warm-up Codility)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Return sign of product without integer overflow (-1, 0, +1).
- **LeetCode Equivalent:** [1822. Sign of the Product of an Array](https://leetcode.com/problems/sign-of-the-product-of-an-array/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Reverse Words in a String (In-Place)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Reverse word order with clean single spacing.
- **LeetCode Equivalent:** [151. Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/)
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 13. Meeting Rooms II (Interval Scheduling)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Minimum conference rooms required for overlapping meeting intervals.
- **LeetCode Equivalent:** [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 14. Spiral Matrix Traversal
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Output $M \times N$ matrix in clockwise spiral order.
- **LeetCode Equivalent:** [54. Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
- **Complexity:** $O(M \times N)$ Time.

#### 15. Largest K such that both K and -K exist
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Find maximum integer $K$ where $-K$ is also present in array.
- **Approach:** Unordered set lookup in single pass.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 16. Longest ZigZag Path in a Binary Tree
- **College/Drive:** Microsoft Campus Slot 2023
- **Problem Summary:** Return the longest ZigZag path contained in a binary tree (alternating between left child and right child transitions).
- **LeetCode Equivalent:** [1372. Longest ZigZag Path in a Binary Tree](https://leetcode.com/problems/longest-zigzag-path-in-a-binary-tree/)
- **Approach:** DFS returning `(longest_if_go_left, longest_if_go_right)`.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 17. Maximum Value by Inserting Digit '5' (Codility Signature)
- **College/Drive:** Codility Drive 2023
- **Problem Summary:** Given an integer $N$ (positive or negative), return the maximum possible value that can be obtained by inserting the digit `'5'` anywhere in the decimal representation of $N$.
- **Approach:** 
  - If positive: Insert `'5'` before the first digit strictly smaller than 5.
  - If negative: Insert `'5'` before the first digit strictly greater than 5.
- **Complexity:** $O(D)$ Time where $D$ is number of digits ($\le 6$).

#### 18. Jump Game III (Reach Zero Index)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Given an array of non-negative integers `arr` and a `start` index. At index $i$, you can jump to $i + arr[i]$ or $i - arr[i]$. Determine if you can reach any index with value 0.
- **LeetCode Equivalent:** [1306. Jump Game III](https://leetcode.com/problems/jump-game-iii/)
- **Approach:** BFS Queue or DFS with a visited boolean array.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 19. Count Visible Nodes on Coordinate Plane (Slope GCD)
- **College/Drive:** Microsoft Off-Campus 2023
- **Problem Summary:** Given $N$ points on a 2D plane representing buildings. A person stands at origin $(0, 0)$. A building is blocked if another building lies directly along the same ray from the origin. Find total visible buildings.
- **Approach:** Represent each point $(x, y)$ by its reduced ray direction $(x / \gcd(|x|, |y|), y / \gcd(|x|, |y|))$ stored in a Hash Set.
- **Complexity:** $O(N \log(\min(X, Y)))$ Time, $O(N)$ Space.

#### 20. Count Substrings Without Repeating Characters of Fixed Length
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Count substrings of length $K$ that consist entirely of unique characters.
- **LeetCode Equivalent:** [1100. Find K-Length Substrings With No Repeated Characters](https://leetcode.com/problems/find-k-length-substrings-with-no-repeated-characters/)
- **Approach:** Sliding window of size $K$ with frequency counter.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.
