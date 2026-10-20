# Eternal (Zomato) Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🍔

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 65 to 90 minutes
- **Structure Breakdown:**
  1. **Algorithmic Coding Section:** 3 Coding Problems (Medium to Hard difficulty, 50–65 mins).
  2. **Technical MCQs Section:** 13 to 18 MCQs (20–25 mins) covering Core CS Fundamentals (DBMS, OS, Computer Networks) and Machine Learning / Data Science basics.
- **Evaluation Criteria:**
  - Zomato (Eternal group: Zomato, Blinkit, Hyperpure, District) emphasizes deep algorithmic problem-solving and clean edge-case management.
  - Test-case evaluation is strict, with hidden performance checks testing $O(N)$ or $O(N \log N)$ thresholds.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Tree Transformations & Cuts | Hard | Minimizing tree height, subtree cut-and-attach, tree balancing |
| **Very High** | In-Place Swaps & Zero-Fixing | Medium | Sorting non-zero elements while keeping zeros stationary |
| **High** | Combinatorial String Scoring | Medium - Hard | Character frequency powers modulo $10^9+7$, rolling hashes |
| **High** | Grid Geometry & Barrier Traversals | Medium | Cartesian movements with restricted diagonal barriers |
| **Medium** | Core CS & ML MCQs | Medium | SQL joins, normalization, gradient descent, precision vs recall |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Sort Non-Zero Elements Keeping Zeroes Fixed
- **Problem Summary:** Given an array of integers containing zeroes and positive numbers. Sort the non-zero elements in non-decreasing order while keeping all zeroes in their exact original positions.
- **Approach:** Extract all non-zero elements into a separate array, sort it, and write them back sequentially into non-zero positions of the original array.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

### 2. Tree Rebalancing with Subtree Detachment
- **Problem Summary:** Given a tree with $N$ vertices, you are allowed to detach at most one subtree and reattach it to any other node in the tree. Minimize the resulting tree height.
- **Approach:** Tree DP to find tree center/centroid and diameter. Reattaching the disconnected subtree's center to the principal component's center yields the optimal height.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 3. String Score by Frequency Powers Modulo $10^9 + 7$
- **Problem Summary:** Given a string $S$, compute the score of all substrings, where the score of a substring is defined as $\prod (\text{char\_val})^{\text{freq}} \pmod{10^9 + 7}$.
- **Approach:** Sliding window / Contribution method with modular exponentiation.
- **Complexity:** $O(N)$ Time.

### 4. Stone Placement with Adjacent Unit Difference
- **Problem Summary:** Given a tree of $N$ nodes, place stones on nodes such that for every edge $(u, v)$, $|stones[u] - stones[v]| = 1$, and total stones placed is minimized.
- **Approach:** Check bipartiteness of tree (always bipartite for trees). Color nodes with distance parity from root. Assign parity $+1$ and $0$ accordingly.
- **Complexity:** $O(N)$ Time.
