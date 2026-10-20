# Google Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🔍

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Google Online Challenge (GOC)** / **HackerEarth** / Google Workspace Internal Code Portal
- **Test Duration:** 60 minutes (2 questions) or 90 minutes (select international/university tracks)
- **Format:** Pure algorithmic coding (No MCQs, No Aptitude)
- **Cutoff Benchmark:** Typically requires 100% test cases passed on at least 1 problem + majority/optimal test cases passed on the second. Google has stringent plagiarism detection (MOSS-like code similarity analysis).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Advanced Dynamic Programming:** Tree DP with rerooting, digit DP, bitmask DP, state compression.
- **Trees & Graphs:** Lowest Common Ancestor (LCA), binary lifting, multi-source BFS, Dijkstra on state machines.
- **Segment Trees & Fenwick Trees:** Range updates with point/range queries, coordinate compression.
- **Greedy & Binary Search on Answer:** Predicate monotonicity, sweep line algorithms.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Maximum Good Subarray / Segment Score (IIT Roorkee / IIT Delhi 2024)
- **College/Drive:** IITs Campus Drive Slot 1 (2024)
- **Problem Summary:** Given an array $A$ of $N$ integers and an integer $K$. You can choose any subarray and reverse at most one contiguous subsegment inside it. Find the maximum possible sum of the chosen subarray such that all adjacent differences are $\le K$.
- **Constraints:** $1 \le N \le 10^5$, $-10^9 \le A[i] \le 10^9$.
- **Approach:** Kadane's algorithm modification combined with prefix/suffix min-max arrays and two pointers.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 2. Path XOR Queries on Trees with Binary Lifting (BITS Pilani 2024)
- **College/Drive:** BITS Campus Drive (2024)
- **Problem Summary:** Given a tree with $N$ vertices, each node having a weight $W_i$. Answer $Q$ queries: Find the number of paths between node $U$ and node $V$ whose cumulative XOR sum equals $X$.
- **Constraints:** $N \le 10^5, Q \le 10^5, W_i \le 10^9$.
- **Approach:** Rooted tree prefix XORs from root $R$. XOR sum between $U$ and $V$ is $X_U \oplus X_V \oplus W_{\text{LCA}(U, V)}$. Binary lifting for $O(\log N)$ LCA queries.
- **Complexity:** $O((N + Q) \log N)$ Time, $O(N)$ Space.

#### 3. Minimum Cost Tree Rerooting (NIT Trichy / Surathkal 2024)
- **College/Drive:** NITs Day 1 Slot 2 (2024)
- **Problem Summary:** Given an undirected tree where moving from node $u$ to $v$ costs $C_{u, v}$. Each node has $P_i$ people. Find a meeting node that minimizes total transportation cost for all people.
- **Constraints:** $N \le 2 \times 10^5$.
- **Approach:** Tree DP with rerooting technique (2-pass DFS: bottom-up subtree sum + top-down parent contribution propagation).
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 4. Split Array with Monotonic Differences (Google Winter Intern 2025)
- **College/Drive:** Winter Intern Off-Campus (2025)
- **Problem Summary:** Partition an array of $N$ elements into $K$ contiguous subarrays such that the maximum of the sums of the subarrays is minimized, subject to an additional penalty condition based on element parity.
- **Approach:** Binary Search on answer combined with a greedy verification function.
- **Complexity:** $O(N \log(\text{Sum}))$.

#### 5. Maximum Beautiful Sequence under Arithmetic Constraints (IIIT Hyderabad 2024)
- **College/Drive:** IIIT-H Day 1 (2024)
- **Problem Summary:** Given an array $A$, find the longest subsequence where every pair of adjacent elements $(x, y)$ satisfies $|x - y| \le D$ and $x \times y > 0$.
- **Approach:** Segment Tree over values with coordinate compression to query range maximums $[x - D, x + D]$ in $O(\log N)$.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Range Module / Segment Tree with Lazy Propagation (Google SWE 2023)
- **College/Drive:** Google Online Challenge Slot 1 (2023)
- **Problem Summary:** A Range Module tracks ranges of numbers. Implement `addRange(left, right)`, `queryRange(left, right)`, and `removeRange(left, right)`.
- **LeetCode Equivalent:** [715. Range Module](https://leetcode.com/problems/range-module/)
- **Approach:** Dynamic Segment Tree with lazy propagation or `std::map<int, int>` tracking disjoint intervals.
- **Complexity:** $O(\log N)$ per query.

#### 7. Snapshot Array with History Lists (IIT Bombay 2023)
- **College/Drive:** IIT Bombay On-Campus (2023)
- **Problem Summary:** Implement `SnapshotArray(length)`, `set(index, val)`, `snap()`, and `get(index, snap_id)` in logarithmic time per query.
- **LeetCode Equivalent:** [1146. Snapshot Array](https://leetcode.com/problems/snapshot-array/)
- **Approach:** Maintain list of `(snap_id, value)` pairs per index; `get` uses binary search (`bisect_right`).
- **Complexity:** $O(1)$ set, $O(\log K)$ get.

#### 8. Race Car Minimum Instructions (Google GOC Slot 2 2023)
- **College/Drive:** GOC Off-Campus (2023)
- **Problem Summary:** Car starts at position 0 with speed +1. Commands: 'A' (accelerate) doubles speed, 'R' (reverse) resets speed to -1 or +1. Return length of shortest sequence of instructions to reach target position.
- **LeetCode Equivalent:** [818. Race Car](https://leetcode.com/problems/race-car/)
- **Approach:** Breadth-First Search (BFS) with state `(position, speed)` or Dynamic Programming on target.
- **Complexity:** $O(T \log T)$ Time where $T$ is target.

#### 9. Find All People With Secret (Graph BFS with Timestamps)
- **College/Drive:** Google Summer Intern Drive 2023
- **Problem Summary:** Return a list of all the people that have the secret after all the meetings have occurred. Meetings occur simultaneously at specific timestamps.
- **LeetCode Equivalent:** [2092. Find All People With Secret](https://leetcode.com/problems/find-all-people-with-secret/)
- **Approach:** Group meetings by timestamp. Within each timestamp, build an adjacency list and run BFS/DFS or Disjoint Set Union (DSU) with rollback for people not connected to secret holders.
- **Complexity:** $O(M \log M)$ Time where $M$ is total meetings.

#### 10. Longest Path With Different Adjacent Characters (Tree DFS)
- **College/Drive:** Google Campus Placement Slot 3 (2023)
- **Problem Summary:** You are given a tree rooted at node 0 consisting of $n$ nodes. Each node has a character. Return the length of the longest path in the tree such that no pair of adjacent nodes on the path have the same character.
- **LeetCode Equivalent:** [2246. Longest Path With Different Adjacent Characters](https://leetcode.com/problems/longest-path-with-different-adjacent-characters/)
- **Approach:** Post-order DFS returning the longest valid downward path from current node, while updating global maximum diameter from top two longest downward branches.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.
