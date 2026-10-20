# Goldman Sachs Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏛️

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

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Probability & Combinatorics:** Bayes' Theorem, expected value, card/dice distributions, conditional probability.
- **Array & String Manipulation:** Run-length encoding, cyclic shifts, subarray balance, 2-pointer techniques.
- **Dynamic Programming:** Stock buy & sell variations, minimum path costs, coin change variants.
- **HashMaps & Frequency Counting:** Anagram grouping, prefix frequency checks, first non-repeating character.
- **Graph Traversals & Shortest Path:** Dijkstra on currency arbitrage, DAG reachability.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Currency Arbitrage / Negative Cycle Detection
- **College/Drive:** IIT Roorkee / IIT Kanpur 2024
- **Problem Summary:** Given a matrix of exchange rates between $N$ currencies, determine if a cycle exists where a trader can start with 1 unit of a currency and make a strictly greater return through a series of trades (Negative cycle in log space).
- **Approach:** Floyd-Warshall or Bellman-Ford on $-\log(\text{rate})$.
- **Complexity:** $O(N^3)$ Time.

#### 2. Run Length Encoding / String Compression
- **College/Drive:** BITS Pilani / NIT Trichy 2024
- **Problem Summary:** Given a string $s$, compress it such that consecutive identical characters are replaced with the character and its frequency count.
- **LeetCode Equivalent:** [443. String Compression](https://leetcode.com/problems/string-compression/)
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 3. High Five / Student Average Scores
- **College/Drive:** DTU / NSUT 2024
- **Problem Summary:** Given a list of scores for different students, return each student's top 5 average score, sorted by student ID.
- **Approach:** Hash map mapping `student_id -> min_heap` of size at most 5.
- **Complexity:** $O(N \log 5) = O(N)$ Time.

#### 4. Knight Probability in Chessboard (2D DP / Probability)
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Summary:** On an $n \times n$ chessboard, a knight starts at cell `(row, column)` and makes $k$ moves. Each move is chosen uniformly from the 8 possible moves. Return the probability that the knight remains on the board after making $k$ moves.
- **LeetCode Equivalent:** [688. Knight Probability in Chessboard](https://leetcode.com/problems/knight-probability-in-chessboard/)
- **Approach:** 3D DP: $dp[k][r][c] = \sum_{\text{dirs}} \frac{1}{8} dp[k-1][nr][nc]$.
- **Complexity:** $O(K \times N^2)$ Time, $O(N^2)$ Space.

#### 5. Best Time to Buy and Sell Stock with Cooldown
- **College/Drive:** Engineering Campus Hiring 2024
- **Problem Summary:** Given daily prices, maximize profit with mandatory 1-day cooldown after selling.
- **LeetCode Equivalent:** [309. Best Time to Buy and Sell Stock with Cooldown](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-cooldown/)
- **Approach:** State-machine DP with 3 states: `hold`, `sold`, `rest`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. First Unique Character in a String
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Return index of first non-repeating character in string.
- **LeetCode Equivalent:** [387. First Unique Character in a String](https://leetcode.com/problems/first-unique-character-in-a-string/)
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 7. Trapping Rain Water (Two Pointers)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Calculate total water trapped in elevation histogram.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Fractional Knapsack Problem (Greedy)
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Maximize value under capacity constraint allowing fractional picks.
- **Approach:** Sort items descending by value-to-weight ratio $\frac{V_i}{W_i}$.
- **Complexity:** $O(N \log N)$ Time.

#### 9. Minimum Size Subarray Sum
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Smallest subarray whose sum $\ge \text{target}$.
- **LeetCode Equivalent:** [209. Minimum Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 10. Maximum Subarray Product
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Contiguous subarray with largest product.
- **LeetCode Equivalent:** [152. Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/)
- **Complexity:** $O(N)$ Time.

---

## 🧮 Frequently Asked Mathematics & Quantitative MCQs
1. **Expected Rolls for a Fair Die:** What is the expected number of rolls to get all numbers from 1 to 6?
   - *Solution:* Harmonic sum $6 \times (1 + \frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \frac{1}{5} + \frac{1}{6}) = 14.7$ rolls.
2. **Bayes' Theorem on Rare Diseases:** Probability of true infection given test accuracy of 99% and prevalence of 0.1%.
3. **Card Selection:** Probability of drawing 2 aces in a row without replacement from a standard 52-card deck: $\frac{4}{52} \times \frac{3}{51} = \frac{1}{221}$.
