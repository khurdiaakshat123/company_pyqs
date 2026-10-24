# Jane Street Online Assessment & Interview Guide (2023 - 2025/2026) 🎲

## 📌 Assessment Overview & Test Logistics
- **Assessment Style:** Custom Quantitative Assessment / Mental Math Fast-Paced Test / Take-Home Systems Challenge
- **Components:**
  1. **Mental Math Speed Test (First Round Screen):** 80 arithmetic/fraction/percentage questions in 8 minutes or 40 questions in 5 minutes. Penalties apply for incorrect guesses (Negative marking).
  2. **Quantitative & Probability Assessment:** 3 to 5 multi-step questions covering probability, expected value, Markov chains, and game theory.
  3. **Software Take-Home / HackerRank Coding:** Writing high-throughput simulators, custom memory allocators, or state-machine graph parsers.
- **Core Philosophy:** Jane Street rejects memorized LeetCode templates. They evaluate:
  - **Mathematical Rigor & Mental Math:** Rapid estimation and error-free mental calculation under pressure.
  - **Probability & Expected Value:** Combinatorics, Bayes' theorem, conditional expectation, martingales, optimal stopping.
  - **Systems Mindset & Immutability:** Clean recursive patterns, zero memory leaks, thread-safety, edge-case vigilance.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Probability & Combinatorics:** Expected number of steps to reach target, betting games, random walks on lattices and graphs.
- **Optimal Stopping Theory:** The secretary problem variants, dice rolling stopping time, coin flip stopping rules.
- **Game Theory & Minimax:** Nim game variants, payoff matrices, asymmetric information betting games.
- **Simulation & Systems Design:** Order book matching engines, discrete event simulation, memory allocators, lock-free queues, functional state machines.
- **Continuous & Streaming Algorithms:** Online median calculation, reservoir sampling, prefix routing.

---

## 📝 Multi-Year OA & Technical Screening Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. The Coin Flip Game (Expected Value / Martingale)
- **Drive/Role:** Quant Trading / SWE Campus Intern & New Grad 2024–2025
- **Problem Summary:** You flip a fair coin repeatedly. You can choose to stop playing at any time and receive $\$1$ for every Head and pay $\$1$ for every Tail. If you play optimally with a maximum limit of $N$ flips, what is your expected payout?
- **Constraints:** $N \le 1000$.
- **Approach:** Dynamic Programming working backwards from the $N$-th flip (backward induction):
  $$E[t] = \max\left(H - T, \frac{1}{2} E[t+1 \mid \text{Head}] + \frac{1}{2} E[t+1 \mid \text{Tail}]\right)$$
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

#### 2. Random Walk on a Regular Octahedron / Cube
- **Drive/Role:** Quant Research Screening 2024–2025
- **Problem Summary:** A particle starts at vertex 0 of a cube (8 vertices). At each step, it transitions to an adjacent vertex with probability $\frac{1}{3}$. Find the expected number of steps until it reaches the diagonally opposite vertex.
- **Constraints:** Exact analytical closed form or linear system solution.
- **Approach:** Set up a system of linear equations grouping vertices by distance from the target (distance 3, 2, 1, 0):
  - $E_3 = 1 + E_2$
  - $E_2 = 1 + \frac{2}{3} E_3 + \frac{1}{3} E_1$
  - $E_1 = 1 + \frac{1}{3} E_2 + \frac{2}{3} E_0$ where $E_0 = 0$.
  - Solve the 3 equations to get $E_3 = 10$.
- **Complexity:** $O(1)$ analytical derivation.

#### 3. High-Throughput Limit Order Book (LOB) Simulation
- **Drive/Role:** SWE Systems New Grad 2024–2025
- **Problem Summary:** Implement an in-memory limit order book that supports `addOrder(id, side, price, qty)`, `cancelOrder(id)`, and returns market depth with price-time priority matching.
- **Constraints:** Up to $10^6$ operations; latency per operation $< 5\ \mu\text{s}$.
- **Approach:** Map of price levels to doubly linked list of orders (`std::map<double, std::list<Order>>`), plus a Hash Map of `order_id` to iterator for $O(1)$ cancellations.
- **Complexity:** $O(\log P)$ for price level discovery, $O(1)$ for cancel and execution.

#### 4. 100-Sided Die Stopping Game
- **Drive/Role:** Quantitative Trading Phone Screen 2024–2025
- **Problem Summary:** You roll a fair 100-sided die. After each roll, you can take the dollar amount on the die and stop, or pay $\$1$ to re-roll. What is the optimal threshold strategy and expected payoff?
- **Constraints:** Number of sides $S = 100$, cost $c = 1$.
- **Approach:** If current expected value is $E$, optimal strategy is to stop if roll $X \ge \lceil E \rceil$.
  $$E = -1 + \sum_{x=1}^{100} \frac{\max(x, E)}{100}$$
  Solve iteratively to find threshold $k \approx 87$ and $E \approx 87.35$.
- **Complexity:** $O(S)$ numerical convergence.

