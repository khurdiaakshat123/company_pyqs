# Samsung R&D (SRIB / SRI-N) Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) 📱

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Samsung SWC (Software Competency Platform)** / Custom HackerEarth
- **Test Duration:** 180 minutes (3 hours)
- **Format:** **1 Single Comprehensive Algorithmic Problem** (Occasionally 1 Large + 1 Medium)
- **The "50 Test Cases" Rule:**
  - The assessment provides ~10 public test cases and runs ~40 hidden test cases (total ~50 test cases).
  - **Passing 50/50 test cases is MANDATORY.** Scoring 49/50 results in an automatic fail with zero partial credit.
- **Environment Restrictions:** In traditional Samsung SWC examinations, usage of standard template libraries (STL like `std::vector`, `std::map`, `std::queue`) can be restricted or heavily monitored; candidates are strongly advised to know manual implementations using static arrays.
- **Core Skillset:** Backtracking with aggressive branch-and-bound pruning, Bitmask Dynamic Programming, Multi-Source BFS, and 2D Grid physical simulations.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Backtracking & Recursion with Pruning:** N-Queens variants, grid path generation, branch-and-bound pruning.
- **Dynamic Programming with Bitmask:** Traveling Salesperson Problem (TSP), state compression, burst balloons.
- **Multi-Source BFS / Grid Traversals:** Wormhole networks, explosion propagation, shortest path with obstacles.
- **Simulation & State Search:** Board games, pipe connections, laser/mirror reflections.
- **Binary Search on Answer:** Allocation problems, minimal jump height, sensor range maximization.

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
- **Approach:** Permutations of gates ($3! = 6$ orders), backtracking placing fishermen into closest available adjacent spots with tie-breaking branching.
- **Complexity:** $O(6 \times 2^3 \times N)$ with branch-and-bound pruning.

#### 4. Endoscope / Pipe Connection Simulation (BFS on States)
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Summary:** An endoscope is inserted into a grid of connected pipes (7 types of pipes: horizontal, vertical, L-shaped, etc.). Given the entry coordinate and maximum cable length $L$, calculate the total number of pipe segments reachable.
- **Approach:** BFS tracking valid connection matching between adjacent pipe ports (North, South, East, West compatibility matrices).
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 5. Aeroplane Bombing Game / 2D Grid Simulation
- **College/Drive:** Samsung SRI-N Campus 2024
- **Problem Summary:** A plane starts at the bottom of an $N \times 5$ grid moving upwards row-by-row. Grid cells contain coins (+1), enemies, or empty space. The plane can detonate a bomb once to destroy all enemies in the next 5 consecutive rows. Find the maximum coins the plane can collect before dying.
- **Approach:** 3D Dynamic Programming / Backtracking: `solve(row, col, bomb_used, bomb_timer)`.
- **Complexity:** $O(N \times 5 \times 2 \times 6)$ Time.

#### 6. Rock Climbing / Minimal Jump Height
- **College/Drive:** IIT Kanpur / IIT Kharagpur 2024
- **Problem Summary:** Given an $M \times N$ grid of rocks ($1$) and empty spaces ($0$), you start at the bottom-left corner and want to reach the goal flag at the top. From any rock, you can walk horizontally left/right to adjacent rocks. You can also jump vertically up or down up to $H$ units between rocks in the same column. Find the minimum integer jump height $H$ required to reach the goal.
- **Approach:** Binary Search on jump height $H \in [0, M]$. For each mid $H$, perform BFS/DFS to verify reachability from start to destination.
- **Complexity:** $O((M \times N) \log M)$ Time, $O(M \times N)$ Space.

