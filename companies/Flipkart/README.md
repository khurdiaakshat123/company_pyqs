# Flipkart Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🛒

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **SHL** (Primary for On-Campus / Off-Campus SDE-1) / **HackerEarth** (Flipkart GRiD Hackathon)
- **Duration:** 90 minutes (3 Coding Questions)
- **Difficulty Breakdown:**
  - Question 1: Easy to Medium (Arrays, Strings, Greedy logic)
  - Question 2: Medium (Trees, Graphs, Sorting, Interval Scheduling)
  - Question 3: Hard (Complex 2D Dynamic Programming, Matrix Paths, Constructive Algorithms)
- **Scoring & Cutoff:** 
  - Partial marks are awarded based on hidden test cases cleared.
  - Solving 2 questions completely + partial test cases on the 3rd usually guarantees an interview shortlist.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

Flipkart problem statements are intentionally lengthy and formatted as real-world e-commerce inventory, logistics, or delivery stories:

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Dynamic Programming | Hard | 2D/3D state DP, Knapsack with multiple constraints, Subsequence selection |
| **Very High** | Graphs & BFS/DFS | Medium - Hard | Shortest path on grid, component counting, topological order in supply chains |
| **High** | Greedy & Interval Scheduling | Medium | Order batching, warehouse delivery intervals, meeting room variants |
| **High** | Strings & Frequency Matching | Medium | Substring permutation queries, anagram substrings under threshold |
| **Medium** | Constructive Algorithms | Medium - Hard | Array rearrangement under adjacent difference bounds |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Delivery Drone Path / Minimum Fuel Route (Flipkart GRiD)
- **Problem Summary:** A drone must deliver packages between cities connected by bi-directional flight routes with fuel costs. At each city, the drone can refuel up to a tank capacity $C$. Find the minimum total fuel cost or return -1 if impossible.
- **Approach:** Modified Dijkstra's Algorithm maintaining `(current_cost, city, fuel_remaining)` state in a priority queue.
- **Complexity:** $O(E \log(V \times C))$.

### 2. Maximum Delivery Slots (Interval Scheduling with Weights)
- **Problem Summary:** Given $N$ delivery requests with start time, end time, and customer value. Find the maximum total value such that no two delivery slots overlap.
- **LeetCode Equivalent:** [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)
- **Approach:** Dynamic Programming combined with Binary Search (sort jobs by end time, `dp[i] = max(dp[i-1], job.val + dp[prev_non_overlapping])`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

### 3. K-Consecutive Array Reconstruction
- **Problem Summary:** Given integers $N$ and $K$. Rearrange elements from $1$ to $N$ such that for any two consecutive segments of size $K$, the difference between their sums is at most 1.
- **Approach:** Mathematical pattern and constructive sorting balancing alternate odd/even index placements.
- **Complexity:** $O(N)$ Time.

### 4. Maximum String Subsets Matching Binary Constraints
- **Problem Summary:** You are given an array of binary strings `strs` and two integers $m$ and $n$. Return the size of the largest subset of `strs` such that there are at most $m$ 0's and $n$ 1's in the subset.
- **LeetCode Equivalent:** [474. Ones and Zeroes](https://leetcode.com/problems/ones-and-zeroes/)
- **Approach:** 2D 0/1 Knapsack Dynamic Programming.
- **Complexity:** $O(\text{len}(strs) \times m \times n)$ Time.

---

## 💡 Cracking Flipkart OA: Proven Tips
1. **Decouple the Story from the Algorithm:** Flipkart uses long paragraphs describing warehouses, carts, and delivery vans. Immediately extract the mathematical inputs, bounds, and output goal.
2. **Prioritize Questions 1 & 2:** Ensure zero compile errors and full test-case passage on the first two problems within 45–50 minutes before tackling the hard DP problem.
