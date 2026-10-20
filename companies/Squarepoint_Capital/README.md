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
- **Grid & Matrix Simulations:** Cascading tile clearance, gravity compaction, multi-pass board evaluations.
- **Graph Traversals & Shortest Paths:** Rate conversion cycles (negative cycles via Bellman-Ford), Dijkstra with transaction delays.
- **Custom Data Structures & Heaps:** Sliding window median (two heaps or multiset), order execution simulators, top-K streams.
- **Dynamic Programming:** Interval DP, buy/sell stock with cooldown and transaction fees.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Cascading Grid Tile & Clearance Simulator
- **College/Drive:** IIT Bombay / BITS Pilani 2024
- **Problem Summary:** Given an $M \times N$ grid of labeled tiles. Removing a tile triggers cascading clearance: if all tiles in a row/column share the same label or reach zero weight, the row/column collapses and remaining tiles shift downward. Simulate $K$ removal steps and calculate final non-empty cells.
- **Approach:** Custom 2D grid simulation with in-place column compaction and BFS/DFS component tracking.
- **Complexity:** $O(M \times N \times K)$ Time, $O(M \times N)$ Space.

#### 2. Currency Arbitrage via Rate Matrix (Log Transformed Shortest Path)
- **College/Drive:** IIT Delhi / IIT Kharagpur 2024
- **Problem Summary:** Given a directed graph representing exchange rates between $N$ currencies, find the maximum conversion rate from currency $A$ to currency $B$ using at most $K$ exchanges, or detect if an infinite arbitrage cycle exists.
- **Approach:** Bellman-Ford algorithm using edge weights $w(u, v) = -\log(\text{rate}(u, v))$ to transform multiplication of rates into addition of negative logarithms. Detect negative weight cycles.
- **Complexity:** $O(K \times E)$ Time, $O(V)$ Space.

#### 3. Sliding Window Median (Dual Balanced Heaps)
- **College/Drive:** IIT Madras / Quant SWE Campus 2024
- **Problem Summary:** Given an array of integers `nums` and a sliding window of size $k$, return the median of the elements in the window at each step.
- **LeetCode Equivalent:** [480. Sliding Window Median](https://leetcode.com/problems/sliding-window-median/)
- **Approach:** Two balanced heaps (Max-Heap for lower half, Min-Heap for upper half) with lazy removal hash map, or balanced BST (`std::multiset` in C++).
- **Complexity:** $O(N \log K)$ Time, $O(K)$ Space.

#### 4. Continuous Subarray Range Product
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** Return the number of contiguous subarrays where the product of elements is strictly less than $K$.
- **LeetCode Equivalent:** [713. Subarray Product Less Than K](https://leetcode.com/problems/subarray-product-less-than-k/)
- **Approach:** Sliding window with two pointers (`left`, `right`). For each valid right pointer, add `(right - left + 1)`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Search Suggestion System (Trie + Lexicographical Order)
- **College/Drive:** Off-Campus Quant Hiring 2024
- **Problem Summary:** Design a search suggestion system that, after each character of a search word is typed, returns at most 3 lexicographically smallest search results matching the prefix.
- **LeetCode Equivalent:** [1268. Search Suggestions System](https://leetcode.com/problems/search-suggestions-system/)
- **Approach:** Trie data structure storing at most 3 top strings at each trie node or Binary Search (`std::lower_bound`) on sorted vocabulary.
- **Complexity:** $O(N \log N + L \log N)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Largest Rectangle in Histogram
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Find the area of the largest rectangle in the histogram.
- **LeetCode Equivalent:** [84. Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/)
- **Approach:** Monotonic Increasing Stack of bar indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 7. Network Delay Time with Latency Bounds
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Calculate minimum time for all nodes to receive a signal from source node $K$.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's algorithm using Priority Queue.
- **Complexity:** $O(E \log V)$ Time, $O(V + E)$ Space.

#### 8. Best Time to Buy and Sell Stock with Cooldown
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Maximize stock profit with a 1-day cooldown period after selling.
- **LeetCode Equivalent:** [309. Best Time to Buy and Sell Stock with Cooldown](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-cooldown/)
- **Approach:** State machine DP with 3 states: `held`, `sold`, `rest`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Median of Two Sorted Arrays
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Find median of two sorted arrays of sizes $m$ and $n$ in $O(\log(m+n))$ time.
- **LeetCode Equivalent:** [4. Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)
- **Approach:** Binary search on the partition of the smaller array.
- **Complexity:** $O(\log(\min(m, n)))$ Time, $O(1)$ Space.

#### 10. Longest Repeating Character Replacement
- **College/Drive:** Off-Campus Drive 2023
- **Problem Summary:** Return longest substring containing same letter after at most $k$ replacements.
- **LeetCode Equivalent:** [424. Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/)
- **Approach:** Sliding window with max frequency tracker: `(window_len - max_freq) <= k`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 💡 Squarepoint Coding Assessment Best Practices
1. **Precision Matters:** Quant test suites check for exact numerical edge cases; use `double` or `long double` for float math and check for division by zero.
2. **64-bit Overflow Awareness:** When computing sums or products of arrays where elements are up to $10^9$, immediately cast accumulator variables to `long long` (or `int64_t`).
3. **Space Optimizations:** Strive for $O(1)$ or $O(K)$ space on sliding window problems rather than copying large sub-arrays.
