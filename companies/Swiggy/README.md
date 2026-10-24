# Swiggy Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🛵

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **HackerEarth**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  - 3 Algorithmic Coding Questions (Medium to Hard).
  - *Important Language Restriction:* In certain recent campus and off-campus recruitment drives, permitted coding languages were strictly restricted to **Java and Golang** (or Java, C++, Python in earlier rounds).
- **Evaluation Criteria:**
  - Fast-paced consumer internet tech stack (30+ LPA CTC for SDE-1).
  - Emphasis on grid pathfinding, delivery graph logistics, and state DP.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Multi-Source BFS & Matrix Grids:** Delivery kitchen radius, delivery boy travel time, multi-source contagion.
- **Shortest Paths & Routing:** Dijkstra with dynamic surge or traffic penalties, shortest clear path.
- **Dynamic Programming:** Knapsack variations, 2D weight/volume knapsack, maximum delivery batch values.
- **Sliding Window & Two Pointers:** Bounded time interval deliveries, peak surge tracking, container with most water.
- **Topological Sorting:** Dish cooking prerequisites, order delivery staging.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Kitchen Delivery Boy Allocation (Multi-Source BFS)
- **College/Drive:** IIT BHU / NIT Surathkal 2024–2025
- **Problem Summary:** A city map of size $M \times N$ has cloud kitchens (`K`), delivery locations (`D`), traffic obstacles (`X`), and empty roads (`.`). Find the minimum time required for delivery executives departing from all cloud kitchens simultaneously to reach all delivery locations.
- **Constraints:** $1 \le M, N \le 500$.
- **Approach:** Multi-Source BFS initializing queue with all cloud kitchens coordinates. Track maximum distance reached across all `'D'` cells.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 2. Shortest Delivery Route with Dynamic Surge Penalties (Dijkstra)
- **College/Drive:** BITS Pilani 2024–2025
- **Problem Summary:** Given a weighted directed graph of $N$ road intersections with normal travel times $W_{u,v}$. Certain road segments experience dynamic surge multipliers depending on the time of arrival $T$ (i.e., cost becomes $W_{u,v} \times \text{multiplier}$ if $T \in [\text{start}, \text{end}]$). Find the minimum arrival time from kitchen $S$ to customer $C$.
- **Constraints:** $N \le 10^4, E \le 5 \times 10^4$.
- **Approach:** Modified Dijkstra's Algorithm with dynamic edge relaxation based on current cumulative time.
- **Complexity:** $O(E \log V)$ Time.

#### 3. Maximum Order Bundles under Weight & Volume (2D Knapsack)
- **College/Drive:** DTU / NSUT 2024–2025
- **Problem Summary:** A delivery bag has weight capacity $W$ and volume capacity $V$. Given $N$ food orders with weight, volume, and commission, find the maximum commission that can be carried in a single trip.
- **Constraints:** $N \le 100$, $W, V \le 100$.
- **Approach:** 2D 0/1 Knapsack Dynamic Programming:
  $$dp[w][v] = \max(dp[w][v], \text{val} + dp[w - \text{weight}][v - \text{vol}])$$
- **Complexity:** $O(N \times W \times V)$ Time.

#### 4. Continuous Subarray with Maximum Delivery Efficiency
- **College/Drive:** IIIT Delhi 2024–2025
- **Problem Summary:** Given an array of order ratings and tips, find a contiguous subarray of size at least $K$ that maximizes the ratio of $\frac{\sum \text{tips}}{\sum \text{ratings}}$.
- **Constraints:** $1 \le K \le N \le 10^5$.
- **Approach:** Binary Search on the target ratio + Kadane's on transformed array $A[i] = \text{tips}[i] - \text{mid} \times \text{ratings}[i]$.
- **Complexity:** $O(N \log(\text{Precision}))$ Time.

