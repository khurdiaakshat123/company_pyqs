# Google Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🔍

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Google Online Challenge (GOC)** / **HackerEarth** / Google Workspace Internal Code Portal
- **Test Duration:** 60 minutes (2 questions) or 90 minutes (select international/university tracks)
- **Format:** Pure algorithmic coding (No MCQs, No Aptitude)
- **Cutoff Benchmark:** Typically requires 100% test cases passed on at least 1 problem + majority/optimal test cases passed on the second. Google has stringent plagiarism detection (MOSS-like code similarity analysis).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Advanced Dynamic Programming:** Tree DP with rerooting, digit DP, bitmask DP, state compression.
- **Trees & Graphs:** Lowest Common Ancestor (LCA), binary lifting, multi-source BFS, Dijkstra on state machines, DSU on values.
- **Segment Trees & Fenwick Trees:** Range updates with point/range queries, coordinate compression, 2D offline rectangle counting.
- **Greedy & Binary Search on Answer:** Predicate monotonicity, sweep line algorithms, binary search on answer space.
- **Strings & Combinatorics:** Subsequence counting modulo $10^9+7$, non-overlapping palindromic decompositions, rolling hashes.

---

## 📝 Verified Multi-Year OA Question Bank (Past 3 Years)
*Every problem listed below is a distinct, verified question sourced from 2023, 2024, and 2025/2026 campus placement drives (IITs, NITs, BITS, DTU) and off-campus Google Online Challenges. Duplicates across college slots have been strictly merged.*

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

#### 6. Palindromic Triples (Google OA 2024)
- **College/Drive:** Google India SWE OA (July 2024)
- **Problem Summary:** Given a lowercase string $S$ ($|S| \le 10^5$), find the number of ways to choose 3 distinct palindromic substrings $(i_1, j_1), (i_2, j_2), (i_3, j_3)$ such that they appear in strictly non-overlapping sequential order: $i_1 \le j_1 < i_2 \le j_2 < i_3 \le j_3 \le |S|$. Return the total count modulo $10^9+7$.
- **Approach:** 
  1. Manacher's Algorithm or Rolling Hash (Rabin-Karp) to compute palindromic substrings.
  2. Maintain `start_count[i]` (palindromes starting at $i$) and `end_count[i]` (palindromes ending at $i$).
  3. Prefix sum combinations to compute pairs and triples in linear time.
- **Complexity:** $O(N)$ Time with Manacher's, $O(N)$ Space.

#### 7. Distinct Decimal Values of Subsequences (Google India OA 2024)
- **College/Drive:** Google India Off-Campus 2024
- **Problem Summary:** Given a binary string of length $N$ ($N \le 2 \times 10^5$), find the number of distinct decimal values formed by taking all non-empty subsequences modulo $10^9 + 7$.
- **Approach:** Dynamic programming with last seen bit tracker. `dp[i]` represents distinct values formed ending at index $i$. Because binary numbers without leading zeroes uniquely represent integers, ignore subsequences with leading zeroes except for the single-character `"0"`.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 8. Server Coordinate & Rectangular Boundary Queries (Google OA 2024)
- **College/Drive:** Google University Placement 2024
- **Problem Summary:** You are given $N$ servers located at $(x_i, y_i)$ where each server can cover a rectangular region from $(0, 0)$ to $(x_i, y_i)$. You are given $Q$ client requests $(u_j, v_j)$. For each request, find the number of servers capable of servicing it ($x_i \ge u_j$ and $y_i \ge v_j$).
- **Constraints:** $N, Q \le 10^5$, coordinates up to $10^9$.
- **Approach:** Offline query processing: Sort servers and queries by x-coordinate descending. Insert y-coordinates into a Fenwick Tree (Binary Indexed Tree) with coordinate compression, then query suffix sum $\ge v_j$.
- **Complexity:** $O((N + Q) \log(N + Q))$ Time, $O(N + Q)$ Space.

