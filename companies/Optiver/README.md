# Optiver Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) ⚡

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank Desktop** (Strictly proctored with full screen, webcam, and system process tracking)
- **Test Duration:** 90 to 120 minutes
- **Structure Breakdown (Multi-Component Assessment):**
  1. **Low-Level Design (LLD) & Financial Simulation:** Rather than isolated algorithmic functions, Optiver requires candidates to implement structural classes, interfaces, and methods for a complete financial engine (e.g., Future Pricing Engine, Limit Order Book, Smart Order Router).
  2. **Technical MCQs Section:** 10 to 15 MCQs covering Operating Systems, Computer Networks (Socket communication, TCP/UDP latency, kernel bypass), and Algorithms.
  3. **Zap-N Cognitive & Mental Math Screen:** Fast-paced assessment with 80 arithmetic questions in 8 minutes (addition, subtraction, multiplication, fractions) with negative marking, alongside reflex games.
- **Evaluation Criteria:**
  - Optiver is an elite global proprietary trading and market-making firm.
  - Clean object-oriented architecture, correct edge-case handling, and numerical precision (floating-point tolerances) are strictly scrutinized.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Low-Level Class Design & Simulation:** Building trading engines, order books, dividend adjustments, future pricing models.
- **Binary Search on Time Series:** Querying closest timestamps, dividend impact before maturity, sliding window rates.
- **Computer Networks & Latency MCQs:** TCP/UDP sockets, kernel bypass (Solarflare, DPDK), packet drop handling, round-trip time.
- **Data Structures & Heaps:** Price level ordering, depth of book tracking, transaction matching.
- **Concurrency & Memory Management:** Cache invalidation, atomic updates, lock contention, memory ordering.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Future Pricing Engine (Optiver Signature OA)
- **College/Drive:** IIT Delhi / IIT Bombay Campus Hiring 2024–2025
- **Problem Summary:** Implement a `FuturePricingEngine` that calculates theoretical future prices of an underlying stock contract with maturity timestamp $T$.
  - Support operations:
    - `addDividend(timestamp, amount)`: records cash dividends paid by underlying asset.
    - `updateStockPrice(timestamp, price)`: updates underlying price.
    - `calculateFuturePrice(timestamp, maturity, risk_free_rate)`: returns theoretical future price using the formula:
      $$F = (S - \text{PV}(\text{Dividends})) \times e^{r \times (T - t)}$$
      where $\text{PV}(\text{Dividends}) = \sum \text{div}_i \times e^{-r \times (t_{\text{div}} - t)}$ for all dividends occurring between current time $t$ and maturity $T$.
- **Constraints:** Up to $10^5$ events and queries; timestamps strictly non-decreasing.
- **Approach:** Maintain dividends in a sorted structure (`std::map` in C++ / `bisect` in Python). Use Binary Search (`upper_bound`) to find dividends falling strictly in the window $[t, T]$.
- **Complexity:** $O(\log K)$ per query where $K$ is total dividend events.

#### 2. Continuous Limit Order Book Matching Engine
- **College/Drive:** IIT Madras / BITS Pilani 2024–2025
- **Problem Summary:** Maintain bid and ask orders. Match incoming market orders at best prices; support order cancellation by `order_id` in $O(1)$ or $O(\log N)$ time.
- **Constraints:** Up to $10^5$ orders; price precision 2 decimals.
- **Approach:** Map of Price Levels (`std::map<double, std::list<Order>>`) combined with HashMap mapping `order_id -> std::list<Order>::iterator` for fast cancellation.
- **Complexity:** $O(\log P)$ where $P$ is distinct price levels.

#### 3. Smart Order Router (SOR) with Latency & Fees
- **College/Drive:** IIT Kanpur / CMU Off-Campus 2024–2025
- **Problem Summary:** A trader wants to buy $Q$ shares. Multiple exchanges offer shares at various price levels, each with an associated execution fee and network latency. Route orders to minimize total cost including penalty for delay.
- **Constraints:** Exchanges $\le 20$, total available depth $\ge Q$.
- **Approach:** Greedy matching sorted by effective cost `(price + fee_per_share + latency_penalty)` or Min-Cost Flow / Knapsack DP.
- **Complexity:** $O(E \log E)$ Time.

#### 4. Fast Log Server Timeline Tracker
- **College/Drive:** Optiver Global SWE Screening 2024–2025
- **Problem Summary:** Design a logging server that records timestamps of client events and supports queries: `recordLog(timestamp)`, `getLogsInWindow(start, end)`, and `purgeOldLogs(threshold)`.
- **Constraints:** $10^6$ operations; memory strictly bounded.
- **Approach:** Circular ring buffer / Deque with binary search for window queries.
- **Complexity:** $O(1)$ amortized record, $O(\log N)$ query.

