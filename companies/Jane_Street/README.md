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
- **Simulation & Systems Design:** Order book matching engines, discrete event simulation, memory allocators, functional state machines.

---

## 📝 Multi-Year OA & Technical Screening Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. The Coin Flip Game (Expected Value / Martingale)
- **Drive/Role:** Quant Trading / SWE Campus Intern & New Grad 2024
- **Problem Summary:** You flip a fair coin repeatedly. You can choose to stop playing at any time and receive $\$1$ for every Head and pay $\$1$ for every Tail. If you play optimally with a maximum limit of $N$ flips, what is your expected payout?
- **Approach:** Dynamic Programming working backwards from the $N$-th flip (backward induction):
  $$E[t] = \max\left(H - T, \frac{1}{2} E[t+1 \mid \text{Head}] + \frac{1}{2} E[t+1 \mid \text{Tail}]\right)$$
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

#### 2. Random Walk on a Regular Octahedron / Cube
- **Drive/Role:** Quant Research Screening 2024
- **Problem Summary:** A particle starts at vertex 0 of a cube (8 vertices). At each step, it transitions to an adjacent vertex with probability $\frac{1}{3}$. Find the expected number of steps until it reaches the diagonally opposite vertex.
- **Approach:** Set up a system of linear equations grouping vertices by distance from the target (distance 3, 2, 1, 0).
  - $E_3 = 1 + E_2$
  - $E_2 = 1 + \frac{2}{3} E_3 + \frac{1}{3} E_1$
  - $E_1 = 1 + \frac{1}{3} E_2 + \frac{2}{3} E_0$ where $E_0 = 0$.
  - Solve the 3 equations to get $E_3 = 10$.
- **Complexity:** $O(1)$ analytical derivation.

#### 3. High-Throughput Limit Order Book (LOB) Simulation
- **Drive/Role:** SWE Systems New Grad 2024
- **Problem Summary:** Implement an in-memory limit order book that supports `addOrder(id, side, price, qty)`, `cancelOrder(id)`, and returns market depth with price-time priority matching.
- **Approach:** Map of price levels to doubly linked list of orders (`std::map<double, std::list<Order>>`), plus a Hash Map of `order_id` to iterator for $O(1)$ cancellations.
- **Complexity:** $O(\log P)$ for price insertion, $O(1)$ for cancel and execution.

#### 4. 100-Sided Die Stopping Game
- **Drive/Role:** Quantitative Trading Phone Screen 2024
- **Problem Summary:** You roll a fair 100-sided die. After each roll, you can take the dollar amount on the die and stop, or pay $\$1$ to re-roll. What is the optimal threshold strategy and expected payoff?
- **Approach:** If current expected value is $E$, optimal strategy is to stop if roll $X \ge \lceil E \rceil$.
  $$E = -1 + \sum_{x=1}^{100} \frac{\max(x, E)}{100}$$
  Solve iteratively or numerically to find threshold $k \approx 87$ and $E \approx 87.35$.

#### 5. Grid Path with Parity-Toggling Obstacles
- **Drive/Role:** SWE Take-Home Assessment 2024
- **Problem Summary:** A robot traverses an $M \times N$ grid where stepping onto a cell toggles the open/closed states of adjacent cells. Detect if an infinite state cycle exists and compute the cycle period.
- **Approach:** State representation as `(robot_x, robot_y, bitmask_grid_state)`. Floyd's Cycle-Finding Algorithm (Tortoise and Hare) or Hash Map of visited states.
- **Complexity:** $O(M \cdot N \cdot 2^{M \cdot N})$ worst case state space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Asymmetric Information Coin Bet
- **Drive/Role:** Trading Intern Screen 2023
- **Problem Summary:** Two players bet on coin flips where one player knows the coin bias $p \in \{0.4, 0.6\}$ with equal prior. Find the Nash Equilibrium betting strategy.
- **Approach:** Game theoretic zero-sum analysis; derive Bayesian Nash equilibrium mixed strategies.

#### 7. Segregated Free-List Memory Allocator
- **Drive/Role:** Systems Engineering Assessment 2023
- **Problem Summary:** Implement custom `malloc` and `free` operations managing a contiguous memory buffer with minimal fragmentation.
- **Approach:** Power-of-two buddy system or segregated free lists with immediate header/footer coalescing.
- **Complexity:** $O(1)$ amortized allocation/free.

#### 8. Russian Roulette with Consecutive Bullets
- **Drive/Role:** Quant Interview 2023
- **Problem Summary:** A 6-cylinder revolver has 2 bullets placed in adjacent chambers. Player 1 pulls trigger (clicks on empty). Should Player 2 spin or pull trigger immediately?
- **Approach:** Conditional probability: 4 empty chambers. Since the first pull was empty, only 1 of the 4 empty chambers has a bullet immediately following it. Pulling trigger immediately has $\frac{1}{4} = 25\%$ chance of bullet, whereas spinning has $\frac{2}{6} = 33.33\%$. Strategy: Pull trigger immediately!

#### 9. Nim Game with Custom Subtraction Sets
- **Drive/Role:** Algorithm Screen 2023
- **Problem Summary:** Two players take turns removing $S \in \{1, 3, 4\}$ stones from a pile of $N$ stones. Determine winning player.
- **LeetCode Equivalent:** [292. Nim Game variant](https://leetcode.com/problems/nim-game/) / Sprague-Grundy Theorem
- **Approach:** Compute Grundy values (mex function) or boolean DP states modulo pattern.
- **Complexity:** $O(N)$ or $O(1)$ with period detection.

#### 10. Card Draw Without Replacement Expected Value
- **Drive/Role:** Campus Quant Slot 2023
- **Problem Summary:** Standard 52-card deck. Red cards earn $+\$1$, Black cards lose $-\$1$. You can stop drawing at any time. What is the optimal stopping policy?
- **Approach:** Backward induction dynamic programming on remaining `(red, black)` cards:
  $$V(r, b) = \max\left(0, \frac{r}{r+b}(1 + V(r-1, b)) + \frac{b}{r+b}(-1 + V(r, b-1))\right)$$
- **Complexity:** $O(R \cdot B)$ states where $R=26, B=26$ ($26 \times 26 = 676$ states).

---

## 💡 Cracking Jane Street Quantitative & Systems Screens
1. **Mental Math Speed Drills:** Practice arithmetic with fractions, two-digit multiplications ($73 \times 89$), and volatility percentages without scratch paper.
2. **Backward Induction:** In sequential decision games with a finite horizon, always work backward from the terminal state $t = N$.
3. **State Invariants:** In systems programming tasks, write down explicit assertions verifying order invariants (e.g. `order_quantity > 0`, `bid < ask` cross conditions).
