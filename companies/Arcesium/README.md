# Arcesium Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Core CS Fundamentals MCQs (20 mins)** – 10 to 15 MCQs covering Operating Systems, DBMS/SQL, OOPs (Java/C++), and Computer Networks.
  2. **Section 2: Algorithmic Coding (60 mins, 2 to 3 Questions)** – Medium to Hard difficulty problems.
- **Evaluation Criteria:**
  - Arcesium (spun out of D. E. Shaw) provides post-trade investment lifecycle and asset management software.
  - Stringent evaluation of time and space complexity with emphasis on clean edge-case management.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Graph Theory & Connectivity | Medium - Hard | Bipartiteness check, cycle detection, multi-source BFS, reachability |
| **Very High** | Strings & Chunk Reversals | Medium | Interval modifications, $k$-step substring reversals, anagram balancing |
| **High** | Dynamic Programming & Sliding Window | Medium - Hard | Subarray optimizations, bounded coin exchange, sequence scoring |
| **High** | Core CS & OOP MCQs | Medium | Java Garbage Collection, SQL indexing, deadlock conditions, TCP handshake |
| **Medium** | Priority Queues & Log Processing | Medium | Sequential payload ordering, time-series trade reconciliation |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Hostile Groups / Bipartite Graph Verification
- **Problem Summary:** You are given $N$ people and an array of pairs representing hostile relationships. Determine if it is possible to split the people into two distinct groups such that no two people in the same group are hostile toward each other.
- **LeetCode Equivalent:** [886. Possible Bipartition](https://leetcode.com/problems/possible-bipartition/)
- **Approach:** Graph 2-Coloring via Breadth-First Search (BFS) or Depth-First Search (DFS). If an adjacent neighbor already has the same color, return `false`.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

### 2. Reverse String Chunks in Intervals of K
- **Problem Summary:** Given a string $s$ and an integer $k$, reverse the first $k$ characters for every $2k$ characters counting from the start of the string.
- **LeetCode Equivalent:** [541. Reverse String II](https://leetcode.com/problems/reverse-string-ii/)
- **Approach:** Step forward by $2k$ in a loop; reverse the subsegment $[i, \min(i + k - 1, n - 1)]$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 3. Investment Portfolio Cash Settlement
- **Problem Summary:** Given a sequence of $N$ daily trade cash inflows and outflows, determine the minimum initial capital required so that the running balance never drops below zero at any point.
- **Approach:** Prefix sum scan tracking the minimum running balance; required initial capital is $\max(0, -\text{min\_prefix\_sum})$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 4. Course Schedule & Prerequisite Validation
- **Problem Summary:** Given $N$ modules and their prerequisite dependencies, determine if it is possible to finish all modules.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Kahn's Algorithm (Topological Sort using in-degrees).
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.