#### 5. Sliding Window Realized Volatility Calculator
- **College/Drive:** Campus Placement 2024–2025
- **Problem Summary:** Given a real-time stream of stock prices, compute the annualized realized volatility over the last $W$ seconds at each price arrival.
- **Constraints:** Stream length $N \le 10^6$, window $W \le 3600$.
- **Approach:** Maintain log returns in a sliding window deque. Update running sum of returns and sum of squared returns in $O(1)$ time to compute standard deviation.
- **Complexity:** $O(1)$ per stream update, $O(W)$ Space.

#### 6. Spot-Perpetual Funding Rate Arbitrage Engine
- **College/Drive:** Optiver Amsterdam / London Drive 2024
- **Problem Summary:** Model cash-and-carry arbitrage opportunities between spot and perpetual futures. Given exchange funding rates paid every 8 hours, compute optimal rebalancing schedule given borrowing costs and trading fees.
- **Constraints:** Lookback window $T = 365$ days, trading fee $0.05\%$.
- **Approach:** Dynamic programming over discrete rebalancing states maximizing cumulative net return after borrowing cost and slip fees.
- **Complexity:** $O(T)$ Time, $O(1)$ Space.

#### 7. Minimum Latency Route in Colocation Network
- **College/Drive:** IIT Delhi / IIT Bombay 2024
- **Problem Summary:** Direct fiber connections between global exchange matching engines have transmission latency and drop probabilities. Find the route that achieves packet delivery within timeout $T$ while minimizing total transmission latency.
- **Constraints:** $V \le 500, E \le 3000$.
- **Approach:** Modified Dijkstra on state `(node, accumulated_latency)` or Bellman-Ford DP `dp[u][t]` = min drop probability within latency $t$.
- **Complexity:** $O(E \cdot T)$ Time, $O(V \cdot T)$ Space.

#### 8. Options Delta-Hedging Portfolio Balancer
- **College/Drive:** Quant Research Slot 2024
- **Problem Summary:** Maintain a delta-neutral options portfolio. As underlying price $S$ fluctuates, rebalance stock holdings only when portfolio $|\Delta| > \Delta_{\text{threshold}}$ to minimize transaction costs.
- **Constraints:** $N \le 10^5$ ticks, options contracts $K \le 50$.
- **Approach:** Streaming simulation tracking aggregate portfolio delta $\sum w_i \Delta_i(S)$. Greedily buy/sell shares to reset delta to 0 upon crossing threshold.
- **Complexity:** $O(N \cdot K)$ Time, $O(K)$ Space.

#### 9. High-Frequency Market Making Quoting Engine
- **College/Drive:** Optiver Sydney SWE / Quant 2024
- **Problem Summary:** Implement the Avellaneda-Stoikov market making inventory model. Calculate reservation price $R(s, q, t) = s - q \gamma \sigma^2 (T - t)$ and optimal bid/ask quote spreads around $R$ given inventory $q$ and inventory risk parameter $\gamma$.
- **Constraints:** Closed-form evaluation on streaming tick feed.
- **Approach:** Direct $O(1)$ pricing evaluation per tick; update bid/ask quotes in order book.
- **Complexity:** $O(1)$ Time per price tick.

#### 10. Sliding Window VWAP with Exponential Decay
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** Calculate Volume-Weighted Average Price (VWAP) where historical volume decays exponentially with half-life $\tau$:
  $$\text{VWAP} = \frac{\sum P_i V_i e^{-\lambda (t - t_i)}}{\sum V_i e^{-\lambda (t - t_i)}}$$
- **Constraints:** Continuous real-time feed of ticks.
- **Approach:** Exponential Moving Average (EMA) state tracking. Update numerator and denominator in $O(1)$ time by multiplying existing state by $e^{-\lambda \Delta t}$ before adding new tick.
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Currency Arbitrage Detection (Negative Cycle Bellman-Ford)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Given currency exchange matrix, detect if an arbitrage path exists that yields profit $> 1.0$.
- **Constraints:** $N \le 100$ currencies.
- **Approach:** Bellman-Ford using $-\log(\text{rate})$ weights to detect negative weight cycles.
- **Complexity:** $O(V \cdot E)$ Time.

