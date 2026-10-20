# Amazon Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 📦

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Structure & Duration:**
  - **Part 1: Coding Challenge (90 minutes)** – 2 algorithmic coding problems (Medium to Hard).
  - **Part 2: Work Style Assessment (15–20 minutes)** – Situational judgment test evaluating Amazon's 16 Leadership Principles (LPs).
- **Proctoring:** Webcam enabled, tab-switch monitoring, copy-paste disabled inside editor.
- **Passing Cutoff:** Full score (100% test cases on both questions) is heavily prioritized for direct interview invites. The Work Style Assessment score is equally weighted.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Sliding Window & Two Pointers | Medium | Substring matching, maximum/minimum segment costs, frequency balance |
| **Very High** | Heaps & Priority Queues | Medium - Hard | Top K frequent elements, minimum cost to connect ropes/servers, median stream |
| **High** | Dynamic Programming | Medium - Hard | Knapsack variants, bounded capacity choices, stock buy & sell variations |
| **High** | Breadth-First Search (BFS) | Medium | Multi-source BFS on 2D grid (routing packages, infection/rotting grids) |
| **High** | Monotonic Stack / Queue | Medium - Hard | Next greater element, subarray minimums sum, largest rectangle in histogram |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Amazon Fulfillment Centers / Minimum Keypresses
- **Problem Summary:** Given a string of lowercase letters representing characters typed on an older keypad where each key can hold multiple characters. Assign letters to keys 1–9 such that total keypresses to type the string is minimized.
- **Approach:** Count character frequencies, sort descending, assign top 9 most frequent letters to 1 press each, next 9 to 2 presses, remaining to 3 presses.
- **Complexity:** $O(N + 26 \log 26) = O(N)$ Time.

### 2. Maximum Delivery Center Throughput (Parcel Optimization)
- **Problem Summary:** Given $N$ servers, each with a processing speed. Divide servers into triplets such that the second maximum of each triplet is maximized overall.
- **Approach:** Sort speeds, pick the largest elements greedily to maximize the median of triplets.
- **Complexity:** $O(N \log N)$ Time.

### 3. Total Cost to Connect Servers / Minimal Connected Cost
- **Problem Summary:** Given server connection costs with an array of positive integers, repeatedly combine the two smallest servers. The cost of connecting is the sum of their weights until one connected component remains.
- **LeetCode Equivalent:** [1167. Minimum Cost to Connect Sticks](https://leetcode.com/problems/minimum-cost-to-connect-sticks/)
- **Approach:** Min-Heap (`std::priority_queue` with greater comparator in C++ / `heapq` in Python).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

### 4. Count Maximum Contiguous Channel Buffers (Subarray Range Sum)
- **Problem Summary:** Find the sum of `(max(subarray) - min(subarray))` across all contiguous subarrays of an array of size $N$.
- **Constraints:** $1 \le N \le 10^5$.
- **Approach:** Monotonic stack to find the count of subarrays where each element acts as the maximum and minimum respectively in $O(N)$.
- **LeetCode Equivalent:** [2104. Sum of Subarray Ranges](https://leetcode.com/problems/sum-of-subarray-ranges/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

## 🧭 Amazon Work Style Assessment (Behavioral Section)
- Select the option that aligns strongest with Amazon's core LPs:
  - **Customer Obsession:** Prioritize long-term customer trust over short-term revenue.
  - **Ownership:** Never say "that's not my job"; accept accountability for dependencies.
  - **Bias for Action:** Speed matters in business; calculated risk-taking is valued over endless analysis.
  - **Deliver Results:** Rise to the occasion despite obstacles; meet critical deadlines.
