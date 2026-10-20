# Databricks Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🧱

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **CodeSignal** (General Coding Assessment - GCA Framework) / **HackerRank**
- **Test Duration:** 70 minutes (4 Tasks)
- **Cutoff Benchmark:** Databricks maintains one of the highest technical screening bars in the industry. On CodeSignal's 300–850 scoring scale, a score of **$\ge 830 - 840$** (flawless execution with near-optimal time/space complexity on all 4 tasks) is typically necessary to move forward to the technical rounds.
- **Evaluation Criteria:** Clean production-level design, handling edge cases, and high computational efficiency on distributed-style data stream problems.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Data Stream Simulation & Parsing | Medium - Hard | Processing Unix-like command logs, tracking state machines, CIDR block matching |
| **Very High** | Directed Acyclic Graphs (DAGs) | Hard | Topological sort, task dependency resolution, cycle detection, path counting |
| **High** | Specialized Trees & Intervals | Medium - Hard | Custom tree traversals, interval intersections, sliding window aggregation |
| **High** | Class & State Management Design | Hard | Custom iterators, sluggish arrays, snapshot memory data structures |
| **Medium** | Advanced Dynamic Programming | Hard | Grid transformations, multi-dimensional state transitions |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Unix File System Path Parser & Simplifier
- **Problem Summary:** Given an absolute path for a Unix-style file system, which begins with a slash `'/'`. Transform this path to its simplified canonical path.
- **LeetCode Equivalent:** [71. Simplify Path](https://leetcode.com/problems/simplify-path/)
- **Approach:** Split by `'/'`, process directory tokens using a Stack. Ignore `.` and empty strings; pop for `..`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 2. Task Dependency Scheduling / Course Schedule III
- **Problem Summary:** You are given $N$ computing tasks with dependencies forming a Directed Acyclic Graph (DAG). Each task has a duration $D_i$ and a deadline $T_i$. Schedule the maximum number of tasks without missing deadlines.
- **LeetCode Equivalent:** [630. Course Schedule III](https://leetcode.com/problems/course-schedule-iii/)
- **Approach:** Sort tasks by deadline; maintain a Max-Heap of running durations. If total duration exceeds deadline, greedily remove the longest task seen so far.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

### 3. Sluggish Array / Range Modification Tracking
- **Problem Summary:** Design a data structure that supports range additions `add(l, r, val)` and point queries `get(index)` in $O(1)$ amortized time.
- **Approach:** Difference array (Prefix Sum technique) or Lazy Propagation on Segment Tree.
- **Complexity:** $O(1)$ range updates with difference array, $O(N)$ query or $O(\log N)$ with Segment Tree.

### 4. IP Routing Prefix Matching (CIDR)
- **Problem Summary:** Given a list of CIDR network routing rules and a stream of incoming IPv4 destination addresses, return the routing rule with the longest prefix match for each IP.
- **Approach:** Binary Trie storing 32-bit binary representations of network addresses.
- **Complexity:** $O(32) = O(1)$ lookup per IP.
