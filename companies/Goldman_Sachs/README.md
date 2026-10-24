# Goldman Sachs Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 135 minutes total (timed section by section)
- **Sections Breakdown:**
  1. **Section 1: Coding (DSA)** – 2 Questions (60 minutes).
  2. **Section 2: Quantitative Aptitude & Mathematics** – 8 to 10 Questions (20 minutes). Heavy weightage on Probability, Combinatorics, and Financial Math.
  3. **Section 3: Computer Science Fundamentals** – 7 to 10 MCQs (20 minutes). OS, DBMS, Algorithms.
  4. **Section 4: Subjective / Behavioral Writing** – 2 short essay questions on financial ethics or problem handling (15 minutes).
- **Negative Marking:** Present in MCQ sections (+5 for correct, -2 for incorrect, or +1, -0.25). Guesswork is strictly discouraged.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Probability & Combinatorics:** Bayes' Theorem, expected value, card/dice distributions, conditional probability, derangements.
- **Array & String Manipulation:** Better compression, run-length encoding, cyclic shifts, subarray balance, 2-pointer techniques.
- **Dynamic Programming:** Stock buy & sell variations, knight probability, minimum path costs, coin change variants.
- **HashMaps & Priority Queues:** Resource priority tracker, high five scores, reorganize string, anagram grouping.
- **Graph Traversals & Shortest Path:** Currency arbitrage via negative cycle detection, DAG reachability.

---

## 📝 Verified Multi-Year OA Question Bank (Past 3 Years)
*Every problem listed below is a distinct, verified question sourced from 2023, 2024, and 2025/2026 campus placement drives (IITs, NITs, BITS, DTU) and off-campus HackerRank tests. Duplicates across college slots have been strictly merged.*

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Currency Arbitrage / Negative Cycle Detection
- **College/Drive:** IIT Roorkee / IIT Kanpur 2024
- **Problem Summary:** Given a matrix of exchange rates between $N$ currencies, determine if a cycle exists where a trader can start with 1 unit of a currency and make a strictly greater return through a series of trades (Negative cycle in log space).
- **Approach:** Floyd-Warshall or Bellman-Ford on $-\log(\text{rate})$.
- **Complexity:** $O(N^3)$ Time.

#### 2. Better Compression of String (Merge Characters and Sum Counts)
- **College/Drive:** Goldman Sachs Campus Drive 2024
- **Problem Summary:** You are given an alphanumeric string consisting of letters followed by counts (e.g., `"a3c9b2c1"` or `"a12c4b2a1"`). Return the compressed version where counts for identical characters are summed together, characters are ordered in alphabetical order, and formatted as `char + total_count` (e.g., `"a13b2c10"`). Note counts can exceed single digits.
- **Approach:** Parse string using string stream or pointers; extract character and multi-digit integer. Accumulate in a 26-element array. Reconstruct output string in sorted order.
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
- **Complexity:** $O(K \cdot N^2)$ Time, $O(N^2)$ Space.

