# Squarepoint Capital Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) 📈

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **Codility**
- **Test Duration:** 90 to 120 minutes
- **Structure Breakdown:**
  - 2 to 3 Algorithmic Coding Problems (LeetCode Medium to Hard).
  - High-frequency quantitative/trading algorithmic challenges with strict runtime bounds ($O(N)$ or $O(N \log N)$), memory efficiency, and corner-case precision.
- **Evaluation Criteria:**
  - Squarepoint is a global quantitative investment firm.
  - Solutions that pass public examples but fail hidden large-scale stress tests due to $O(N^2)$ algorithmic choices are eliminated automatically. Flawless handling of integer overflow (64-bit `long long`) and floating-point precision ($10^{-9}$) is required.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Dynamic Range Queries & Two Pointers:** Sliding window conditions, interval merging, prefix calculations, continuous subarray products.
- **Grid & Matrix Simulations:** Cascading tile clearance, gravity compaction, multi-pass board evaluations, longest path in matrix.
- **Graph Traversals & Shortest Paths:** Rate conversion cycles (negative cycles via Bellman-Ford), Dijkstra with transaction delays, MST.
- **Custom Data Structures & Heaps:** Sliding window median (two heaps or multiset), order execution simulators, top-K streams.
- **Dynamic Programming:** Interval DP, buy/sell stock with cooldown, job scheduling with binary search, parallel schedule completion.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Cascading Grid Tile & Clearance Simulator
- **College/Drive:** IIT Bombay / BITS Pilani 2024–2025
- **Problem Summary:** Given an $M \times N$ grid of labeled tiles. Removing a tile triggers cascading clearance: if all tiles in a row/column share the same label or reach zero weight, the row/column collapses and remaining tiles shift downward. Simulate $K$ removal steps and calculate final non-empty cells.
- **Constraints:** $M, N \le 100$, $K \le 500$.
- **Approach:** Custom 2D grid simulation with in-place column compaction (two-pointer gravity shift) and BFS/DFS component tracking.
- **Complexity:** $O(M \times N \times K)$ Time, $O(M \times N)$ Space.

#### 2. Currency Arbitrage via Rate Matrix (Log Transformed Shortest Path)
- **College/Drive:** IIT Delhi / IIT Kharagpur 2024–2025
- **Problem Summary:** Given a directed graph representing exchange rates between $N$ currencies, find the maximum conversion rate from currency $A$ to currency $B$ using at most $K$ exchanges, or detect if an infinite arbitrage cycle exists.
- **Constraints:** $N \le 200$, edges $\le 2000$.
- **Approach:** Bellman-Ford algorithm using edge weights $w(u, v) = -\log(\text{rate}(u, v))$ to transform multiplication of rates into addition of negative logarithms. Detect negative weight cycles.
- **Complexity:** $O(K \times E)$ Time, $O(V)$ Space.