#### 5. Rotting Oranges / Food Spoilage Simulation
- **College/Drive:** On-Campus Slot 1 (2024–2025)
- **Problem Summary:** Calculate minimum minutes until no fresh food items remain on the warehouse grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten food items.
- **Complexity:** $O(M \times N)$ Time.

#### 6. Meeting Rooms II / Delivery Fleet Sizing
- **College/Drive:** Campus Drive Slot 2 (2024)
- **Problem Summary:** Find minimum delivery executives needed to handle all delivery time windows without delay.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- **Approach:** Min-Heap storing active delivery end times or two-pointer start/end sort.
- **Complexity:** $O(N \log N)$ Time.

#### 7. Word Ladder / Sequence Food Order Modification
- **College/Drive:** Off-Campus 2024
- **Problem Summary:** Find shortest transformation sequence between two meal configuration strings.
- **Constraints:** $1 \le beginWord.length \le 10$, $1 \le wordList.length \le 5000$.
- **LeetCode Equivalent:** [127. Word Ladder](https://leetcode.com/problems/word-ladder/)
- **Approach:** Bidirectional BFS checking 1-character mutations against dictionary hash set.
- **Complexity:** $O(M^2 \times N)$ Time.

#### 8. Longest Substring Without Repeating Dishes
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Find longest sequence of distinct restaurant orders.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with hash map storing last seen indices.
- **Complexity:** $O(N)$ Time.

#### 9. Subarray Sum Equals K
- **College/Drive:** Swiggy Bangalore Drive 2024
- **Problem Summary:** Find continuous order sequences summing to target value $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency counter.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Course Schedule II / Order Cooking Prerequisites
- **College/Drive:** Campus Slot 2024
- **Problem Summary:** Given cooking steps and prerequisite pairs, return valid cooking sequence.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm for Topological Sort using indegree array and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Trapping Rain Water
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Network Delay Time / Delivery Hub Ping
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Calculate time for all delivery hubs to receive broadcast from central kitchen.
- **Constraints:** $1 \le N \le 100$, $1 \le edges \le 6000$.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's algorithm with Min-Heap.
- **Complexity:** $O(E \log V)$ Time.

#### 13. Daily Temperatures / Peak Demand Spikes
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Find days to wait for higher order volume.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 14. Coin Change (Fewest Denominations)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Minimum coins needed to make change.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 15. Merge Intervals (Delivery Time Windows)
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Merge all overlapping delivery time slots.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time and merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 16. Product of Array Except Self without Division
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 17. House Robber (1D Dynamic Programming)
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Maximize order value without selecting two adjacent restaurants.
- **Constraints:** $1 \le nums.length \le 100$.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** DP: `dp[i] = max(dp[i-1], dp[i-2] + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 18. Search in Rotated Sorted Array
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find target in rotated sorted array in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 5000$.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking sorted half.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 19. Container With Most Water
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Two pointers inward maximizing area between vertical lines.
- **Constraints:** $2 \le heights.length \le 10^5$.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 20. Shortest Path in Binary Matrix (8-Directional BFS)
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Find shortest path in binary grid from top-left to bottom-right moving in 8 directions.
- **Constraints:** $1 \le n \le 100$.
- **LeetCode Equivalent:** [1091. Shortest Path in Binary Matrix](https://leetcode.com/problems/shortest-path-in-binary-matrix/)
- **Approach:** Breadth-First Search (BFS) level traversal.
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

---

## 💡 Cracking Swiggy SDE OA & Interview Rounds
1. **Language Preparedness (Java / Golang):** Practice standard library data structures (`PriorityQueue`, `HashMap`, `ArrayDeque` in Java) as language choice may be restricted during OA rounds.
2. **Pathfinding & Spatial Heuristics:** Spatial 2D/3D grids (BFS, modified Dijkstra, A*) are central to Swiggy's delivery logistics problems.
3. **Handle Edge Cases Early:** Check for disconnected delivery nodes, empty order batches, zero capacity bags, and matrix boundary limits.
