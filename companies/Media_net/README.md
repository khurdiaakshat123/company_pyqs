# Media.net (Directi) Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) 🌐

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 to 120 minutes
- **Structure Breakdown:**
  - 3 Algorithmic Coding Problems (Competitive Programming / Hard).
  - No MCQs, pure high-difficulty algorithmic challenges.
- **Evaluation Criteria:**
  - Media.net (Directi) is legendary in Indian campus placements for setting Codeforces Div. 2 D/E level problems.
  - Very strict $O(N)$ or $O(N \log N)$ execution constraints. Submissions with naive quadratic complexities score 0 on hidden test cases.
  - Solving 2 out of 3 problems completely typically guarantees an interview call.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Trees & Heavy Tree DP:** Root-to-leaf path queries, subtree XORs, tree diameter rerooting, Euler tour flattening.
- **String Algorithms & Tries:** Longest prefix matches, Aho-Corasick, KMP / Z-algorithm, shortest common supersequence.
- **Segment Trees with Lazy Propagation:** Dynamic range maximum, sum updates, range inversion.
- **Constructive Mathematics & Combinatorics:** Parity manipulation, bitwise game theory, AP-free permutations.
- **Greedy Deadline Scheduling:** Campaign scheduling with heaps, merge intervals.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Root-to-Leaf Path XOR Queries on Weighted Tree
- **College/Drive:** IIT Bombay / IIT Kanpur 2024–2025
- **Problem Summary:** Given a tree with $N$ vertices rooted at node 1. Each edge has a weight $W_i$. Answer $Q$ queries: Given node $U$ and integer $X$, find the maximum XOR sum achievable by XORing $X$ with the path weight from $U$ to any node in its subtree.
- **Constraints:** $1 \le N, Q \le 10^5$, edge weights $\le 10^9$.
- **Approach:** Flatten tree into array using Euler Tour (subtree becomes contiguous range $[in[U], out[U]]$). Persistent Trie / Segment Tree over Trie to answer maximum XOR range queries in $O(30)$.
- **Complexity:** $O(N \log N + Q \times 30)$ Time.

#### 2. Ad-Auction Keyword Bidding (Trie + KMP)
- **College/Drive:** BITS Pilani 2024–2025
- **Problem Summary:** Given a master ad search query string $S$ of length $N$ and a dictionary of $M$ bidding keywords. Find the maximum number of non-overlapping keywords from the dictionary that can be matched as substrings in $S$.
- **Constraints:** $|S| \le 10^5$, $\sum |keywords| \le 10^5$.
- **Approach:** Aho-Corasick Automaton or Trie matching combined with Interval Scheduling Greedy choice.
- **Complexity:** $O(N + \sum |keywords|)$ Time.

#### 3. Range Maximum Segment Tree with Lazy Range Inversion
- **College/Drive:** IIIT Hyderabad 2024–2025
- **Problem Summary:** Given an array of integers, support $Q$ queries:
  1. Multiply all elements in range $[L, R]$ by $-1$.
  2. Find the maximum subarray sum in range $[L, R]$.
- **Constraints:** $1 \le N, Q \le 10^5$.
- **Approach:** Segment Tree with Lazy Propagation storing: `total_sum`, `max_prefix`, `max_suffix`, `max_subarray`, and their corresponding inverted negative counterparts.
- **Complexity:** $O((N + Q) \log N)$ Time.

#### 4. Constructive Binary Sequence Balance
- **College/Drive:** DTU / NSUT 2024–2025
- **Problem Summary:** Given integer $N$, construct a permutation of $1$ to $N$ such that no three elements $(P_i, P_j, P_k)$ with $i < j < k$ form an arithmetic progression ($P_j - P_i = P_k - P_j$).
- **Constraints:** $1 \le N \le 10^5$.
- **Approach:** Divide and conquer: Place all odd numbers in the first half (recursively solved), and all even numbers in the second half (recursively solved).
- **Complexity:** $O(N \log N)$ Time.