#### 3. Sliding Window Median (Dual Balanced Heaps)
- **College/Drive:** IIT Madras / Quant SWE Campus 2024–2025
- **Problem Summary:** Given an array of integers `nums` and a sliding window of size $k$, return the median of the elements in the window at each step.
- **Constraints:** $1 \le nums.length \le 10^5$, $1 \le k \le nums.length$.
- **LeetCode Equivalent:** [480. Sliding Window Median](https://leetcode.com/problems/sliding-window-median/)
- **Approach:** Two balanced heaps (Max-Heap for lower half, Min-Heap for upper half) with lazy removal hash map, or balanced BST (`std::multiset` in C++).
- **Complexity:** $O(N \log K)$ Time, $O(K)$ Space.

#### 4. Continuous Subarray Range Product
- **College/Drive:** BITS Pilani 2024–2025
- **Problem Summary:** Return the number of contiguous subarrays where the product of elements is strictly less than $K$.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$, $1 \le nums[i] \le 1000$, $0 \le k \le 10^6$.
- **LeetCode Equivalent:** [713. Subarray Product Less Than K](https://leetcode.com/problems/subarray-product-less-than-k/)
- **Approach:** Sliding window with two pointers (`left`, `right`). For each valid right pointer, add `(right - left + 1)`. Handle $k \le 1$ as edge case returning 0.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Search Suggestion System (Trie + Lexicographical Order)
- **College/Drive:** Off-Campus Quant Hiring 2024–2025
- **Problem Summary:** Design a search suggestion system that, after each character of a search word is typed, returns at most 3 lexicographically smallest search results matching the prefix.
- **Constraints:** $1 \le products.length \le 1000$, $1 \le searchWord.length \le 1000$.
- **LeetCode Equivalent:** [1268. Search Suggestions System](https://leetcode.com/problems/search-suggestions-system/)
- **Approach:** Trie data structure storing at most 3 top strings at each trie node or Binary Search (`std::lower_bound`) on sorted vocabulary.
- **Complexity:** $O(N \log N + L \log N)$ Time.

#### 6. Minimum Cost to Connect All Data Centers (MST)
- **College/Drive:** IIT Roorkee / IIT BHU 2024
- **Problem Summary:** Given coordinates of $N$ financial data centers on a 2D plane, find the minimum cost to make all points connected where cost between two points is their Manhattan distance.
- **Constraints:** $1 \le N \le 1000$, coordinates in $[-10^6, 10^6]$.
- **LeetCode Equivalent:** [1584. Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)
- **Approach:** Prim's Algorithm maintaining min distance array from tree to unvisited vertices in $O(V^2)$, avoiding explicit edge storage.
- **Complexity:** $O(V^2)$ Time, $O(V)$ Space.

#### 7. Longest Increasing Path in a Matrix
- **College/Drive:** Squarepoint Campus Slot 2024
- **Problem Summary:** Given an $M \times N$ integers matrix, return the length of the longest increasing path. From each cell, you can move in 4 directions.
- **Constraints:** $1 \le M, N \le 200$, $0 \le matrix[i][j] \le 2^{31} - 1$.
- **LeetCode Equivalent:** [329. Longest Increasing Path in a Matrix](https://leetcode.com/problems/longest-increasing-path-in-a-matrix/)
- **Approach:** Depth-First Search with Memoization (`memo[i][j]`). Since path is strictly increasing, grid forms a Directed Acyclic Graph (DAG) with guaranteed termination.
- **Complexity:** $O(M \cdot N)$ Time, $O(M \cdot N)$ Space.

#### 8. Parallel Courses III / Minimum Total Completion Time
- **College/Drive:** Squarepoint Quant Dev 2024
- **Problem Summary:** Given $N$ tasks with execution `time[i]` and directed prerequisite relations, find the minimum time needed to complete all courses assuming unlimited tasks can be executed simultaneously in parallel once dependencies finish.
- **Constraints:** $1 \le n \le 5 \times 10^4$, $0 \le relations.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [2050. Parallel Courses III](https://leetcode.com/problems/parallel-courses-iii/)
- **Approach:** Topological Sort with Kahn's Algorithm. Maintain `dist[v] = max(dist[v], dist[u] + time[v])` for every incoming prerequisite edge $(u, v)$.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 9. Word Ladder II / All Shortest Mutation Paths
- **College/Drive:** Off-Campus SWE 2024
- **Problem Summary:** Given two words `beginWord` and `endWord`, and a dictionary `wordList`, return all the shortest transformation sequences from `beginWord` to `endWord`.
- **Constraints:** $1 \le beginWord.length \le 5$, $1 \le wordList.length \le 500$.
- **LeetCode Equivalent:** [126. Word Ladder II](https://leetcode.com/problems/word-ladder-ii/)
- **Approach:** BFS to compute level distances and parent adjacency list + DFS backtracking from `endWord` to `beginWord` along valid shortest predecessor edges.
- **Complexity:** $O(N \cdot L + \text{paths})$ Time, $O(N)$ Space.

#### 10. Split Array Largest Sum (Capacity Optimization)
- **College/Drive:** BITS Pilani / IIT Kanpur 2024
- **Problem Summary:** Given an integer array `nums` and an integer `k`, split the array into $k$ non-empty continuous subarrays such that the largest sum of any subarray is minimized.
- **Constraints:** $1 \le nums.length \le 1000$, $1 \le k \le \min(50, nums.length)$, $0 \le nums[i] \le 10^6$.
- **LeetCode Equivalent:** [410. Split Array Largest Sum](https://leetcode.com/problems/split-array-largest-sum/)
- **Approach:** Binary Search on answer in range $[\max(nums), \sum nums]$. Greedily verify whether array can be partitioned into $\le k$ subarrays with max cap $M$.
- **Complexity:** $O(N \log(\sum nums))$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Largest Rectangle in Histogram
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Find the area of the largest rectangle in the histogram.
- **Constraints:** $1 \le heights.length \le 10^5$.
- **LeetCode Equivalent:** [84. Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/)
- **Approach:** Monotonic Increasing Stack of bar indices. When finding a bar shorter than stack top, pop and calculate area `height * (i - stack.top() - 1)`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 12. Network Delay Time with Latency Bounds
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Calculate minimum time for all nodes to receive a signal from source node $K$.
- **Constraints:** $1 \le N \le 100$, $1 \le edges \le 6000$.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's algorithm using Priority Queue.
- **Complexity:** $O(E \log V)$ Time, $O(V + E)$ Space.

#### 13. Best Time to Buy and Sell Stock with Cooldown
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Maximize stock profit with a 1-day cooldown period after selling.
- **Constraints:** $1 \le prices.length \le 5000$.
- **LeetCode Equivalent:** [309. Best Time to Buy and Sell Stock with Cooldown](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-cooldown/)
- **Approach:** State machine DP with 3 states: `held`, `sold`, `rest`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 14. Median of Two Sorted Arrays
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Find median of two sorted arrays of sizes $m$ and $n$ in $O(\log(m+n))$ time.
- **Constraints:** $0 \le m, n \le 1000$.
- **LeetCode Equivalent:** [4. Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)
- **Approach:** Binary search on the partition of the smaller array.
- **Complexity:** $O(\log(\min(m, n)))$ Time, $O(1)$ Space.

#### 15. Longest Repeating Character Replacement
- **College/Drive:** Off-Campus Drive 2023
- **Problem Summary:** Return longest substring containing same letter after at most $k$ replacements.
- **Constraints:** $1 \le s.length \le 10^5$, $0 \le k \le s.length$.
- **LeetCode Equivalent:** [424. Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/)
- **Approach:** Sliding window with max frequency tracker: `(window_len - max_freq) <= k`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. Trapping Rain Water
- **College/Drive:** IIT Delhi Slot 2023
- **Problem Summary:** Given $n$ non-negative integers representing an elevation map where width of each bar is 1, compute how much water it can trap after raining.
- **Constraints:** $1 \le n \le 2 \times 10^4$, $0 \le height[i] \le 10^5$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers (`left`, `right`) with `max_left` and `max_right`. Water accumulated at pointer is bounded by minimum of the two peaks.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 17. Merge K Sorted Lists / Multi-Feed Order Stream
- **College/Drive:** Quant Developer Slot 2023
- **Problem Summary:** Merge $K$ sorted linked lists or time-series price streams into one sorted stream.
- **Constraints:** $K \le 10^4$, total elements $\le 10^5$.
- **LeetCode Equivalent:** [23. Merge k Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/)
- **Approach:** Min-Heap storing `(node.val, node)` of size $K$. Continuously extract root and push next element from that list.
- **Complexity:** $O(N \log K)$ Time, $O(K)$ Space.

#### 18. Maximum Profit in Job Scheduling
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Given $N$ jobs with `startTime`, `endTime`, and `profit`, find the maximum profit you can achieve such that no two jobs overlap.
- **Constraints:** $1 \le N \le 5 \times 10^4$.
- **LeetCode Equivalent:** [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)
- **Approach:** Sort jobs by `endTime`. Dynamic programming: `dp[i] = max(dp[i-1], profit[i] + dp[prev_non_overlapping])` using Binary Search (`upper_bound`) to find the latest compatible previous job.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 19. Subarray Sum Equals K
- **College/Drive:** Squarepoint London / India Screening 2023
- **Problem Summary:** Given an array of integers `nums` and an integer `k`, return total number of subarrays whose sum equals $k$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Hash Map tracking prefix sum frequencies. Add `map[curr_sum - k]` to answer.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 20. Decode String with Nested Multipliers
- **College/Drive:** Technical Assessment 2023
- **Problem Summary:** Given an encoded string like `"3[a2[c]]"`, return its decoded string `"accaccacc"`.
- **Constraints:** $1 \le s.length \le 30$.
- **LeetCode Equivalent:** [394. Decode String](https://leetcode.com/problems/decode-string/)
- **Approach:** Two stacks: one for repeat counts `countStack` and one for accumulated string prefixes `stringStack`.
- **Complexity:** $O(\text{output length})$ Time and Space.

---

## 💡 Squarepoint Coding Assessment Best Practices
1. **Precision Matters:** Quant test suites check for exact numerical edge cases; use `double` or `long double` for float math and check for division by zero.
2. **64-bit Overflow Awareness:** When computing sums or products of arrays where elements are up to $10^9$, immediately cast accumulator variables to `long long` (or `int64_t`).
3. **Space Optimizations:** Strive for $O(1)$ or $O(K)$ space on sliding window problems rather than copying large sub-arrays.
