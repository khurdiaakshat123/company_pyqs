# Zscaler Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🔒

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  - 2 to 3 Algorithmic Coding Problems (Medium to Hard).
  - (In select campus drives) 10 to 15 Core Networking & Security MCQs (TCP/IP, Firewalls, SSL/TLS, Proxies).
- **Evaluation Criteria & Strict Warning:**
  - Zscaler operates cloud security and zero-trust exchange platforms.
  - Automated plagiarism detection is notoriously strict; code mirroring public repositories or exact LeetCode snippets results in immediate disqualification.
  - 100% test case pass on at least 2 questions is required.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Tries & IP Prefix Lookups:** Routing table rules, domain whitelist/blacklist filtering.
- **Large Log Stream Parsing & HashMaps:** Real-time proxy event deduplication.
- **Dynamic Programming & LIS:** Longest increasing subsequence variations, packet ordering.
- **Segment Trees & Range Frequency:** Querying packet surges across time intervals.

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
- **Approach:** Binary Indexed Tree (Fenwick Tree) or Segment Tree.
- **Complexity:** $O(\log N)$ per update and range query.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Network Delay Time / Security Broadcast (Dijkstra)
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Calculate time for a security revocation certificate to reach all proxy nodes in a weighted network.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Complexity:** $O(E \log V)$ Time.

#### 6. Minimum Cost to Connect All Data Centers (MST)
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Find minimum total fiber length to connect all regional proxy gateways.
- **LeetCode Equivalent:** [1584. Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)
- **Approach:** Kruskal's algorithm with Disjoint Set Union (DSU) or Prim's algorithm.
- **Complexity:** $O(E \log E)$ Time.

#### 7. Valid Parentheses with Asterisk Wildcard
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Check if security policy rule syntax with `(`, `)`, and `*` wildcard is valid.
- **LeetCode Equivalent:** [678. Valid Parenthesis String](https://leetcode.com/problems/valid-parenthesis-string/)
- **Approach:** Greedy range tracking `min_open` and `max_open`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Subarray Sum Equals K (Threat Threshold)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Find total subsegments whose threat levels sum to exact threshold $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Complexity:** $O(N)$ Time, $O(N)$ Space.
