# Zscaler Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🔒

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  - 2 to 3 Algorithmic Coding Problems (LeetCode Medium to Hard).
  - (In select campus drives) 10 to 15 Core Networking & Security MCQs (TCP/IP, Firewalls, SSL/TLS Handshake, Reverse Proxies, Zero Trust Architecture).
- **Evaluation Criteria & Strict Warning:**
  - Zscaler operates cloud security and zero-trust exchange platforms worldwide.
  - Automated plagiarism detection is notoriously strict; code mirroring public repositories or exact LeetCode snippets results in immediate disqualification.
  - 100% test case pass on at least 2 questions is required for interview qualification.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Tries & IP Prefix Lookups:** Domain whitelist/blacklist filtering, wildcard matching, CIDR lookup.
- **Log Stream Parsing & HashMaps:** Real-time proxy event deduplication, sliding-window rate limiters.
- **Dynamic Programming & LIS:** Longest increasing subsequence variations, packet ordering, token decoding.
- **Segment Trees & Range Frequency:** Querying packet surges across time intervals.
- **Graphs & Shortest Path:** Network delay time, minimum spanning trees, certificate authority topological sorting.
- **Networking MCQs:** TLS 1.2 vs 1.3, forward proxy vs reverse proxy, TCP 3-way handshake, DNS spoofing, SNI (Server Name Indication).

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Zero Trust Domain Prefix Whitelist (Trie Implementation)
- **College/Drive:** IIT Roorkee / IIT BHU 2024
- **Problem Statement:** A corporate zero-trust firewall maintains a list of $N$ allowed domain wildcards (e.g., `*.google.com`, `internal.*.corp`). Given $Q$ incoming web request URLs, determine whether each URL matches at least one allowed wildcard rule.
- **Approach:** Reverse Trie: Split domains by `.` and insert components in reverse (from TLD backward). Query reverse URL tokens against Trie handling wildcard nodes `*`.
- **Complexity:** $O(L)$ per query where $L$ is domain depth.

