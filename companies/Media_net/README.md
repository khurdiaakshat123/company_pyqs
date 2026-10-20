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
- **Trees & Heavy Tree DP:** Root-to-leaf path queries, subtree XORs, tree diameter rerooting.
- **String Algorithms & Tries:** Longest prefix matches, Aho-Corasick, KMP / Z-algorithm.
- **Segment Trees with Lazy Propagation:** Dynamic range maximum and sum updates.
- **Constructive Mathematics:** Parity manipulation, bitwise game theory.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Root-to-Leaf Path XOR Queries on Weighted Tree
- **College/Drive:** IIT Bombay / IIT Kanpur 2024
- **Problem Statement:** Given a tree with $N$ vertices rooted at node 1. Each edge has a weight $W_i$. Answer $Q$ queries: Given node $U$ and integer $X$, find the maximum XOR sum achievable by XORing $X$ with the path weight from $U$ to any node in its subtree.
- **Approach:** Flatten tree into array using Euler Tour (subtree becomes contiguous range $[in[U], out[U]]$). Persistent Trie / Segment Tree over Trie to answer maximum XOR range queries in $O(30)$.
- **Complexity:** $O(N \log N + Q \times 30)$ Time.

#### 2. Ad-Auction Keyword Bidding (Trie + KMP)
- **College/Drive:** BITS Pilani 2024
- **Problem Statement:** Given a master ad search query string $S$ of length $N$ and a dictionary of $M$ bidding keywords. Find the maximum number of non-overlapping keywords from the dictionary that can be matched as substrings in $S$.
- **Approach:** Aho-Corasick Automaton or Trie matching combined with Interval Scheduling Greedy choice.
- **Complexity:** $O(N + \sum |keywords|)$ Time.

#### 3. Range Maximum Segment Tree with Lazy Range Inversion
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Statement:** Given an array of integers, support $Q$ queries:
  1. Multiply all elements in range $[L, R]$ by $-1$.
  2. Find the maximum subarray sum in range $[L, R]$.
- **Approach:** Segment Tree with Lazy Propagation storing: `total_sum`, `max_prefix`, `max_suffix`, `max_subarray`, and their corresponding inverted negative counterparts.
- **Complexity:** $O((N + Q) \log N)$ Time.

#### 4. Constructive Binary Sequence Balance
- **College/Drive:** DTU / NSUT 2024
- **Problem Statement:** Given integer $N$, construct a permutation of $1$ to $N$ such that no three elements $(P_i, P_j, P_k)$ with $i < j < k$ form an arithmetic progression ($P_j - P_i = P_k - P_j$).
- **Approach:** Divide and conquer: Place all odd numbers in the first half (recursively solved), and all even numbers in the second half (recursively solved).
- **Complexity:** $O(N \log N)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Shortest Common Supersequence
- **College/Drive:** On-Campus Drive Slot 1 (2023)
- **Problem Statement:** Given two strings `str1` and `str2`, return the shortest string that has both `str1` and `str2` as subsequences.
- **LeetCode Equivalent:** [1092. Shortest Common Supersequence](https://leetcode.com/problems/shortest-common-supersequence/)
- **Approach:** Find Longest Common Subsequence (LCS) using DP, then reconstruct string adding characters from both strings.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 6. Course Schedule III / Ad Campaign Deadline Optimizer
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Schedule maximum campaigns with duration and hard deadline.
- **LeetCode Equivalent:** [630. Course Schedule III](https://leetcode.com/problems/course-schedule-iii/)
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 7. Word Break II (All Valid Sentences)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Return all possible space-separated sentence breakdowns from dictionary words.
- **LeetCode Equivalent:** [140. Word Break II](https://leetcode.com/problems/word-break-ii/)
- **Complexity:** Exponential worst-case, memoized DFS.

#### 8. Minimum Number of Flips to Make Binary Grid Palindromic
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Find minimum flips so all rows and columns are palindromes.
- **Complexity:** $O(M \times N)$ Time.