#### 5. Grid Path with Parity-Toggling Obstacles
- **Drive/Role:** SWE Take-Home Assessment 2024–2025
- **Problem Summary:** A robot traverses an $M \times N$ grid where stepping onto a cell toggles the open/closed states of adjacent cells. Detect if an infinite state cycle exists and compute the cycle period.
- **Constraints:** $M \times N \le 20$.
- **Approach:** State representation as `(robot_x, robot_y, bitmask_grid_state)`. Floyd's Cycle-Finding Algorithm (Tortoise and Hare) or Hash Map of visited state indices.
- **Complexity:** $O(M \cdot N \cdot 2^{M \cdot N})$ worst case state space.

#### 6. Lock-Free SPSC Ring Buffer
- **Drive/Role:** High-Performance Systems Engineer 2024
- **Problem Summary:** Implement a cache-aligned, single-producer single-consumer circular queue in C++ without mutex locks or spinlocks.
- **Constraints:** Zero data loss, thread-safe memory ordering (`std::memory_order_acquire` / `std::memory_order_release`).
- **Approach:** Head and tail atomic size_t markers with cache line padding (`alignas(64)`) to eliminate false sharing.
- **Complexity:** $O(1)$ push/pop operations with zero lock contention.

#### 7. Polya's Urn with Color Reinforcement
- **Drive/Role:** Quant Research Drive 2024
- **Problem Summary:** An urn initially contains $w$ white balls and $b$ black balls. A ball is drawn at random; its color is observed, and it is returned along with $c$ additional balls of the same color. Prove that the fraction of white balls is a Martingale and compute the limiting distribution.
- **Approach:** Show that $E[X_{n+1} \mid X_n] = X_n$. Apply Doob's Martingale Convergence Theorem to establish that the limiting proportion follows a Beta distribution $\text{Beta}(w/c, b/c)$.
- **Complexity:** Theoretical proof & Martingale invariant.

#### 8. VWAP Order Slicing Algorithm
- **Drive/Role:** Algorithmic Trading Software 2024
- **Problem Summary:** Given historical intra-day volume curves across $T$ minute bins and an execution order of size $Q$, partition the order into discrete execution slices minimizing market impact and tracking error.
- **Constraints:** $T = 390$ (market minutes), $Q \le 10^7$.
- **Approach:** Dynamic programming / convex quadratic programming minimizing tracking error:
  $$\min \sum_{t=1}^T \left(q_t - Q \cdot \frac{V_t}{V_{\text{total}}}\right)^2 \quad \text{s.t.} \quad \sum q_t = Q, \ q_t \ge 0$$
- **Complexity:** $O(T \log T)$ with greedy water-filling.

#### 9. Asymmetric Information Coin Bet
- **Drive/Role:** Trading Intern Screen 2024
- **Problem Summary:** Two players bet on coin flips where one player knows the coin bias $p \in \{0.4, 0.6\}$ with equal prior. Find the Nash Equilibrium betting strategy.
- **Approach:** Game theoretic zero-sum analysis; derive Bayesian Nash equilibrium mixed strategies to determine when to bluff or fold.
- **Complexity:** $O(1)$ analytical derivation.

#### 10. Segregated Free-List Memory Allocator
- **Drive/Role:** Systems Engineering Assessment 2024
- **Problem Summary:** Implement custom `malloc` and `free` operations managing a contiguous memory buffer with minimal fragmentation.
- **Constraints:** Total buffer size up to 1GB, operations up to $10^5$.
- **Approach:** Power-of-two buddy system or segregated free lists with immediate header/footer coalescing (Knuth boundary-tag method).
- **Complexity:** $O(1)$ amortized allocation/free.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Russian Roulette with Consecutive Bullets
- **Drive/Role:** Quant Interview 2023–2024
- **Problem Summary:** A 6-cylinder revolver has 2 bullets placed in adjacent chambers. Player 1 pulls trigger (clicks on empty). Should Player 2 spin or pull trigger immediately?
- **Approach:** Conditional probability: 4 empty chambers. Since the first pull was empty, only 1 of the 4 empty chambers has a bullet immediately following it. Pulling trigger immediately has $\frac{1}{4} = 25\%$ chance of bullet, whereas spinning has $\frac{2}{6} = 33.33\%$. Strategy: Pull trigger immediately!
- **Complexity:** $O(1)$ analytical derivation.

