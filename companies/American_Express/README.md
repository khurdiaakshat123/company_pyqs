# American Express (Amex) Online Assessment Guide & PYQs (2023 - 2025/2026) 💳

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerEarth** / **Aon CoCubes**
- **Test Duration:** 90 to 105 minutes
- **Structure Breakdown:**
  1. **Technical MCQs:** 15 to 20 Questions covering Data Structures, SQL/DBMS, OS, and Probability/Aptitude (30 mins).
  2. **Coding Section:** 2 to 3 Coding Questions (Medium difficulty, 60–75 mins).
- **Passing Cutoff:** Full score on at least 1.5 coding questions + high accuracy on SQL and DBMS MCQs is required for interview calls.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Dynamic Programming | Medium - Hard | Subset sum, maximum points from cards, knapsack variants, bounded transfers |
| **Very High** | Arrays & Prefix Sums | Medium | Subarray sum divisible by K, running balance tracking, interval scheduling |
| **High** | SQL Queries & Database MCQs | Medium | Joins, group by with having, window functions (`RANK()`, `DENSE_RANK()`), ACID |
| **High** | Strings & HashMaps | Easy - Medium | Substring matching, frequency maps, group anagrams |
| **Medium** | Graph Reachability | Medium | Connected components, BFS path checking |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Maximum Score from Card Points (Amex Classic)
- **Problem Summary:** There are several cards arranged in a row, and each card has an associated number of points. In one step, you can take one card from the beginning or from the end of the row. You have to take exactly $k$ cards. Your score is the sum of the points of the cards you have taken. Return the maximum score you can obtain.
- **LeetCode Equivalent:** [1423. Maximum Score from You Can Obtain from Cards](https://leetcode.com/problems/maximum-points-you-can-obtain-from-cards/)
- **Approach:** Sliding window of size $N - k$. Find the contiguous subarray of size $N - k$ with the minimum sum, then subtract it from total points.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 2. Subarray Sums Divisible by K
- **Problem Summary:** Given an integer array `nums` and an integer $k$, return the number of non-empty subarrays that have a sum divisible by $k$.
- **LeetCode Equivalent:** [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- **Approach:** Prefix sums with modulo arithmetic: `rem = ((sum % k) + k) % k`. Count frequency of each remainder using a HashMap.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

### 3. Credit Card Fraud Detection / Anomaly Detection
- **Problem Summary:** Given a stream of transactions `[amount, timestamp, city]`, flag any transaction where an amount $\ge 1000$ occurs or where two transactions in different cities occur within 60 minutes.
- **Approach:** Sort by timestamp, maintain a sliding window of transactions for each cardholder ID.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

### 4. Coin Change II / Transaction Combinations
- **Problem Summary:** You are given an integer array `coins` representing coins of different denominations and an integer `amount`. Return the number of combinations that make up that amount.
- **LeetCode Equivalent:** [518. Coin Change II](https://leetcode.com/problems/coin-change-ii/)
- **Approach:** Unbounded Knapsack DP: `dp[w] += dp[w - coin]`.
- **Complexity:** $O(N \times \text{amount})$ Time, $O(\text{amount})$ Space.

---

## 🧠 Frequent SQL Queries Asked in Amex OA
```sql
-- Find the 3rd highest transaction amount per user
WITH RankedTransactions AS (
    SELECT user_id, amount,
           DENSE_RANK() OVER (PARTITION BY user_id ORDER BY amount DESC) as rnk
    FROM Transactions
)
SELECT user_id, amount
FROM RankedTransactions
WHERE rnk = 3;
```
