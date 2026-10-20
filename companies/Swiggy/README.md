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
- **Multi-Source BFS & Matrix Grids:** Delivery kitchen radius, delivery boy travel time.
- **Shortest Paths & Routing:** Dijkstra with dynamic surge or traffic penalties.
- **Dynamic Programming:** Knapsack variations, maximum delivery batch values.
- **Sliding Window:** Bounded time interval deliveries, peak surge tracking.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Kitchen Delivery Boy Allocation (Multi-Source BFS)
- **College/Drive:** IIT BHU / NIT Surathkal 2024
- **Problem Statement:** A city map of size $M \times N$ has cloud kitchens (`K`), delivery locations (`D`), traffic obstacles (`X`), and empty roads (`.`). Find the minimum time required for delivery executives departing from all cloud kitchens simultaneously to reach all delivery locations.
- **Approach:** Multi-Source BFS initializing queue with all cloud kitchens coordinates. Track maximum distance reached across all `'D'` cells.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 2. Shortest Delivery Route with Dynamic Surge Penalties (Dijkstra)
- **College/Drive:** BITS Pilani 2024
- **Problem Statement:** Given a weighted directed graph of $N$ road intersections with normal travel times $W_{u,v}$. Certain road segments experience dynamic surge multipliers depending on the time of arrival $T$ (i.e., cost becomes $W_{u,v} \times \text{multiplier}$ if $T \in [\text{start}, \text{end}]$). Find the minimum arrival time from kitchen $S$ to customer $C$.
- **Approach:** Modified Dijkstra's Algorithm with dynamic edge relaxation based on current cumulative time.
- **Complexity:** $O(E \log V)$ Time.

#### 3. Maximum Order Bundles under Weight & Volume (2D Knapsack)
- **College/Drive:** DTU / NSUT 2024
- **Problem Statement:** A delivery bag has weight capacity $W$ and volume capacity $V$. Given $N$ food orders with weight, volume, and commission, find the maximum commission that can be carried in a single trip.
- **Approach:** 2D 0/1 Knapsack Dynamic Programming:
  $$dp[w][v] = \max(dp[w][v], \text{val} + dp[w - \text{weight}][v - \text{vol}])$$
- **Complexity:** $O(N \times W \times V)$ Time.

#### 4. Continuous Subarray with Maximum Delivery Efficiency
- **College/Drive:** IIIT Delhi 2024
- **Problem Statement:** Given an array of order ratings and tips, find a contiguous subarray of size at least $K$ that maximizes the ratio of $\frac{\sum \text{tips}}{\sum \text{ratings}}$.
- **Approach:** Binary Search on the target ratio + Kadane's on transformed array $A[i] = \text{tips}[i] - \text{mid} \times \text{ratings}[i]$.
- **Complexity:** $O(N \log(\text{Precision}))$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Rotting Oranges / Food Spoilage Simulation
- **College/Drive:** On-Campus Slot 1 (2023)
- **Problem Statement:** Calculate minimum minutes until no fresh food items remain on the warehouse grid.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time.

#### 6. Meeting Rooms II / Delivery Fleet Sizing
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Find minimum delivery executives needed to handle all delivery time windows without delay.
- **LeetCode Equivalent:** [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- **Complexity:** $O(N \log N)$ Time.

#### 7. Word Ladder / Sequence Food Order Modification
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Find shortest transformation sequence between two meal configuration strings.
- **LeetCode Equivalent:** [127. Word Ladder](https://leetcode.com/problems/word-ladder/)
- **Complexity:** $O(M^2 \times N)$ Time.

#### 8. Longest Substring Without Repeating Dishes
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Find longest sequence of distinct restaurant orders.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time.