#### 12. Nim Game with Custom Subtraction Sets
- **Drive/Role:** Algorithm Screen 2023–2024
- **Problem Summary:** Two players take turns removing $S \in \{1, 3, 4\}$ stones from a pile of $N$ stones. Determine winning player under optimal play.
- **Constraints:** $N \le 10^9$.
- **LeetCode Equivalent:** [292. Nim Game variant](https://leetcode.com/problems/nim-game/)
- **Approach:** Compute Grundy values (mex function) for small $N$; identify repeating period (period length 7 for $\{1, 3, 4\}$). Output outcome in $O(1)$ via modulo indexing.
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

#### 13. Card Draw Without Replacement Expected Value
- **Drive/Role:** Campus Quant Slot 2023
- **Problem Summary:** Standard 52-card deck. Red cards earn $+\$1$, Black cards lose $-\$1$. You can stop drawing at any time. What is the optimal stopping policy?
- **Constraints:** Total cards $N = 52$ ($R=26, B=26$).
- **Approach:** Backward induction dynamic programming on remaining `(red, black)` cards:
  $$V(r, b) = \max\left(0, \frac{r}{r+b}(1 + V(r-1, b)) + \frac{b}{r+b}(-1 + V(r, b-1))\right)$$
- **Complexity:** $O(R \cdot B)$ states ($26 \times 26 = 676$ states), $O(1)$ per state.

#### 14. Convex Hull Trick for Upper Envelope Queries
- **Drive/Role:** Advanced SWE Screening 2023
- **Problem Summary:** Maintain a set of linear profit lines $y = m x + c$ subject to dynamically added slopes and evaluate the maximum profit at arbitrary coordinate $x$.
- **Constraints:** $N \le 10^5$ line insertions and queries.
- **Approach:** Dynamic Li Chao Tree or monotonic deque convex hull trick (slopes added in sorted order).
- **Complexity:** $O(N \log N)$ or $O(N)$ with sorted slopes.

#### 15. Gambler's Ruin with Drift on 1D Lattice
- **Drive/Role:** Quant Research Assessment 2023
- **Problem Summary:** A gambler starts with $\$k$ and bets $\$1$ repeatedly with probability $p$ of winning and $q = 1-p$ of losing, stopping upon reaching $\$0$ or $\$M$. Derive exact ruin probability and expected duration.
- **Approach:** Second-order linear difference equation:
  $$P(k) = p P(k+1) + q P(k-1), \quad P(0)=1, P(M)=0$$
  Solve characteristic polynomial to yield $P(k) = \frac{(q/p)^M - (q/p)^k}{(q/p)^M - 1}$ for $p \neq 0.5$.
- **Complexity:** $O(1)$ closed form.

#### 16. Fast Fourier Transform Polynomial Multiplication
- **Drive/Role:** Quant Developer 2023
- **Problem Summary:** Given two polynomials of degree up to $10^5$, compute their convolution in $O(N \log N)$ time.
- **Constraints:** Degree $N \le 10^5$, coefficients within modulo $998244353$.
- **Approach:** Number Theoretic Transform (NTT) using primitive roots modulo 998244353 with bit-reversal permutation.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 17. High-Speed Ticker Router with Trie
- **Drive/Role:** Systems Developer 2023
- **Problem Summary:** Route millions of incoming ticker symbols to specific strategy listener callbacks using longest prefix matching.
- **Constraints:** Alphabet `[A-Z]`, max symbol length 12, throughput $> 10^7$ lookups/sec.
- **Approach:** Compact Array-based Trie or Radix Tree where child pointers are direct array indices avoiding pointer chasing overhead.
- **Complexity:** $O(L)$ Time where $L$ is symbol length.

#### 18. Poisson Process Arrival Times Simulation
- **Drive/Role:** Quant Trading Research 2023
- **Problem Summary:** Generate exact inter-arrival event times for market order fills modeled as a homogeneous Poisson process with rate $\lambda$.
- **Approach:** Inverse transform sampling using exponential random variables: $\Delta t = -\frac{\ln(U)}{\lambda}$ where $U \sim \text{Uniform}(0, 1)$.
- **Complexity:** $O(1)$ per generated event.

#### 19. Currency Arbitrage Cycle Detection
- **Drive/Role:** SWE Algorithmic Screening 2023
- **Problem Summary:** Given currency exchange rates matrix $R$, find if an arbitrage cycle exists that yields risk-free profit.
- **Constraints:** $N \le 100$ currencies.
- **Approach:** Transform edge weights to negative logarithms: $w(u, v) = -\ln(R[u][v])$. Run Bellman-Ford algorithm to detect negative weight cycles.
- **Complexity:** $O(V \cdot E)$ Time, $O(V)$ Space.

#### 20. Online Continuous Streaming Median
- **Drive/Role:** Systems SWE Drive 2023
- **Problem Summary:** Maintain the exact median of a continuous stream of tick prices with minimal latency.
- **Constraints:** Stream length $N \le 10^7$.
- **LeetCode Equivalent:** [295. Find Median from Data Stream](https://leetcode.com/problems/find-median-from-data-stream/)
- **Approach:** Dual-heap balance (Max-Heap for lower half, Min-Heap for upper half) maintaining size difference $\le 1$.
- **Complexity:** $O(\log N)$ insertion, $O(1)$ median query.

---

## 💡 Cracking Jane Street Quantitative & Systems Screens
1. **Explain the Intuition First:** State why the math works before doing algebra. Talk through boundary conditions ($N=0, 1, \infty$).
2. **Be Rigorous with Betting / Risk:** Never gamble on negative EV scenarios; always price the risk correctly.
3. **Write Predictable, Zero-Allocation Code:** In systems problems, prefer cache-friendly flat arrays, stack allocation, and minimal locking over complex pointer webs.