#### 9. Subsequence Matching with at Most One Modification (Google OA 2024)
- **College/Drive:** Google SWE Intern Slot 2024
- **Problem Summary:** Given string $A$ and string $B$, check if $B$ appears as a subsequence in $A$ allowing at most 1 character in $B$ (excluding the first character) to be replaced by any other lowercase English letter. Return the smallest starting index of such a subsequence in $A$.
- **Approach:** Precompute next character occurrence table `next_pos[i][char]`. For each possible mismatch position $k \in [1, |B|-1]$, greedy jump using precomputed positions.
- **Complexity:** $O(|A| \times 26 + |B|)$ Time.

#### 10. Minimum Operations to Make Binary Representation Palindromic (Google 2024/2025)
- **College/Drive:** Google Summer Intern Drive (2024)
- **Problem Summary:** Given a positive integer $N$, find the minimum number of $+1$ or $-1$ operations required to convert $N$ into an integer whose standard binary representation (without leading zeroes) is a palindrome.
- **Approach:** Binary representation symmetry construction. For length $L = \lfloor \log_2 N \rfloor + 1$, mirror the first $\lceil L/2 \rceil$ bits to the lower half. Check the three candidate palindromes: same prefix, prefix $-1$, and prefix $+1$. Also check edge cases of length $L-1$ (all 1s) and $L+1$ (`10...01`).
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Range Module / Segment Tree with Lazy Propagation (Google SWE 2023)
- **College/Drive:** Google Online Challenge Slot 1 (2023)
- **Problem Summary:** A Range Module tracks ranges of numbers. Implement `addRange(left, right)`, `queryRange(left, right)`, and `removeRange(left, right)`.
- **LeetCode Equivalent:** [715. Range Module](https://leetcode.com/problems/range-module/)
- **Approach:** Dynamic Segment Tree with lazy propagation or `std::map<int, int>` tracking disjoint intervals.
- **Complexity:** $O(\log N)$ per query.

#### 12. Snapshot Array with History Lists (IIT Bombay 2023)
- **College/Drive:** IIT Bombay On-Campus (2023)
- **Problem Summary:** Implement `SnapshotArray(length)`, `set(index, val)`, `snap()`, and `get(index, snap_id)` in logarithmic time per query.
- **LeetCode Equivalent:** [1146. Snapshot Array](https://leetcode.com/problems/snapshot-array/)
- **Approach:** Maintain list of `(snap_id, value)` pairs per index; `get` uses binary search (`bisect_right`).
- **Complexity:** $O(1)$ set, $O(\log K)$ get.

#### 13. Race Car Minimum Instructions (Google GOC Slot 2 2023)
- **College/Drive:** GOC Off-Campus (2023)
- **Problem Summary:** Car starts at position 0 with speed +1. Commands: 'A' (accelerate) doubles speed, 'R' (reverse) resets speed to -1 or +1. Return length of shortest sequence of instructions to reach target position.
- **LeetCode Equivalent:** [818. Race Car](https://leetcode.com/problems/race-car/)
- **Approach:** Breadth-First Search (BFS) with state `(position, speed)` or Dynamic Programming on target.
- **Complexity:** $O(T \log T)$ Time where $T$ is target.

#### 14. Find All People With Secret (Graph BFS with Timestamps)
- **College/Drive:** Google Summer Intern Drive 2023
- **Problem Summary:** Return a list of all the people that have the secret after all the meetings have occurred. Meetings occur simultaneously at specific timestamps.
- **LeetCode Equivalent:** [2092. Find All People With Secret](https://leetcode.com/problems/find-all-people-with-secret/)
- **Approach:** Group meetings by timestamp. Within each timestamp, build an adjacency list and run BFS/DFS or Disjoint Set Union (DSU) with rollback for people not connected to secret holders.
- **Complexity:** $O(M \log M)$ Time where $M$ is total meetings.

#### 15. Longest Path With Different Adjacent Characters (Tree DFS)
- **College/Drive:** Google Campus Placement Slot 3 (2023)
- **Problem Summary:** You are given a tree rooted at node 0 consisting of $n$ nodes. Each node has a character. Return the length of the longest path in the tree such that no pair of adjacent nodes on the path have the same character.
- **LeetCode Equivalent:** [2246. Longest Path With Different Adjacent Characters](https://leetcode.com/problems/longest-path-with-different-adjacent-characters/)
- **Approach:** Post-order DFS returning the longest valid downward path from current node, while updating global maximum diameter from top two longest downward branches.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 16. Special Subsequence Maximizing Global Frequency Sum (Google SWE Intern 2023)
- **College/Drive:** Google SWE Intern OA (2023)
- **Problem Summary:** Given a string $S$ and integer $K$. A special subsequence has length exactly $K$ and contains all unique characters. Find the total number of distinct special subsequences that maximize the sum of global frequencies of their constituent characters modulo $10^9+7$.
- **Approach:** 
  1. Count global frequencies of all unique characters.
  2. Sort unique characters by frequency descending.
  3. Greedily pick characters with the highest frequencies. If there's a tie at the $K$-th boundary among $M$ characters where $R$ need to be chosen, the number of distinct choices is $\binom{M}{R} \pmod{10^9+7}$.
- **Complexity:** $O(|S| + 26 \log 26) = O(|S|)$ Time, $O(1)$ Space.

#### 17. Athletic Team Dual Event Selection (Google OA 2023)
- **College/Drive:** Google Campus Slot 2023
- **Problem Summary:** You have $N$ athletes. Athlete $i$ takes $A[i]$ seconds to run and $B[i]$ seconds to swim. You must select exactly $X$ runners and $Y$ swimmers such that no athlete participates in both events ($X + Y \le N$). Minimize the total time taken by all $X + Y$ athletes.
- **Approach:** 
  - Difference sort: Sort athletes by $A[i] - B[i]$.
  - The first $X$ athletes in the sorted order are optimal candidates for running, while the rest are optimal candidates for swimming. Prefix/suffix priority queues (Heaps) can handle arbitrary $X, Y$.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 18. Number of Good Paths on Tree (DSU on Values)
- **College/Drive:** Google Placement Season 2023
- **Problem Summary:** There is an undirected tree with $N$ nodes. Each node has a value `vals[i]`. A path is "good" if the starting and ending nodes have the same value, and all intermediate nodes have values $\le$ the starting node's value. Return the number of good paths.
- **LeetCode Equivalent:** [2421. Number of Good Paths](https://leetcode.com/problems/number-of-good-paths/)
- **Approach:** Sort nodes by value. Group edges by $\max(vals[u], vals[v])$. Process edge groups in ascending order using Disjoint Set Union (DSU). For each connected component, count nodes with the current maximum value and add $\binom{\text{count}}{2}$ to the answer.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 19. Maximum Path Quality of a Graph (Backtracking + Graph State)
- **College/Drive:** Google On-Campus Slot 2023
- **Problem Summary:** There is an undirected graph with values on nodes. You start at node 0 and must return to node 0 within `maxTime` total edge travel time. You can visit nodes and edges multiple times, but each node's value is added to total score at most once. Maximize total score.
- **LeetCode Equivalent:** [2065. Maximum Path Quality of a Graph](https://leetcode.com/problems/maximum-path-quality-of-a-graph/)
- **Approach:** Backtracking DFS with pruning. Since maximum node degree $\le 4$ and `maxTime` $\le 100$ with edge time $\ge 10$, total paths are bounded ($\le 4^{10} \approx 10^6$).
- **Complexity:** $O(4^{\text{maxTime}/10})$ Time.

#### 20. Count Subarrays With Fixed Bounds (Sliding Window Extremas)
- **College/Drive:** Google SWE Drive 2023
- **Problem Summary:** You are given an integer array `nums` and two integers `minK` and `maxK`. Return the number of continuous subarrays that contain `minK` as their minimum element and `maxK` as their maximum element.
- **LeetCode Equivalent:** [2444. Count Subarrays With Fixed Bounds](https://leetcode.com/problems/count-subarrays-with-fixed-bounds/)
- **Approach:** Three pointers / indices tracking: `last_min_k_pos`, `last_max_k_pos`, and `last_invalid_pos`. For each index $i$, valid starting positions count is $\max(0, \min(last\_min, last\_max) - last\_invalid)$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.
