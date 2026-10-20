# Optiver Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) ⚡

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank Desktop** (Strictly proctored with full screen, webcam, and system process tracking)
- **Test Duration:** 90 to 120 minutes
- **Structure Breakdown (Multi-Component Assessment):**
  1. **Low-Level Design (LLD) & Financial Simulation:** Rather than isolated algorithmic functions, Optiver requires candidates to implement structural classes, interfaces, and methods for a complete financial engine (e.g., Future Pricing Engine, Limit Order Book, or Log Server).
  2. **Technical MCQs Section:** 10 to 15 MCQs covering Operating Systems, Computer Networks (Socket communication, TCP/UDP latency), and Algorithms.
  3. **Zap-N Cognitive & Reflex Games:** Fast-paced gamified assessment measuring numerical speed, memory recall, pattern recognition, and risk tolerance under tight time pressure.
- **Evaluation Criteria:**
  - Optiver is an elite global proprietary trading and market-making firm.
  - Clean object-oriented architecture, correct edge-case handling, and numerical precision (floating-point tolerances) are strictly scrutinized.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Extremely High** | Low-Level Class Design & Simulation | Hard | Building trading engines, order books, dividend adjustments, pricing engines |
| **Very High** | Binary Search on Time Series | Medium - Hard | Querying closest timestamps, dividend impact before maturity |
| **High** | Computer Networks & Latency MCQs | Medium - Hard | TCP/UDP sockets, kernel bypass, packet drop handling, round-trip time |
| **High** | Data Structures & Heaps | Medium - Hard | Price level ordering, depth of book tracking, transaction matching |
| **Medium** | Concurrency & Memory Management | Medium - Hard | Cache invalidation, atomic updates, lock contention |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Future Pricing Engine (Optiver Signature OA)
- **Problem Summary:** Implement a `FuturePricingEngine` that calculates theoretical future prices of an underlying stock contract with maturity timestamp $T$.
  - Support operations:
    - `addDividend(timestamp, amount)`: records cash dividends paid by underlying asset.
    - `updateStockPrice(timestamp, price)`: updates underlying price.
    - `calculateFuturePrice(timestamp, maturity, risk_free_rate)`: returns theoretical future price using the formula:
      $$F = (S - \text{PV}(\text{Dividends})) \times e^{r \times (T - t)}$$
      where $\text{PV}(\text{Dividends}) = \sum \text{div}_i \times e^{-r \times (t_{\text{div}} - t)}$ for all dividends occurring between current time $t$ and maturity $T$.
- **Approach:** Maintain dividends in a sorted structure (`std::map` in C++ / `bisect` in Python). Use Binary Search (`upper_bound`) to find dividends falling strictly in the window $[t, T]$.
- **Complexity:** $O(\log K)$ per query where $K$ is total dividend events.

### 2. Fast Log Server Timeline Tracker
- **Problem Summary:** Design a logging server that records timestamps of client events and supports queries: `recordLog(timestamp)`, `getLogsInWindow(start, end)`, and `purgeOldLogs(threshold)`.
- **Approach:** Circular ring buffer / Deque with binary search for window queries.
- **Complexity:** $O(1)$ amortized record, $O(\log N)$ query.

### 3. Continuous Limit Order Book Matching
- **Problem Summary:** Maintain bid and ask orders. Match incoming market orders at best prices; support order cancellation by `order_id` in $O(1)$ or $O(\log N)$ time.
- **Approach:** Map of Price Levels (`std::map<double, list<Order>>`) combined with HashMap mapping `order_id -> list::iterator`.
- **Complexity:** $O(\log P)$ where $P$ is distinct price levels.

### 4. Zap-N Mental Arithmetic Test
- Rapid-fire mental math: 80 arithmetic questions in 8 minutes (addition, subtraction, multiplication, fractions) with negative marking for incorrect guesses. Passing requires high speed ($\ge 65+$ correct answers with $> 90\%$ accuracy).
