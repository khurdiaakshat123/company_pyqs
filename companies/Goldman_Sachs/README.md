# Goldman Sachs Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 135 minutes total (timed section by section)
- **Sections Breakdown:**
  1. **Section 1: Coding (DSA)** – 2 Questions (60 minutes).
  2. **Section 2: Quantitative Aptitude & Mathematics** – 8 to 10 Questions (20 minutes). High weightage on Probability & Combinatorics.
  3. **Section 3: Computer Science Fundamentals** – 7 to 10 MCQs (20 minutes). OS, DBMS, Algorithms.
  4. **Section 4: Subjective / Behavioral Writing** – 2 short essay questions on financial ethics or problem handling (15 minutes).
- **Negative Marking:** Present in MCQ sections (+5 for correct, -2 for incorrect, or +1, -0.25). Guesswork is strictly discouraged.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Probability & Combinatorics | Medium - Hard | Bayes' Theorem, expected value, card/dice distributions, conditional probability |
| **Very High** | Array & String Manipulation | Medium | Run-length encoding, cyclic shifts, subarray balance, 2-pointer techniques |
| **High** | Dynamic Programming | Medium - Hard | Stock buy & sell variations, minimum path costs, coin change variants |
| **High** | HashMaps & Frequency Counting | Easy - Medium | Anagram grouping, prefix frequency checks, first non-repeating character |
| **Medium** | Graph Traversals & Shortest Path | Medium - Hard | Dijkstra on currency arbitrage, DAG reachability |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Currency Arbitrage / Maximum Profit Chain
- **Problem Summary:** Given a matrix of exchange rates between $N$ currencies, determine if a cycle exists where a trader can start with 1 unit of a currency and make a strictly greater return through a series of trades (Negative cycle in log space).
- **Approach:** Floyd-Warshall or Bellman-Ford on $-\log(\text{rate})$.
- **Complexity:** $O(N^3)$ Time.

### 2. Run Length Encoding / String Compression
- **Problem Summary:** Given a string $s$, compress it such that consecutive identical characters are replaced with the character and its frequency count.
- **LeetCode Equivalent:** [443. String Compression](https://leetcode.com/problems/string-compression/)
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

### 3. High Five / Student Average Scores
- **Problem Summary:** Given a list of scores for different students, return each student's top 5 average score, sorted by student ID.
- **Approach:** Hash map mapping `student_id -> min_heap` of size at most 5.
- **Complexity:** $O(N \log 5) = O(N)$ Time.

### 4. Maximum Stock Profit with Cooldown / Transaction Fees
- **Problem Summary:** You are given an array `prices` where `prices[i]` is the price of a given stock on the $i$-th day. Calculate maximum profit under transaction constraints.
- **Approach:** State-machine dynamic programming with states: `Hold`, `Sold`, `Rest`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧮 Frequently Asked Mathematics & Quantitative MCQs
1. **Expected Rolls for a Fair Die:** What is the expected number of rolls to get all numbers from 1 to 6?
   - *Solution:* Harmonic sum $6 \times (1 + \frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \frac{1}{5} + \frac{1}{6}) = 14.7$ rolls.
2. **Bayes' Theorem on Rare Diseases:** Probability of true infection given test accuracy of 99% and prevalence of 0.1%.
3. **Card Selection:** Probability of drawing 2 aces in a row without replacement from a standard 52-card deck.
