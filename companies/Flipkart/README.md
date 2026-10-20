# Flipkart Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🛒

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **SHL** (Primary for SDE-1) / **HackerEarth** (Flipkart GRiD)
- **Duration:** 90 minutes (3 Coding Questions)
- **Difficulty Breakdown:**
  - Question 1: Easy to Medium (Arrays, Strings, Greedy logic)
  - Question 2: Medium (Trees, Graphs, Sorting, Interval Scheduling)
  - Question 3: Hard (Complex 2D Dynamic Programming, Matrix Paths, Constructive Algorithms)
- **Scoring & Cutoff:** 
  - Partial marks are awarded based on hidden test cases cleared.
  - Solving 2 questions completely + partial test cases on the 3rd usually guarantees an interview shortlist.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Dynamic Programming:** 2D/3D state DP, knapsack with multiple constraints, subsequence selection.
- **Graphs & BFS/DFS:** Shortest path on grid, component counting, topological order in supply chains.
- **Greedy & Interval Scheduling:** Order batching, warehouse delivery intervals, meeting room variants.
- **Strings & Frequency Matching:** Substring permutation queries, anagram substrings under threshold.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Delivery Drone Path / Minimum Fuel Route (Flipkart GRiD 2024)
- **College/Drive:** Flipkart GRiD National Finals 2024
- **Problem Summary:** A drone must deliver packages between cities connected by bi-directional flight routes with fuel costs. At each city, the drone can refuel up to a tank capacity $C$. Find the minimum total fuel cost or return -1 if impossible.
- **Approach:** Modified Dijkstra's Algorithm maintaining `(current_cost, city, fuel_remaining)` state in a priority queue.
- **Complexity:** $O(E \log(V \times C))$.

#### 2. Maximum Delivery Slots (Weighted Job Scheduling)
- **College/Drive:** IIT Roorkee / IIT Kharagpur 2024
- **Problem Summary:** Given $N$ delivery requests with start time, end time, and customer value. Find the maximum total value such that no two delivery slots overlap.
- **LeetCode Equivalent:** [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)
- **Approach:** Dynamic Programming combined with Binary Search (sort jobs by end time, `dp[i] = max(dp[i-1], job.val + dp[prev_non_overlapping])`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 3. K-Consecutive Array Reconstruction (Constructive Algorithm)
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** Given integers $N$ and $K$. Rearrange elements from $1$ to $N$ such that for any two consecutive segments of size $K$, the difference between their sums is at most 1.
- **Approach:** Mathematical pattern and constructive sorting balancing alternate odd/even index placements.
- **Complexity:** $O(N)$ Time.

#### 4. Maximum String Subsets Matching Binary Constraints (2D Knapsack)
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Summary:** You are given an array of binary strings `strs` and two integers $m$ and $n$. Return the size of the largest subset of `strs` such that there are at most $m$ 0's and $n$ 1's in the subset.
- **LeetCode Equivalent:** [474. Ones and Zeroes](https://leetcode.com/problems/ones-and-zeroes/)
- **Approach:** 2D 0/1 Knapsack Dynamic Programming.
- **Complexity:** $O(\text{len}(strs) \times m \times n)$ Time.

#### 5. Shortest Subarray with Sum at Least K (Monotonic Deque)
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Summary:** Return the length of the shortest, non-empty, contiguous subarray of `nums` with sum at least $k$. Array may contain negative numbers.
- **LeetCode Equivalent:** [862. Shortest Subarray with Sum at Least K](https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/)
- **Approach:** Prefix sums with Monotonic Increasing Deque storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Course Schedule II / Supply Chain Dependencies
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Valid sequence of warehouse batch operations.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Complexity:** $O(V + E)$ Time.

#### 7. Longest Increasing Subsequence
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Patience sorting binary search for LIS.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Complexity:** $O(N \log N)$ Time.

#### 8. Meeting Rooms II / Staging Docks
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Minimum packing bays needed for overlapping delivery times.
- **LeetCode Equivalent:** [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- **Complexity:** $O(N \log N)$ Time.

#### 9. Trapping Rain Water
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Calculate total water trapped in warehouse drain contours.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 10. Coin Change (Fewest Notes)
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Minimum currency notes to pay delivery cash-on-delivery balance.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Complexity:** $O(N \times \text{amount})$ Time.