#### 12. Lock-Free SPSC Ring Buffer Simulator
- **College/Drive:** Systems Screening 2023
- **Problem Summary:** Single-producer single-consumer circular queue without locks.
- **Constraints:** Atomic read/write pointers, power-of-two capacity.
- **Approach:** Atomic head and tail pointers with power-of-two size mask (`index & (capacity - 1)`).
- **Complexity:** $O(1)$ push/pop.

#### 13. Top K Traded Equities in Streaming Ticker
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Continuously report top $K$ traded instruments by total dollar volume.
- **Constraints:** Unique equities up to $10^5$, updates $10^6$.
- **Approach:** Hash Map for instrument volume + Min-Heap of size $K$.
- **Complexity:** $O(\log K)$ per update.

#### 14. Option Greeks Sensitivity Numerical Approximation
- **College/Drive:** Quant Trader Screening 2023
- **Problem Summary:** Compute finite difference delta and gamma approximations for European call option under Black-Scholes.
- **Approach:** Numerical differentiation: $\Delta \approx \frac{C(S+\epsilon) - C(S-\epsilon)}{2\epsilon}$, $\Gamma \approx \frac{C(S+\epsilon) - 2C(S) + C(S-\epsilon)}{\epsilon^2}$.
- **Complexity:** $O(1)$ Time.

#### 15. Zap-N Fast-Paced Mental Arithmetic Benchmark
- **Format:** 80 arithmetic questions in 8 minutes (fractions, 2-digit multiplications, percentage conversions).
- **Benchmark:** Passing cutoff typically requires $\ge 65+$ correct answers with $> 90\%$ accuracy.

#### 16. Trapping Rain Water in Order Profiles
- **College/Drive:** IIT Kanpur Slot 2023
- **Problem Summary:** Compute total units of trapped area across an uneven bar profile representing order depth gaps.
- **Constraints:** $1 \le n \le 3 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 17. Merge Intervals / Exchange Maintenance Windows
- **College/Drive:** Systems Placement 2023
- **Problem Summary:** Given an array of maintenance intervals, merge all overlapping intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time; iterate through intervals extending end time if overlapping.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 18. LRU Cache with $O(1)$ Priority Tie-Breaking
- **College/Drive:** Off-Campus SWE 2023
- **Problem Summary:** Implement Least Recently Used (LRU) cache with capacity $C$.
- **Constraints:** $C \le 3000$, up to $10^5$ operations.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Hash Map mapping key to node iterator in Doubly Linked List.
- **Complexity:** $O(1)$ Time per get and put.

#### 19. Maximum Average Subarray with Minimum Window Length
- **College/Drive:** Advanced Screening 2023
- **Problem Summary:** Find contiguous subarray of length at least $k$ that has the maximum average value.
- **Constraints:** $1 \le k \le n \le 10^4$.
- **LeetCode Equivalent:** [644. Maximum Average Subarray II](https://leetcode.com/problems/maximum-average-subarray-ii/)
- **Approach:** Binary Search on answer average value $M$. Check if there exists a subarray of length $\ge k$ with sum of $(nums[i] - M) \ge 0$ using prefix sums.
- **Complexity:** $O(N \log(\text{range} / \epsilon))$ Time, $O(N)$ Space.

#### 20. Search in Rotated Sorted Order Log
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Given a sorted array rotated at an unknown pivot, find index of target in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 5000$.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Modified Binary Search determining whether the left half or right half is sorted at each midpoint.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent Networking & Systems MCQs in Optiver OA
1. **Kernel Bypass Technologies:**
   - Why do HFT firms use Kernel Bypass (e.g. Solarflare OpenOnload, DPDK) instead of standard Linux sockets?
   - *Answer:* Standard sockets involve context switches between user space and kernel space, OS interrupts, and socket buffer copies. Kernel bypass maps network card buffers directly into user memory, reducing network latency from ~5 microseconds to sub-microsecond levels.
2. **TCP Nagle's Algorithm (`TCP_NODELAY`):**
   - Why do trading systems disable Nagle's algorithm by setting `TCP_NODELAY`?
   - *Answer:* Nagle's algorithm buffers small packets until an ACK is received to improve network bandwidth efficiency, introducing up to 200ms latency delays that are unacceptable for low-latency trading.
3. **Core Pinning & Cache Affinity:**
   - What is the benefit of thread CPU pinning (`pthread_setaffinity_np`) and CPU isolation (`isolcpus`)?
   - *Answer:* Pinning prevents OS thread migration between cores, keeping L1/L2 cache lines hot and eliminating OS scheduler interrupts from preempting execution.
