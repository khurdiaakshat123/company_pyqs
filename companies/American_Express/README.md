# American Express (Amex) Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) 💳

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerEarth** / **Aon CoCubes**
- **Test Duration:** 90 to 105 minutes
- **Structure Breakdown:**
  1. **Technical MCQs:** 15 to 20 Questions covering Data Structures, SQL/DBMS, OS, and Probability/Aptitude (30 mins).
  2. **Coding Section:** 2 to 3 Coding Questions (Medium difficulty, 60–75 mins).
- **Passing Cutoff:** Full score on at least 1.5 coding questions + high accuracy on SQL and DBMS MCQs is required for interview calls.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Dynamic Programming:** Subset sum, maximum points from cards, knapsack variants, bounded transfers.
- **Arrays & Prefix Sums:** Subarray sum divisible by K, running balance tracking, interval scheduling.
- **SQL Queries & Database MCQs:** Joins, group by with having, window functions (`RANK()`, `DENSE_RANK()`), ACID.
- **Strings & HashMaps:** Substring matching, frequency maps, group anagrams.
- **Graph Reachability:** Connected components, BFS path checking.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Maximum Score from Card Points (Amex Classic)
- **College/Drive:** IIT Roorkee / BITS Pilani 2024
- **Problem Summary:** In one step, you can take one card from the beginning or from the end of the row. You have to take exactly $k$ cards. Return the maximum score you can obtain.
- **LeetCode Equivalent:** [1423. Maximum Score from You Can Obtain from Cards](https://leetcode.com/problems/maximum-points-you-can-obtain-from-cards/)
- **Approach:** Sliding window of size $N - k$. Find the contiguous subarray of size $N - k$ with the minimum sum, then subtract it from total points.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Subarray Sums Divisible by K
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Summary:** Given an integer array `nums` and an integer $k$, return the number of non-empty subarrays that have a sum divisible by $k$.
- **LeetCode Equivalent:** [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- **Approach:** Prefix sums with modulo arithmetic: `rem = ((sum % k) + k) % k`. Count frequency of each remainder using a HashMap.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 3. Credit Card Fraud Detection / Anomaly Detection
- **College/Drive:** IIIT Allahabad 2024
- **Problem Summary:** Given a stream of transactions `[amount, timestamp, city]`, flag any transaction where an amount $\ge 1000$ occurs or where two transactions in different cities occur within 60 minutes.
- **Approach:** Sort by timestamp, maintain a sliding window of transactions for each cardholder ID.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 4. Coin Change II / Transaction Combinations
- **College/Drive:** Off-Campus Drive 2024
- **Problem Summary:** Return the number of combinations that make up that amount with given coins.
- **LeetCode Equivalent:** [518. Coin Change II](https://leetcode.com/problems/coin-change-ii/)
- **Approach:** Unbounded Knapsack DP: `dp[w] += dp[w - coin]`.
- **Complexity:** $O(N \times \text{amount})$ Time, $O(\text{amount})$ Space.

#### 5. Real SQL Question: Third Highest Transaction per User
- **College/Drive:** Amex Campus 2024
- **SQL Implementation:**
  ```sql
  WITH RankedTransactions AS (
      SELECT user_id, amount,
             DENSE_RANK() OVER (PARTITION BY user_id ORDER BY amount DESC) as rnk
      FROM Transactions
  )
  SELECT user_id, amount FROM RankedTransactions WHERE rnk = 3;
  ```

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Group Anagrams
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Statement:** Group strings that are anagrams.
- **LeetCode Equivalent:** [49. Group Anagrams](https://leetcode.com/problems/group-anagrams/)
- **Complexity:** $O(N \cdot K \log K)$ Time.

#### 7. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Statement:** Sliding window with hash map.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time.

#### 8. Merge Intervals
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Merge overlapping transaction settlement times.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time.

#### 9. Number of Islands
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** BFS on 2D grid matrix.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Complexity:** $O(M \times N)$ Time.

#### 10. Maximum Subarray Sum (Kadane's)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Maximum contiguous subarray sum.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Complexity:** $O(N)$ Time.
