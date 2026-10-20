# Apple Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🍎

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **CodeSignal**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  - **Coding Section:** 2 to 3 Coding Problems (Easy-Medium to Medium-Hard).
  - **Core CS Section:** 10 to 15 MCQs covering Operating Systems (Processes, Threads, Semaphores), Computer Networks (TCP/UDP, DNS), and C++ / Swift memory management.
- **Evaluation Criteria:** Apple places extreme emphasis on clean, idiomatic code, handling edge cases, and algorithmic efficiency. On CodeSignal, strict test-case coverage determines the candidate's invitation to team interviews.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Strings & Text Parsing | Medium | Substring matching, custom compression, balanced delimiters |
| **Very High** | Arrays & Sliding Window | Medium | Minimum operations, maximum subarray sum, monotonic properties |
| **High** | Trees & Graph Traversal | Medium | BFS / DFS, Tree level-order variations, connected components |
| **High** | Dynamic Programming | Medium - Hard | Knapsack variants, word break, matrix minimum path sums |
| **Medium** | System & Low-Level Concepts | Medium | Memory layouts, reference counting / ARC (Automatic Reference Counting), concurrency |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Minimum Operations to Reduce Array / Target Transform
- **Problem Summary:** Given an array of integers `nums` and an integer `x`. In one operation, you can remove either the leftmost or the rightmost element from the array and subtract its value from `x`. Return the minimum number of operations to reduce `x` to exactly `0`, or `-1` if impossible.
- **LeetCode Equivalent:** [1658. Minimum Operations to Reduce X to Zero](https://leetcode.com/problems/minimum-operations-to-reduce-x-to-zero/)
- **Approach:** Invert the problem: Find the longest contiguous subarray whose sum equals $\sum nums - x$ using a sliding window.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 2. Word Break & Dictionary Matching
- **Problem Summary:** Given a string $s$ and a dictionary of strings `wordDict`, return `true` if $s$ can be segmented into a space-separated sequence of one or more dictionary words.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Approach:** 1D Dynamic Programming: `dp[i]` is true if a valid prefix exists such that `dp[j]` is true and $s[j \dots i]$ is in the dictionary (or using a Trie).
- **Complexity:** $O(N^2)$ Time, $O(N)$ Space.

### 3. Maximum Number of Events That Can Be Attended
- **Problem Summary:** You are given an array of `events` where `events[i] = [startDay, endDay]`. You can attend at most one event on any given day. Return the maximum number of events you can attend.
- **LeetCode Equivalent:** [1353. Maximum Number of Events That Can Be Attended](https://leetcode.com/problems/maximum-number-of-events-that-can-be-attended/)
- **Approach:** Sort events by start day, maintain a Min-Heap of end days for active events, and greedily attend the event ending earliest each day.
- **Complexity:** $O(D + N \log N)$ where $D$ is max days.

### 4. Tree Vertical Level Sum
- **Problem Summary:** Given a binary tree, return the vertical sum of all nodes lying on the same vertical line (assigning root coordinate 0, left child -1, right child +1).
- **Complexity:** $O(N \log N)$ or $O(N)$ with HashMap + BFS.

---

## 🧠 Frequent CS MCQs Asked in Apple OA
1. **Thread vs Process Memory:** Which segments are shared between threads of the same process? (Code/Text, Data, Heap, File descriptors are shared; Stack and Registers are private).
2. **Swift ARC / C++ Smart Pointers:** What causes retain cycles and how are they broken? (Strong reference cycles cause memory leaks; resolved via `weak` or `unowned` references).
3. **TCP vs UDP in Streaming:** Why do latency-critical voice applications prefer UDP? (No head-of-line blocking, no retransmission overhead).
