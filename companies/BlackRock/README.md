# BlackRock Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🏛️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Financial & Technical MCQs (30 mins):** 15 MCQs covering Data Structures, SQL, OOPs, and Financial/Quantitative calculations (portfolio returns, interest formulas).
  2. **Coding Section (60 mins, 2 Questions):** Medium difficulty algorithmic questions themed around asset allocation, transactions, and portfolio management (BlackRock Aladdin platform style).
- **Passing Cutoff:** Full score on both coding problems + high accuracy on SQL and financial/CS MCQs.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Portfolio & Transaction Simulations | Medium | Rebalancing portfolios, rounding allocation differences, transaction matching |
| **Very High** | Arrays & Sliding Window | Medium | Subarray max/min differences, running cash flow tracking |
| **High** | SQL Queries & Data Aggregation | Medium | Aggregate portfolio value, top holdings by asset class, joins |
| **High** | Stacks & Queues | Medium | Next greater price, stock span, sliding window maximum |
| **Medium** | Graph Reachability | Medium | Counterparty credit risk graphs, circular debt settlement |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Portfolio Asset Weight Rebalancing
- **Problem Summary:** An investment portfolio holds $N$ assets with current market values $V_i$. Target percentage allocations are given as $T_i$ (where $\sum T_i = 100\%$). Calculate the exact buy/sell transaction amounts required for each asset to achieve target allocation while minimizing total transaction turnover.
- **Approach:** Calculate $\text{total\_value} = \sum V_i$. For each asset, target value is $\text{total\_value} \times \frac{T_i}{100}$. Trade order is $\text{target\_value} - V_i$.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

### 2. Maximum Subarray Sum with Fixed Window Size (Cash Flow Peak)
- **Problem Summary:** Given a stream of positive and negative transaction amounts, find the window of size $K$ that maximizes cumulative net cash flow.
- **Approach:** Standard Fixed-Size Sliding Window.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 3. Currency Rounding & Decimal Precision Balancing
- **Problem Summary:** Round an array of decimal asset weights such that each rounded weight is an integer, and the sum of rounded weights strictly equals 100, while minimizing the total rounding discrepancy.
- **Approach:** Floor all elements, calculate remainder deficit $D = 100 - \sum \lfloor w_i \rfloor$, sort elements by fractional part descending, and increment top $D$ elements by 1.
- **Complexity:** $O(N \log N)$ Time.

### 4. Daily Stock Prices / Next Greater Element
- **Problem Summary:** Given an array of daily stock prices, find the next day with a strictly higher price for every day in the array.
- **LeetCode Equivalent:** [496. Next Greater Element I](https://leetcode.com/problems/next-greater-element-i/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.