#### 5. Shortest Common Supersequence
- **College/Drive:** On-Campus Drive Slot 1 (2024–2025)
- **Problem Summary:** Given two strings `str1` and `str2`, return the shortest string that has both `str1` and `str2` as subsequences.
- **Constraints:** $1 \le |str1|, |str2| \le 1000$.
- **LeetCode Equivalent:** [1092. Shortest Common Supersequence](https://leetcode.com/problems/shortest-common-supersequence/)
- **Approach:** Find Longest Common Subsequence (LCS) using DP, then reconstruct string adding characters from both strings.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 6. Course Schedule III / Ad Campaign Deadline Optimizer
- **College/Drive:** Campus Drive Slot 2 (2024)
- **Problem Summary:** Schedule maximum campaigns with duration and hard deadline.
- **Constraints:** $1 \le courses.length \le 10^4$.
- **LeetCode Equivalent:** [630. Course Schedule III](https://leetcode.com/problems/course-schedule-iii/)
- **Approach:** Sort by deadline; maintain Max-Heap of durations.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 7. Word Break II (All Valid Sentences)
- **College/Drive:** Off-Campus 2024
- **Problem Summary:** Return all possible space-separated sentence breakdowns from dictionary words.
- **Constraints:** $1 \le s.length \le 20$.
- **LeetCode Equivalent:** [140. Word Break II](https://leetcode.com/problems/word-break-ii/)
- **Approach:** Trie of dictionary words combined with DFS memoization.
- **Complexity:** Exponential worst-case, heavily memoized.

#### 8. Minimum Number of Flips to Make Binary Grid Palindromic
- **College/Drive:** Campus Hiring 2024
- **Problem Summary:** Find minimum flips so all rows and columns are palindromes.
- **Constraints:** $1 \le M, N \le 200$.
- **Approach:** Group cells that map to each other under 4-way row/col reflection: `(r, c)`, `(M-1-r, c)`, `(r, N-1-c)`, `(M-1-r, N-1-c)`. Set all 4 to majority bit.
- **Complexity:** $O(M \times N)$ Time, $O(1)$ Space.

#### 9. Count of Smaller Numbers After Self
- **College/Drive:** Media.net Pune Drive 2024
- **Problem Summary:** Return number of smaller elements to the right of each element in an array.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [315. Count of Smaller Numbers After Self](https://leetcode.com/problems/count-of-smaller-numbers-after-self/)
- **Approach:** Coordinate compression + Fenwick Tree / BIT traversed right to left.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 10. Longest Increasing Path in a Matrix
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Return length of longest strictly increasing path in integer matrix.
- **Constraints:** $1 \le M, N \le 200$.
- **LeetCode Equivalent:** [329. Longest Increasing Path in a Matrix](https://leetcode.com/problems/longest-increasing-path-in-a-matrix/)
- **Approach:** DFS with 2D memoization table.
- **Complexity:** $O(M \times N)$ Time and Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Trapping Rain Water II (3D Elevation Grid)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Elevation map 3D water capacity.
- **Constraints:** $1 \le M, N \le 200$.
- **LeetCode Equivalent:** [407. Trapping Rain Water II](https://leetcode.com/problems/trapping-rain-water-ii/)
- **Approach:** Min-Heap priority queue starting from boundaries inward.
- **Complexity:** $O(M \cdot N \log(M \cdot N))$ Time.

#### 12. Network Delay Time / Node Broadcast
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Calculate time for all network nodes to receive broadcast update.
- **Constraints:** $1 \le N \le 100$, $1 \le edges \le 6000$.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's algorithm with Min-Heap.
- **Complexity:** $O(E \log V)$ Time.

#### 13. Subarray Sum Equals K
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Count total continuous subarrays whose sum equals $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency counter.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 14. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Minimum minutes to infect all items in 2D grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 15. Daily Temperatures / Metric Spike Monotonic Stack
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Find days to wait for a higher value.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 16. Merge Intervals
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Merge all overlapping intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time; merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 17. Product of Array Except Self without Division
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 18. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Sliding window with hash map storing last seen indices.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

#### 19. Search in Rotated Sorted Array
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Find target in rotated sorted array in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 5000$.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking sorted half.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 20. Container With Most Water
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Two pointers inward maximizing area between vertical lines.
- **Constraints:** $2 \le heights.length \le 10^5$.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 💡 Media.net Competitive Programming OA Guidelines
1. **Prepare for Segment Trees and Trie Variations:** Media.net regularly sets dynamic range tree problems with lazy propagation and persistent trie queries.
2. **Heavy Constraints Vigilance:** Watch out for $10^5$ queries on trees; tree flattening via Euler Tour into 1D arrays is the key reduction technique.
3. **Write Fast I/O:** Use `cin.tie(NULL); ios_base::sync_with_stdio(false);` in C++ to prevent I/O bottlenecks from causing TLE.
