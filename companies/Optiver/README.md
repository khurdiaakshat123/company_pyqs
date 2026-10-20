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
- **College/Drive:** IIT Delhi / IIT Bombay Campus Hiring 2024
- **Problem Summary:** Implement a `FuturePricingEngine` that calculates theoretical future prices of an underlying stock contract with maturity timestamp $T$.
  - Support operations:
    - `addDividend(timestamp, amount)`: records cash dividends paid by underlying asset.
    - `updateStockPrice(timestamp, price)`: updates underlying price.
    - `calculateFuturePrice(timestamp, maturity, risk_free_rate)`: returns theoretical future price using the formula:
      $$F = (S - \text{PV}(\text{Dividends})) \times e^{r \times (T - t)}$$
      where $\text{PV}(\text{Dividends}) = \sum \text{div}_i \times e^{-r \times (t_{\text{div}} - t)}$ for all dividends occurring between current time $t$ and maturity $T$.
- **Approach:** Maintain dividends in a sorted structure (`std::map` in C++ / `bisect` in Python). Use Binary Search (`upper_bound`) to find dividends falling strictly in the window $[t, T]$.
- **Complexity:** $O(\log K)$ per query where $K$ is total dividend events.

#### 2. Continuous Limit Order Book Matching Engine
- **College/Drive:** IIT Madras / BITS Pilani 2024
- **Problem Summary:** Maintain bid and ask orders. Match incoming market orders at best prices; support order cancellation by `order_id` in $O(1)$ or $O(\log N)$ time.
- **Approach:** Map of Price Levels (`std::map<double, std::list<Order>>`) combined with HashMap mapping `order_id -> std::list<Order>::iterator` for fast cancellation.
- **Complexity:** $O(\log P)$ where $P$ is distinct price levels.

#### 3. Smart Order Router (SOR) with Latency & Fees
- **College/Drive:** IIT Kanpur / CMU Off-Campus 2024
- **Problem Summary:** A trader wants to buy $Q$ shares. Multiple exchanges offer shares at various price levels, each with an associated execution fee and network latency. Route orders to minimize total cost including penalty for delay.
- **Approach:** Greedy matching sorted by effective cost `(price + fee_per_share + latency_penalty)` or Min-Cost Flow / Knapsack DP.
- **Complexity:** $O(E \log E)$ Time.

#### 4. Fast Log Server Timeline Tracker
- **College/Drive:** Optiver Global SWE Screening 2024
- **Problem Summary:** Design a logging server that records timestamps of client events and supports queries: `recordLog(timestamp)`, `getLogsInWindow(start, end)`, and `purgeOldLogs(threshold)`.
- **Approach:** Circular ring buffer / Deque with binary search for window queries.
- **Complexity:** $O(1)$ amortized record, $O(\log N)$ query.

#### 5. Sliding Window Realized Volatility Calculator
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Given a real-time stream of stock prices, compute the annualized realized volatility over the last $W$ seconds at each price arrival.
- **Approach:** Maintain log returns in a sliding window deque. Update running sum of returns and sum of squared returns in $O(1)$ time to compute standard deviation.
- **Complexity:** $O(1)$ per stream update, $O(W)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Currency Arbitrage Detection (Negative Cycle Bellman-Ford)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Given currency exchange matrix, detect if an arbitrage path exists that yields profit $> 1.0$.
- **Approach:** Bellman-Ford using $-\log(\text{rate})$ weights.
- **Complexity:** $O(V \cdot E)$ Time.

#### 7. Lock-Free Ring Buffer Simulator
- **College/Drive:** Systems Screening 2023
- **Problem Summary:** Single-producer single-consumer circular queue without locks.
- **Approach:** Atomic head and tail pointers with power-of-two size mask (`index & (capacity - 1)`).
- **Complexity:** $O(1)$ push/pop.

#### 8. Top K Traded Equities in Streaming Ticker
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Continuously report top $K$ traded instruments by total dollar volume.
- **Approach:** Hash Map for instrument volume + Min-Heap of size $K$.
- **Complexity:** $O(\log K)$ per update.

#### 9. Option Greeks Sensitivity Approximation
- **College/Drive:** Quant Trader Screening 2023
- **Problem Summary:** Compute finite difference delta and gamma approximations for European call option under Black-Scholes.
- **Approach:** Numerical differentiation: $\Delta \approx \frac{C(S+\epsilon) - C(S-\epsilon)}{2\epsilon}$, $\Gamma \approx \frac{C(S+\epsilon) - 2C(S) + C(S-\epsilon)}{\epsilon^2}$.
- **Complexity:** $O(1)$ Time.

#### 10. Zap-N Fast-Paced Mental Arithmetic Screen
- **Format:** 80 arithmetic questions in 8 minutes (fractions, 2-digit multiplications, percentage conversions).
- **Benchmark:** Passing cutoff typically requires $\ge 65+$ correct answers with $> 90\%$ accuracy.

---

## 🧠 Frequent Networking & Systems MCQs in Optiver OA
1. **Kernel Bypass Technologies:**
   - Why do HFT firms use Kernel Bypass (e.g. Solarflare OpenOnload, DPDK) instead of standard Linux sockets?
   - *Answer:* Standard sockets involve context switches between user space and kernel space, OS interrupts, and socket buffer copies. Kernel bypass maps network card buffers directly into user memory, reducing network latency from ~5 microseconds to sub-microsecond levels.
2. **TCP Nagle's Algorithm (`TCP_NODELAY`):**
   - Why do trading systems disable Nagle's algorithm by setting `TCP_NODELAY`?
   - *Answer:* Nagle's algorithm buffers small packets until an ACK is received to improve network bandwidth efficiency, introducing up to 200ms latency delays that are unacceptable for low-latency trading.
