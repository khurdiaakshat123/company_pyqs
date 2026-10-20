# Squarepoint Capital Online Assessment Guide & PYQs (2023 - 2025/2026) 📈

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **Codility**
- **Test Duration:** 90 to 120 minutes
- **Structure Breakdown:**
  - 2 to 3 Algorithmic Coding Problems (LeetCode Medium to Hard).
  - Heavy emphasis on strict computational runtime bounds ($O(N)$ or $O(N \log N)$), memory efficiency, and corner-case precision.
- **Evaluation Criteria:**
  - Proprietary quant trading firm with very high compensation packages.
  - Solutions that pass public examples but fail hidden large-scale stress tests due to $O(N^2)$ algorithmic choices are eliminated automatically.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Dynamic Range Queries & Two Pointers | Medium - Hard | Sliding window conditions, interval merging, prefix calculations |
| **Very High** | Grid & Matrix Simulations | Medium - Hard | Bookshelf / tile clearance simulations, connected components |
| **High** | Graph Traversals & Shortest Paths | Medium - Hard | Rate conversion cycles (negative cycles), Dijkstra with transfer penalties |
| **High** | Custom Data Structures & Heaps | Medium - Hard | Sliding window median, transaction book order simulations |
| **Medium** | Low-Level Systems & Concurrency | Medium | Thread-safe data structures, cache awareness |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Grid Tile / Bookshelf Clearance Simulation
- **Problem Summary:** Given an $M \times N$ grid of labeled tiles. Removing a tile triggers a cascading clearance: if all tiles in a row or column share the same label or reach zero weight, the entire row/column collapses and remaining tiles shift downward. Simulate $K$ removal steps and calculate final non-empty cells.
- **Approach:** Custom grid simulation with 2D array compaction and BFS/DFS component tracking.
- **Complexity:** $O(M \times N \times K)$ Time.

### 2. Currency Arbitrage via Rate Matrix
- **Problem Summary:** Given a directed graph representing exchange rates between $N$ currencies, find the maximum conversion rate from currency $A$ to currency $B$ using at most $K$ exchanges.
- **Approach:** Bellman-Ford or Modified Dijkstra using $-\log(\text{rate})$ to transform multiplication to addition.
- **Complexity:** $O(K \times E)$ Time, $O(V)$ Space.

### 3. Autocomplete Search Query Suggestions (Trie + Min-Heap)
- **Problem Summary:** Design a search suggestion system that, after each character of a search word is typed, returns at most 3 lexicographically smallest search results matching the typed prefix.
- **LeetCode Equivalent:** [1268. Search Suggestions System](https://leetcode.com/problems/search-suggestions-system/)
- **Approach:** Trie data structure storing at most 3 top strings at each trie node or Binary Search on sorted vocabulary.
- **Complexity:** $O(N \log N + L \log N)$ Time.

### 4. Continuous Subarray Range Product
- **Problem Summary:** Return the number of contiguous subarrays where the product of elements is strictly less than $K$.
- **LeetCode Equivalent:** [713. Subarray Product Less Than K](https://leetcode.com/problems/subarray-product-less-than-k/)
- **Approach:** Sliding window with two pointers (`left`, `right`). For each valid right pointer, add `(right - left + 1)`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.
