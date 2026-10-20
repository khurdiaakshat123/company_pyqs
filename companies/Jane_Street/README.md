# Jane Street Online Assessment & Interview Guide (2023 - 2025/2026) 🎲

## 📌 Assessment Overview & Test Logistics
- **Assessment Style:** Custom Quantitative Assessment / CodeSignal Take-Home Challenge
- **Core Philosophy:** Jane Street rejects standard memorized LeetCode templates. Their testing evaluates:
  - **Mathematical Reasoning & Mental Math:** High-speed calculation under pressure.
  - **Probability & Expected Value:** Combinatorics, Bayes' theorem, conditional probability, martingales, game-theoretic betting.
  - **Functional & Systems Mindset:** Clean recursive patterns, immutability, state transitions, edge-case rigor (their production stack is OCaml, but C++/Python are accepted in assessments).

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Extremely High** | Probability & Combinatorics | Hard | Expected number of steps to reach target, betting games, random walks |
| **Very High** | Game Theory & Optimal Strategies | Hard | Nim game variants, minimax, zero-sum games, bluffing and payoff matrices |
| **High** | Simulation & State Management | Hard | Complex state machine tracking, packet ordering, discrete event simulation |
| **High** | Recursion & Functional Data Flow | Hard | Backtracking, immutable data structures, lazy sequences |

---

## 📝 Recent Real Questions & Puzzles Asked (2023, 2024, 2025)

### 1. The Coin Flip Game (Expected Value / Martingale)
- **Problem Summary:** You flip a fair coin repeatedly. You can choose to stop playing at any time and receive $\$1$ for every Head and pay $\$1$ for every Tail. If you play optimally with a maximum limit of $N$ flips, what is your expected payout?
- **Approach:** Dynamic Programming working backwards from the $N$-th flip (backward induction):
  $$E[t] = \max\left(H - T, \frac{1}{2} E[t+1 \mid \text{Head}] + \frac{1}{2} E[t+1 \mid \text{Tail}]\right)$$
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

### 2. Random Walk on a Regular Graph
- **Problem Summary:** A particle starts at vertex 0 on a cube (8 vertices) or regular octahedron. At each step, it chooses an adjacent vertex with equal probability. What is the expected number of steps until it reaches the diagonally opposite vertex?
- **Approach:** System of linear equations set up on symmetric vertex classes based on distance from target. Solve using Gaussian elimination or Markov absorption states.

### 3. Grid Path with Conditional Obstacles (Simulation)
- **Problem Summary:** Simulate a robot moving on a grid where visiting a cell toggles state transitions on adjacent cells according to predefined parity rules. Find if a periodic cycle exists and compute the cycle period.
- **Approach:** Floyd's Cycle Detection (Tortoise and Hare) or Hash Set state hashing on bitmask configuration.
- **Complexity:** $O(2^K)$ bounded states.

### 4. Memory Allocator with Strict Boundaries
- **Problem Summary:** Implement a custom memory chunk allocator that minimizes external fragmentation under random allocation and deallocation operations.
- **Approach:** Segregated free lists with boundary tag coalescing (Buddy allocation system).

---

## 💡 Cracking Jane Street Technical Tests
1. **Never guess numbers:** If an interviewer asks an expected value question, always derive the equation algebraically before plugging in numbers.
2. **Be upfront about assumptions:** When problem constraints are ambiguous, explicitly state edge cases ($N=0$, degenerate probabilities, infinity bounds) before coding.
