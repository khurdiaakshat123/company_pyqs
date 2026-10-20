# Google Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🔍

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** Google Online Challenge (GOC) / HackerEarth / Google Workspace Internal Code Portal
- **Test Duration:** 60 minutes (2 questions) or 90 minutes (2 questions in some university campus hiring drives)
- **Format:** Pure algorithmic coding (No MCQs, No Aptitude)
- **Cutoff Benchmark:** Typically requires 100% test cases passed on at least 1 problem + majority/optimal test cases passed on the second. Google has stringent plagiarism detection (MOSS-like code similarity analysis).

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

Google's OA is known for unique, non-standard problem formulations that are rarely verbatim LeetCode clones. They test pure problem reduction and mathematical observation:

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Dynamic Programming | Medium - Hard | State transitions with bitmasking, Digit DP, Tree DP, Subsequence optimization |
| **Very High** | Trees & Graphs | Hard | Tree rerooting, Lowest Common Ancestor (LCA), Topological Sort, Multi-source BFS, Dijkstra |
| **High** | Segment Trees & BIT | Hard | Range minimum/sum queries with point/range updates, Coordinate compression |
| **High** | Greedy & Binary Search | Medium - Hard | Binary Search on Answer Space (Monotonic Predicates), Sweepline |
| **Medium** | Disjoint Set Union (DSU) | Medium | Component merging, Kruskal's MST variations, cycle detection |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Maximum Good Subarray / Segment Score (2024 Campus Drive)
- **Problem Summary:** Given an array $A$ of $N$ integers and an integer $K$. You can choose any subarray and reverse at most one contiguous subsegment inside it. Find the maximum possible sum of the chosen subarray such that all adjacent differences are $\le K$.
- **Constraints:** $1 \le N \le 10^5$, $-10^9 \le A[i] \le 10^9$.
- **Approach:** Kadane's algorithm modification combined with prefix/suffix min-max arrays and two pointers.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 2. Path XOR Queries on Trees (2024 Off-Campus)
- **Problem Summary:** Given a tree with $N$ vertices, each node having a weight $W_i$. Answer $Q$ queries: Find the number of paths between node $U$ and node $V$ whose cumulative XOR sum equals $X$.
- **Constraints:** $N \le 10^5, Q \le 10^5, W_i \le 10^9$.
- **Approach:** Rooted tree prefix XORs from root $R$. XOR sum between $U$ and $V$ is $X_U \oplus X_V \oplus W_{\text{LCA}(U, V)}$. Heavy-light decomposition or binary lifting for LCA.
- **Complexity:** $O((N + Q) \log N)$ Time, $O(N)$ Space.

### 3. Minimum Cost Tree Rerooting (2023 - 2024 Hiring Drive)
- **Problem Summary:** Given an undirected tree where moving from node $u$ to $v$ costs $C_{u, v}$. Each node has $P_i$ people. Find a meeting node that minimizes total transportation cost for all people.
- **Constraints:** $N \le 2 \times 10^5$.
- **Approach:** Tree DP with rerooting technique (2-pass DFS: bottom-up subtree sum + top-down parent contribution propagation).
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 4. Split Array with Monotonic Differences (2025 Winter Intern)
- **Problem Summary:** Partition an array of $N$ elements into $K$ contiguous subarrays such that the maximum of the sums of the subarrays is minimized, subject to an additional penalty condition based on element parity.
- **Approach:** Binary Search on answer combined with a greedy verification function.
- **Complexity:** $O(N \log(\text{Sum}))$.

---

## 💡 Cracking Google OA: Proven Tips
1. **Never copy-paste code:** Google automatically disqualifies candidates whose code shows high lexical and syntactic similarity with online solutions.
2. **Watch for Integer Overflow:** Always use `long long` in C++ / `BigInt` or 64-bit integers; constraints frequently reach $10^9 \times 10^5 = 10^{14}$.
3. **Handle Edge Cases Early:** $N=1, K=0$, all negative numbers, duplicate values, linear graphs (skewed trees), and disconnected components.
