# Infosys Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🏢

## 📌 OA Overview & Test Logistics
Infosys conducts recruitment through tiered tracks via **HackerEarth** (for SP & DSE roles) and **Infosys Internal Assessment Portal**:
1. **Specialist Programmer (SP - 9.5 LPA) & Digital Specialist Engineer (DSE - 6.25 LPA):**
   - **Platform:** **HackerEarth**
   - **Duration:** 180 minutes (3 hours)
   - **Format:** 3 Coding Questions (No MCQs, No Aptitude)
     - Question 1: Easy-Medium (DSE benchmark)
     - Question 2: Medium-Hard (DSE/SP benchmark)
     - Question 3: Hard (SP benchmark - Advanced DP, Trees/Graphs)
2. **Systems Engineer (SE - 3.6 LPA):**
   - **Duration:** 100 minutes (54 Questions)
   - **Sections:** Mathematical Ability (10 Q), Logical Reasoning (15 Q), Verbal Ability (20 Q), Pseudocode (5 Q), Numerical Puzzles (4 Q).

---

## 🎯 SP & DSE Coding Exam Pattern (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Dynamic Programming | Medium - Hard | State DP, Tree DP, Digit DP, Partition DP, Subarray score maximization |
| **Very High** | Graph & Tree Algorithms | Medium - Hard | Shortest path, Cycle detection, Tree diameter, Rerooting, Multi-source BFS |
| **High** | Number Theory & Combinatorics | Medium | Modular arithmetic, Prime factorization (Sieve of Eratosthenes), GCD |
| **High** | Greedy & Disjoint Sets (DSU) | Medium | Component connectivity, Kruskal's MST, Interval compression |
| **Medium** | Bit Manipulation | Medium | Bitwise AND/OR/XOR of subarrays, set bit parity |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Beautiful Path in Weighted Directed Graph (SP Track)
- **Problem Summary:** Given a directed graph with $N$ vertices and $M$ edges, where each vertex has an English letter. A path is called "beautiful" if the frequency of the most frequent letter on that path is maximized. Return this maximum frequency, or $-1$ if the graph contains a cycle reachable along a path.
- **Approach:** Topological Sort (Kahn's Algorithm) combined with DP: `dp[u][char]` stores the maximum frequency of `char` on any path ending at node `u`. If topological sort cannot process all reachable nodes, a cycle exists.
- **Complexity:** $O(26 \times (V + E))$ Time, $O(26 \times V)$ Space.

### 2. Minimum Operations to Equalize Subarrays (DSE Track)
- **Problem Summary:** Given an array $A$ of size $N$, partition it into $K$ contiguous subarrays. In each operation, you can increment or decrement any element by 1. Find the minimum operations to make all elements within each subarray equal to the median of that subarray.
- **Approach:** Prefix sums on sorted subarrays or quickselect / median calculation with prefix array.
- **Complexity:** $O(N \log N)$ Time.

### 3. Maximum Subsequence Value under Parity Constraints (SP Track)
- **Problem Summary:** Select a subsequence from an array such that no two adjacent chosen elements have the same parity (alternating odd/even) and the sum is maximized.
- **Approach:** 1D DP maintaining two running maximums: `dp_even` (ending with an even number) and `dp_odd` (ending with an odd number).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 4. Tree Node Deletion to Minimize Components
- **Problem Summary:** Given a tree with $N$ nodes, delete at most $K$ edges such that each resulting connected component has an even sum of node values.
- **Approach:** Post-order DFS. Calculate subtree sums from the leaves upward; whenever a subtree sum is even, greedily cut that edge.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

## 💡 Cracking Infosys SP/DSE
1. **Partial Scoring:** HackerEarth grants partial points for passing $X$ out of $Y$ test cases. Always implement at least a working $O(N^2)$ solution if the optimal $O(N \log N)$ approach is elusive.
2. **SP Cutoff:** Clearing 2 full questions + partial on the 3rd typically qualifies you for the SP (9.5 LPA) interview; clearing 1 full + 1 partial qualifies for DSE (6.25 LPA).
