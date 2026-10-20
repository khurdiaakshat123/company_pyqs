# Samsung R&D (SRIB / SRI-N) Online Assessment Guide & PYQs (2023 - 2025/2026) 📱

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Samsung SWC (Software Competency Platform)** / Custom HackerEarth
- **Test Duration:** 180 minutes (3 hours)
- **Format:** **1 Single Comprehensive Algorithmic Problem**
- **The "50 Test Cases" Rule:**
  - The assessment provides ~10 public test cases and runs ~40 hidden test cases (total ~50 test cases).
  - **Passing 50/50 test cases is MANDATORY.** Scoring 49/50 results in an automatic fail with zero partial credit.
- **Environment Restrictions:** In traditional Samsung SWC examinations, usage of standard template libraries (STL like `std::vector`, `std::map`, `std::queue`) can be restricted or heavily monitored; candidates are strongly advised to know manual implementations using static arrays.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

Samsung problems are classic competitive programming problems (Codeforces Div. 2 / 1400–1700 rating):

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Extremely High** | Backtracking & Recursion with Pruning | Hard | N-Queens variants, grid path generation, branch-and-bound pruning |
| **Very High** | Dynamic Programming with Bitmask | Hard | Traveling Salesperson Problem (TSP), state compression, burst balloons |
| **Very High** | Multi-Source BFS / Grid Traversals | Medium - Hard | Wormhole networks, explosion propagation, shortest path with obstacles |
| **High** | Simulation & State Search | Medium - Hard | Board games, pipe connections, laser/mirror reflections |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Wormhole / Space Teleporter (Samsung Classic)
- **Problem Summary:** You want to travel from source $(S_x, S_y)$ to destination $(D_x, D_y)$. The normal cost of walking between $(x_1, y_1)$ and $(x_2, y_2)$ is $|x_1 - x_2| + |y_1 - y_2|$ (Manhattan distance). There are $N$ bidirectional wormholes ($N \le 10$). Entering a wormhole from one end transports you to the other end with a specified fixed cost $W_i$. You can enter a wormhole at either end, and you can use any wormhole at most once. Find the minimum cost to reach destination.
- **Approach:** Backtracking / DFS exploring all $2^N \times N!$ permutations or Dijkstra on a graph of $(2N + 2)$ nodes.
- **Complexity:** $O((2N)!)$ with pruning or $O(V^2 \log V)$ with Dijkstra.

### 2. Burst Balloons / Missile Defense System
- **Problem Summary:** You are given $n$ targets, indexed from $0$ to $n - 1$. Each target has a score `nums[i]`. If you burst target $i$, you get `nums[i - 1] * nums[i] * nums[i + 1]` points. Find the maximum points you can collect.
- **LeetCode Equivalent:** [312. Burst Balloons](https://leetcode.com/problems/burst-balloons/)
- **Approach:** Interval Dynamic Programming: `dp[i][j] = max(dp[i][j], dp[i][k] + dp[k][j] + nums[i]*nums[k]*nums[j])` where $k$ is the LAST balloon burst in interval $(i, j)$.
- **Complexity:** $O(N^3)$ Time, $O(N^2)$ Space.

### 3. Fishermen and Gates Problem
- **Problem Summary:** There are $N$ spots along a river bank and 3 gates. Each gate has a specific coordinate and a number of fishermen waiting to enter. Each fisherman must occupy an empty spot, and the distance walked is $|spot - gate| + 1$. Find the minimum total distance walked by all fishermen.
- **Approach:** Permutations of gates ($3! = 6$ orders), backtracking placing fishermen into closest available adjacent spots.
- **Complexity:** $O(6 \times 2^3 \times N)$ with greedy tie-breaking.

### 4. Endoscope / Pipe Connection Simulation
- **Problem Summary:** An endoscope is inserted into a grid of connected pipes (7 types of pipes: horizontal, vertical, L-shaped, etc.). Given the entry coordinate and maximum cable length $L$, calculate the total number of pipe segments reachable.
- **Approach:** BFS tracking valid connection matching between adjacent pipe ports.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

---

## 💡 Cracking Samsung R&D OA
1. **Pass ALL Test Cases:** Do not leave edge cases unhandled ($N=1$, negative coordinates, zero distances). Samsung does not reward partial solutions.
2. **Prune Early in Recursion:** If the current running cost in backtracking exceeds the global minimum found so far (`if (current_cost >= min_cost) return;`), prune immediately.