#### 2. Network Flow Log Packet Deduplication (Hash + Sliding Window)
- **College/Drive:** NIT Trichy / Warangal 2024
- **Problem Statement:** A security gateway processes incoming TCP packet hashes `(hash, timestamp)`. If a packet with the same hash was processed within the previous $K$ seconds, flag it as a replayed/duplicate packet and drop it. Return the count of dropped packets.
- **Approach:** Hash Map mapping `hash -> last_seen_timestamp`. If $\text{timestamp} - \text{last\_seen} \le K$, increment drop counter; else update timestamp.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 3. Longest Increasing Subsequence / Threat Anomaly Score
- **College/Drive:** BITS Pilani 2024
- **Problem Statement:** Given an array of security threat risk scores over time, find the length of the longest strictly increasing subsequence of threat scores.
- **LeetCode Equivalent:** [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- **Approach:** Patience Sorting with Binary Search (`std::lower_bound`). Maintain array `tails` where `tails[i]` stores smallest tail of all increasing subsequences of length $i+1$.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 4. Range Packet Surge Query (Fenwick Tree / Segment Tree)
- **College/Drive:** DTU / NSUT 2024
- **Problem Statement:** Network sensors record packet counts at second $T$. Process $Q$ queries of two types:
  1. Add $V$ packets at timestamp $T$.
  2. Find total packet count between timestamps $T_1$ and $T_2$.
- **Approach:** Binary Indexed Tree (Fenwick Tree) or Segment Tree with point updates and range sum queries.
- **Complexity:** $O(\log N)$ per update and range query.

#### 5. Sliding Window Maximum / Real-Time Proxy Throughput Spike
- **College/Drive:** IIT Delhi 2024
- **Problem Statement:** Find maximum packet burst in every continuous sliding window of size $K$ across a live network stream.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Approach:** Monotonic Decreasing Deque storing indices. Maintain deque elements strictly decreasing.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 6. Certificate Authority Hierarchy Verification (Course Schedule II)
- **College/Drive:** IIT Bombay 2024
- **Problem Statement:** A public key infrastructure has intermediate certificates with prerequisite parent signatures. Find a valid issuance sequence or detect cyclic dependency.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's algorithm for topological sorting using in-degrees and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 7. Design In-Memory Sliding Window Rate Limiter
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Statement:** Design a per-client API rate limiter allowing at most $M$ requests in any rolling window of $S$ seconds. Return whether request at timestamp $T$ is allowed.
- **Approach:** Hash Map mapping `client_id -> std::deque<timestamp>`. For incoming request at $T$, pop elements from front where $t \le T - S$. If deque size $< M$, push $T$ and allow; else reject.
- **Complexity:** $O(1)$ amortized per request, $O(C \times M)$ Space.

#### 8. Minimum Window Substring / Packet Signature Search
- **College/Drive:** BITS Goa 2024
- **Problem Statement:** Given a raw network payload string `s` and a malware signature string `t`, find the shortest contiguous slice of `s` containing all characters of `t`.
- **LeetCode Equivalent:** [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- **Approach:** Sliding window with character count frequency maps and condition counter.
- **Complexity:** $O(|S| + |T|)$ Time, $O(\Sigma)$ Space.

#### 9. Merge Intervals / Firewall Maintenance Window Consolidation
- **College/Drive:** NIT Surathkal 2024
- **Problem Statement:** Merge overlapping maintenance downtime intervals for high-availability proxies.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort intervals by start time. Merge greedily if `curr.start <= prev.end`.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 10. Malware Lateral Movement Simulation (Rotting Oranges)
- **College/Drive:** DTU Delhi 2024
- **Problem Statement:** Network grid containing clean nodes, infected nodes, and firewalled isolated nodes. Calculate minimum time steps until all clean nodes are infected, or $-1$ if complete infection is blocked.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS initializing queue with all initial infected nodes.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Network Delay Time / Security Broadcast (Dijkstra)
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Calculate time for a security revocation certificate to reach all proxy nodes in a weighted network.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Complexity:** $O(E \log V)$ Time.

#### 12. Minimum Cost to Connect All Data Centers (MST)
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Find minimum total fiber length to connect all regional proxy gateways.
- **LeetCode Equivalent:** [1584. Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)
- **Approach:** Kruskal's algorithm with Disjoint Set Union (DSU) or Prim's algorithm.
- **Complexity:** $O(E \log E)$ Time.

#### 13. Valid Parentheses with Asterisk Wildcard
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Check if security policy rule syntax with `(`, `)`, and `*` wildcard is valid.
- **LeetCode Equivalent:** [678. Valid Parenthesis String](https://leetcode.com/problems/valid-parenthesis-string/)
- **Approach:** Greedy range tracking `min_open` and `max_open`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 14. Subarray Sum Equals K (Threat Threshold)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Find total subsegments whose threat levels sum to exact threshold $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 15. Trapping Rain Water
- **College/Drive:** NSUT Delhi 2023
- **Problem Statement:** Compute water trapped by elevation map.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers inward from boundaries.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. Search in Rotated Sorted Array
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Find index of target in rotated sorted array in $O(\log N)$ time.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Complexity:** $O(\log N)$ Time.

#### 17. Word Break / Payload Signature Matcher
- **College/Drive:** IIT Kharagpur 2023
- **Problem Statement:** Determine if payload string can be split into valid signature keywords.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Approach:** 1D DP boolean array: `dp[i]` is true if prefix `s[0...i-1]` is valid.
- **Complexity:** $O(N^2)$ Time, $O(N)$ Space.

#### 18. LRU DNS Proxy Cache
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Implement an LRU cache with $O(1)$ operations.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Hash Map combined with Doubly Linked List.
- **Complexity:** $O(1)$ Time per operation.

#### 19. Encrypted Tunnel Routing (Reconstruct Itinerary)
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Reconstruct valid routing path visiting all hops in lexicographical order.
- **LeetCode Equivalent:** [332. Reconstruct Itinerary](https://leetcode.com/problems/reconstruct-itinerary/)
- **Approach:** Hierholzer's Eulerian path algorithm.
- **Complexity:** $O(E \log E)$ Time.

#### 20. Chunked Protocol Parsing (Decode String)
- **College/Drive:** University Hiring 2023
- **Problem Statement:** Decode nested string encoding format `k[string]`.
- **LeetCode Equivalent:** [394. Decode String](https://leetcode.com/problems/decode-string/)
- **Approach:** Dual stack for multipliers and string builders.
- **Complexity:** $O(\text{Output Length})$ Time and Space.

---

## 🧠 Frequent Networking & Security MCQs Asked in Zscaler OA
1. **Forward Proxy vs Reverse Proxy:**
   - What is the fundamental difference in deployment and purpose between a Forward Proxy and a Reverse Proxy?
   - *Answer:* A Forward Proxy sits in front of clients (employees) to inspect and filter outbound traffic towards the internet (hiding client identity). A Reverse Proxy sits in front of backend web servers to handle load balancing, SSL termination, and DDoS protection for inbound traffic (hiding server infrastructure).
2. **TLS 1.3 0-RTT (Zero Round Trip Time) Resumption:**
   - How does TLS 1.3 achieve 0-RTT connection resumption, and what is its security trade-off?
   - *Answer:* Clients use a Pre-Shared Key (PSK) derived from a prior session to send encrypted application data in the very first `ClientHello` message without waiting for server response. The security trade-off is vulnerability to **Replay Attacks**, which requires application-level safeguards (e.g. idempotency tokens).
3. **SNI (Server Name Indication) in HTTPS:**
   - Why is Server Name Indication (SNI) necessary during the initial TLS handshake?
   - *Answer:* SNI allows the client to specify the target hostname during the initial unencrypted handshake so that a server hosting multiple virtual domains on a single IP address can present the correct digital certificate.
