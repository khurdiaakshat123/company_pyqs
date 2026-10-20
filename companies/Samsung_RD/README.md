# Samsung R&D (SRIB / SRI-N) Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) 📱

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Samsung SWC (Software Competency Platform)** / Custom HackerEarth
- **Test Duration:** 180 minutes (3 hours)
- **Format:** **1 Single Comprehensive Algorithmic Problem**
- **The "50 Test Cases" Rule:**
  - The assessment provides ~10 public test cases and runs ~40 hidden test cases (total ~50 test cases).
  - **Passing 50/50 test cases is MANDATORY.** Scoring 49/50 results in an automatic fail with zero partial credit.
- **Environment Restrictions:** In traditional Samsung SWC examinations, usage of standard template libraries (STL like `std::vector`, `std::map`, `std::queue`) can be restricted or heavily monitored; candidates are strongly advised to know manual implementations using static arrays.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Backtracking & Recursion with Pruning:** N-Queens variants, grid path generation, branch-and-bound pruning.
- **Dynamic Programming with Bitmask:** Traveling Salesperson Problem (TSP), state compression, burst balloons.
- **Multi-Source BFS / Grid Traversals:** Wormhole networks, explosion propagation, shortest path with obstacles.
- **Simulation & State Search:** Board games, pipe connections, laser/mirror reflections.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Wormhole / Space Teleporter (Samsung Signature Classic)
- **College/Drive:** IIT Roorkee / IIT BHU 2024
- **Problem Summary:** You want to travel from source $(S_x, S_y)$ to destination $(D_x, D_y)$. The normal cost of walking between $(x_1, y_1)$ and $(x_2, y_2)$ is $|x_1 - x_2| + |y_1 - y_2|$ (Manhattan distance). There are $N$ bidirectional wormholes ($N \le 10$). Entering a wormhole from one end transports you to the other end with a specified fixed cost $W_i$. You can enter a wormhole at either end, and you can use any wormhole at most once. Find the minimum cost to reach destination.
- **Approach:** Backtracking / DFS exploring all $2^N \times N!$ permutations or Dijkstra on a graph of $(2N + 2)$ nodes.
- **Complexity:** $O((2N)!)$ with pruning or $O(V^2 \log V)$ with Dijkstra.

#### 2. Burst Balloons / Missile Defense System (Interval DP)
- **College/Drive:** BITS Pilani / NIT Trichy 2024
- **Problem Summary:** Given $n$ targets, indexed from $0$ to $n - 1$. Each target has a score `nums[i]`. If you burst target $i$, you get `nums[i - 1] * nums[i] * nums[i + 1]` points. Find the maximum points you can collect.
- **LeetCode Equivalent:** [312. Burst Balloons](https://leetcode.com/problems/burst-balloons/)
- **Approach:** Interval Dynamic Programming: `dp[i][j] = max(dp[i][j], dp[i][k] + dp[k][j] + nums[i]*nums[k]*nums[j])` where $k$ is the LAST balloon burst in interval $(i, j)$.
- **Complexity:** $O(N^3)$ Time, $O(N^2)$ Space.

#### 3. Fishermen and Gates Problem (Backtracking with Pruning)
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** There are $N$ spots along a river bank and 3 gates. Each gate has a specific coordinate and a number of fishermen waiting to enter. Each fisherman must occupy an empty spot, and the distance walked is $|spot - gate| + 1$. Find the minimum total distance walked by all fishermen.
- **Approach:** Permutations of gates ($3! = 6$ orders), backtracking placing fishermen into closest available adjacent spots.
- **Complexity:** $O(6 \times 2^3 \times N)$ with greedy tie-breaking.

#### 4. Endoscope / Pipe Connection Simulation (BFS on States)
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Summary:** An endoscope is inserted into a grid of connected pipes (7 types of pipes: horizontal, vertical, L-shaped, etc.). Given the entry coordinate and maximum cable length $L$, calculate the total number of pipe segments reachable.
- **Approach:** BFS tracking valid connection matching between adjacent pipe ports.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 5. Aeroplane Bombing Game / 2D Grid Simulation
- **College/Drive:** Samsung SRI-N Campus 2024
- **Problem Summary:** A plane starts at the bottom of an $N \times 5$ grid moving upwards row-by-row. Grid cells contain coins (+1), enemies, or empty space. The plane can detonate a bomb once to destroy all enemies in the next 5 consecutive rows. Find the maximum coins the plane can collect before dying.
- **Approach:** 3D Dynamic Programming / Backtracking: `solve(row, col, bomb_used, bomb_timer)`.
- **Complexity:** $O(N \times 5 \times 2 \times 6)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Travelling Salesperson Problem (TSP) with Bitmask DP
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Minimum cost Hamiltonian cycle visiting all $N$ cities ($N \le 16$).
- **Approach:** Bitmask DP: $dp[mask][city] = \min(cost[city][nxt] + dp[mask \cup (1 \ll nxt)][nxt])$.
- **Complexity:** $O(N^2 \cdot 2^N)$ Time.

#### 7. Bipartite Graph Coloring
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Check if graph nodes can be 2-colored without adjacent conflict.
- **LeetCode Equivalent:** [785. Is Graph Bipartite?](https://leetcode.com/problems/is-graph-bipartite/)
- **Complexity:** $O(V + E)$ Time.

#### 8. Minimum Knight Moves on Infinite Chessboard
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Minimum knight moves from $(0, 0)$ to $(x, y)$.
- **LeetCode Equivalent:** [1197. Minimum Knight Moves](https://leetcode.com/problems/minimum-knight-moves/)
- **Approach:** BFS with coordinate symmetry reduction to quadrant 1.
- **Complexity:** $O(|x \times y|)$ Time.

#### 9. Warmup: Cycle Detection in Undirected Graph
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Detect if an undirected graph contains a cycle using DFS or DSU.
- **Complexity:** $O(V + E)$ Time.

#### 10. Maximum Subarray Sum
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Kadane's algorithm.
- **Complexity:** $O(N)$ Time.