#### 7. Kim and Refrigerators (TSP with Fixed Start and End)
- **College/Drive:** DTU / NSUT Delhi 2024
- **Problem Summary:** Mr. Kim starts at his office $(O_x, O_y)$ and must deliver refrigerators to $N$ customers ($N \le 10$) before returning to his home $(H_x, H_y)$. The distance between any two locations is the Manhattan distance. Find the minimum total distance traveled to visit all $N$ customers exactly once.
- **LeetCode Equivalent:** Variation of [943. Find the Shortest Superstring](https://leetcode.com/problems/find-the-shortest-superstring/) / TSP.
- **Approach:** Backtracking permutation search or Bitmask DP: `dp[mask][u]` = minimum distance having visited subset `mask` ending at node `u`. Final step transitions from last node to Home.
- **Complexity:** $O(N^2 \cdot 2^N)$ Time, $O(N \cdot 2^N)$ Space.

#### 8. Laser Beam & Angled Mirror Reflection Grid
- **College/Drive:** Samsung SRIB Campus 2024 / VIT Vellore
- **Problem Summary:** A laser is shot from $(0, 0)$ heading East into an $M \times N$ grid containing flat mirrors inclined at $45^\circ$ (`/` and `\`) and absorptive obstacles (`#`). Reflect the laser ray until it exits the grid, hits an obstacle, or enters an infinite cycle. Calculate the total number of distinct mirrors illuminated.
- **Approach:** State simulation `(r, c, dir)` where `dir` $\in \{\text{North, East, South, West}\}$. Track visited states with a 3D boolean array `visited[r][c][dir]` to detect cycles.
- **Complexity:** $O(M \times N \times 4)$ Time, $O(M \times N)$ Space.

#### 9. Convex Hull / Outer Sensor Boundary (Graham Scan)
- **College/Drive:** IIT BHU / IIT Guwahati 2025
- **Problem Summary:** Given $N$ sensor coordinates on a smart campus floor, find the minimal subset of vertices that form a convex polygon containing all sensor coordinates.
- **LeetCode Equivalent:** [587. Erect the Fence](https://leetcode.com/problems/erect-the-fence/)
- **Approach:** Monotone Chain or Graham Scan algorithm using 2D cross-product orientation tests (`cross(OA, OB) >= 0`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 10. Maximum Energy Path with Solar Recharging Nodes
- **College/Drive:** Samsung SRI-B Off-Campus 2024
- **Problem Summary:** A robot with maximum battery capacity $C$ moves through a directed weighted graph. Traversing edge $e=(u, v)$ consumes $w(e)$ energy. Certain nodes have solar chargers that recharge battery back to $C$. Find the minimum total energy consumed to reach destination without running out of battery, or $-1$ if impossible.
- **Approach:** Modified Dijkstra algorithm where node states are defined by `(node_id, current_battery)`.
- **Complexity:** $O((V \cdot C + E \cdot C) \log(V \cdot C))$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Travelling Salesperson Problem (TSP) with Bitmask DP
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Minimum cost Hamiltonian cycle visiting all $N$ cities ($N \le 16$).
- **Approach:** Bitmask DP: $dp[mask][city] = \min(cost[city][nxt] + dp[mask \cup (1 \ll nxt)][nxt])$.
- **Complexity:** $O(N^2 \cdot 2^N)$ Time.

#### 12. Bipartite Graph Coloring
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Check if graph nodes can be 2-colored without adjacent conflict.
- **LeetCode Equivalent:** [785. Is Graph Bipartite?](https://leetcode.com/problems/is-graph-bipartite/)
- **Complexity:** $O(V + E)$ Time.

#### 13. Minimum Knight Moves on Infinite Chessboard
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Minimum knight moves from $(0, 0)$ to $(x, y)$.
- **LeetCode Equivalent:** [1197. Minimum Knight Moves](https://leetcode.com/problems/minimum-knight-moves/)
- **Approach:** BFS with coordinate symmetry reduction to quadrant 1.
- **Complexity:** $O(|x \times y|)$ Time.

#### 14. Frog Jump Across River with Stone Increments
- **College/Drive:** BITS Goa Campus 2023
- **Problem Summary:** A frog is crossing a river with stones at given units. The frog can only jump forward. If the frog's last jump was $k$ units, its next jump must be either $k - 1$, $k$, or $k + 1$ units. Determine if the frog can reach the last stone.
- **LeetCode Equivalent:** [403. Frog Jump](https://leetcode.com/problems/frog-jump/)
- **Approach:** DP with Hash Map / Set: `dp[stone]` contains set of valid incoming jump sizes $k$.
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

#### 15. Robot Cleaner / Room Cleaning Simulation
- **College/Drive:** NSUT Delhi Campus Hiring 2023
- **Problem Summary:** A robot cleaner is placed in an unknown grid containing obstacles. The robot has APIs: `move()`, `turnLeft()`, `turnRight()`, `clean()`. Clean the entire room without getting trapped.
- **LeetCode Equivalent:** [489. Robot Room Cleaner](https://leetcode.com/problems/robot-room-cleaner/)
- **Approach:** Backtracking DFS with relative coordinates $(r, c)$ and direction offset `d`. Upon returning from a recursive branch, backtrack the physical robot (turn 180, move, turn 180).
- **Complexity:** $O(4 \times (N - M))$ where $N$ is total cells and $M$ is obstacles.

#### 16. Sudoku Solver (Classic Backtracking)
- **College/Drive:** Samsung SWC 2023
- **Problem Summary:** Write a program to solve a Sudoku puzzle by filling the empty cells. Empty cells contain `'.'`.
- **LeetCode Equivalent:** [37. Sudoku Solver](https://leetcode.com/problems/sudoku-solver/)
- **Approach:** Recursive backtracking checking bitmask / boolean validity arrays for row, column, and $3 \times 3$ subgrid.
- **Complexity:** $O(9^m)$ where $m$ is number of blank cells; extremely fast with bitmask pruning.

#### 17. N-Queens with Blocked / Broken Grid Cells
- **College/Drive:** Samsung University Hiring 2023
- **Problem Summary:** Place $N$ non-attacking queens on an $N \times N$ chessboard where a given list of cells are broken (cannot place any queen, but queens can attack through them).
- **Approach:** Backtracking column by column with bitmask tracking of active rows, left diagonals, and right diagonals.
- **Complexity:** $O(N!)$ worst case, pruned rapidly.

#### 18. Aggressive Cows / Magnetic Force Between Balls
- **College/Drive:** Samsung SWC Off-Campus 2023
- **Problem Summary:** Given $N$ stall positions and $K$ cows, assign cows to stalls such that the minimum distance between any two of them is as large as possible.
- **LeetCode Equivalent:** [1552. Magnetic Force Between Two Balls](https://leetcode.com/problems/magnetic-force-between-two-balls/)
- **Approach:** Binary search on minimum distance $D \in [1, \text{pos}[N - 1] - \text{pos}[0]]$. Greedy verification in $O(N)$ time.
- **Complexity:** $O(N \log(\max - \min))$ Time, $O(1)$ Space.

#### 19. Cycle Detection in Undirected Graph
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Detect if an undirected graph contains a cycle using DFS or Disjoint Set Union (DSU).
- **Complexity:** $O(V + E)$ Time, $O(V)$ Space.

#### 20. Contiguous Subarray with Maximum Sum (Kadane's)
- **College/Drive:** Samsung Screening Round 2023
- **Problem Statement:** Standard Kadane's algorithm to compute maximum contiguous sum in an integer array with negative values.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 💡 Practical Samsung SWC Exam Preparation Strategy
1. **Never use `std::unordered_map` / `std::unordered_set` if time limits are tight:** Samsung SWC test cases intentionally construct hash collision anti-patterns. Use fixed-size boolean static lookup tables or sort + binary search.
2. **Master Manual Static Array Implementations:** Always know how to implement custom BFS queues (`int q[100000][2]`, `int head = 0, tail = 0;`) without depending on `<queue>`.
3. **Always Check Boundary Conditions:** Watch out for $0$-indexed vs $1$-indexed grids, unreachable destinations returning `-1`, and negative coordinates.