#### 5. String Burst / Cascading Duplicate Removal
- **College/Drive:** BITS Pilani / NIT Warangal 2024
- **Problem Summary:** Given a string $S$ and an integer $K$, repeatedly remove all contiguous blocks of identical characters of length $\ge K$. When characters are removed, the remaining left and right segments concatenate, which may trigger new burst removals. Continue until no such block exists.
- **LeetCode Equivalent:** [1209. Remove All Adjacent Duplicates in String II](https://leetcode.com/problems/remove-all-adjacent-duplicates-in-string-ii/)
- **Approach:** Stack storing pairs of `(char, consecutive_count)`. If count reaches $K$, pop from stack. Reconstruct string from stack contents.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 6. Matrix Special Elements (Row/Column Extremas)
- **College/Drive:** Goldman Sachs India Off-Campus 2024
- **Problem Summary:** Given an $M \times N$ integer matrix, an element is defined as "special" if it is strictly the minimum in its row and strictly the maximum in its column (or vice versa). Count all special elements in the matrix.
- **LeetCode Equivalent:** [1380. Lucky Numbers in a Matrix](https://leetcode.com/problems/lucky-numbers-in-a-matrix/)
- **Approach:** Compute row minimums array and column maximums array. Find elements that appear in both.
- **Complexity:** $O(M \times N)$ Time, $O(M + N)$ Space.

#### 7. Resource Priority / Update Tracker (LRU / Ordered Map)
- **College/Drive:** Goldman Sachs SDE-1 Screening 2024
- **Problem Summary:** Maintain a real-time stream of incoming financial price quotes `(ticker, price, timestamp)`. Updates should override older quotes, but when queried, tickers must be returned strictly in order of their initial appearance timestamp.
- **Approach:** Hash Map mapping `ticker -> current_price`, combined with an array/list maintaining the unique order of discovery.
- **Complexity:** $O(1)$ update, $O(N)$ report.

#### 8. Minimum Size Subarray Sum
- **College/Drive:** Campus Placement Drive 2024
- **Problem Summary:** Given an array of positive integers `nums` and a positive integer `target`, return the minimal length of a contiguous subarray of which the sum is greater than or equal to `target`. If there is no such subarray, return 0.
- **LeetCode Equivalent:** [209. Minimum Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/)
- **Approach:** Sliding window with two pointers (`left`, `right`). Expand `right`, shrink `left` while sum $\ge target$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Find Missing and Repeated Values in 1 to N
- **College/Drive:** Goldman Sachs On-Campus 2024
- **Problem Summary:** Given an $N \times N$ 2D grid containing integers from $1$ to $N^2$ where one number is repeated twice and one number is missing. Find both numbers.
- **LeetCode Equivalent:** [2965. Find Missing and Repeated Values](https://leetcode.com/problems/find-missing-and-repeated-values/)
- **Approach:** Gauss Sum Difference: Compute $S_1 = \sum x - \sum \text{expected}$ and $S_2 = \sum x^2 - \sum \text{expected}^2$. Solve linear system for missing and repeated values.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Extra Space.

#### 10. Reorganize String (Max-Heap Priority)
- **College/Drive:** Goldman Sachs Quant Tech 2024
- **Problem Summary:** Given a string $s$, rearrange the characters of $s$ so that any two adjacent characters are not the same. Return empty string if impossible.
- **LeetCode Equivalent:** [767. Reorganize String](https://leetcode.com/problems/reorganize-string/)
- **Approach:** Max-Heap of character frequencies. Greedily pop top two most frequent distinct characters and append to result.
- **Complexity:** $O(N \log 26) = O(N)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Run Length Encoding / String Compression
- **College/Drive:** BITS Pilani / NIT Trichy 2023
- **Problem Summary:** Compress consecutive identical characters in-place.
- **LeetCode Equivalent:** [443. String Compression](https://leetcode.com/problems/string-compression/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Best Time to Buy and Sell Stock with Transaction Fee
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Maximum profit with multiple buy and sell transactions subject to a flat transaction fee.
- **LeetCode Equivalent:** [714. Best Time to Buy and Sell Stock with Transaction Fee](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-transaction-fee/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 13. Fraction to Recurring Decimal
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Given two integers representing numerator and denominator of a fraction, return the fraction in string format. If the fractional part is repeating, enclose the repeating part in parentheses.
- **LeetCode Equivalent:** [166. Fraction to Recurring Decimal](https://leetcode.com/problems/fraction-to-recurring-decimal/)
- **Approach:** Long division simulation using a Hash Map mapping `remainder -> index in result string` to detect cycle start.
- **Complexity:** $O(\text{denominator})$ Time.

#### 14. Median of Two Sorted Arrays
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find median of two sorted arrays of size $M$ and $N$ in $O(\log(\min(M, N)))$ time.
- **LeetCode Equivalent:** [4. Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)
- **Approach:** Binary search on the partition of the smaller array.
- **Complexity:** $O(\log(\min(M, N)))$ Time, $O(1)$ Space.

#### 15. Trapping Rain Water
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Compute amount of trapped water between elevation map bars after rain.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers inward maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. Decode Ways (Dynamic Programming)
- **College/Drive:** Campus Slot 3 (2023)
- **Problem Summary:** A message containing letters from A-Z can be encoded into numbers using mapping 'A' -> "1", ..., 'Z' -> "26". Given a string of digits, determine total number of ways to decode it.
- **LeetCode Equivalent:** [91. Decode Ways](https://leetcode.com/problems/decode-ways/)
- **Approach:** Space-optimized DP: $dp[i] = dp[i-1]$ (if valid single digit) $+ dp[i-2]$ (if valid two-digit number $\in [10, 26]$).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 17. Grid Pathfinding with Dynamic Obstacles / Penalties
- **College/Drive:** Advanced SWE Slot 2023
- **Problem Summary:** Find minimum cost path from top-left to bottom-right of matrix where each step incurs cell cost and entering an obstacle cell costs additional penalty $P$.
- **Approach:** Dijkstra's Algorithm or 2D Dynamic Programming table.
- **Complexity:** $O(M \times N \log(M \times N))$ Time.

---

### 🧮 Frequently Tested Quantitative Math & Probability PYQs
1. **At Least K Heads in N Coin Flips:**
   - *Problem:* A fair coin is tossed $N$ times. What is the probability of getting at least $K$ heads?
   - *Solution:* $\sum_{i=K}^N \binom{N}{i} \left(\frac{1}{2}\right)^N$.
2. **Derangements of N Items (Letters in Envelopes):**
   - *Problem:* What is the probability that none of $N$ letters end up in their correct envelope?
   - *Formula:* $!N = N! \sum_{i=0}^N \frac{(-1)^i}{i!} \approx \frac{N!}{e}$. Probability converges to $\frac{1}{e} \approx 36.79\%$.
3. **Bayes' Theorem Medical Testing:**
   - *Problem:* A disease affects 1 in 1000 people. A test is 99% accurate (1% false positive, 1% false negative). If a person tests positive, what is the probability they actually have the disease?
   - *Calculation:*
     $$P(D \mid +) = \frac{P(+ \mid D) P(D)}{P(+ \mid D) P(D) + P(+ \mid \neg D) P(\neg D)} = \frac{0.99 \times 0.001}{(0.99 \times 0.001) + (0.01 \times 0.999)} \approx 9.01\%$$
