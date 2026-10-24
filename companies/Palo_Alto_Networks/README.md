# Palo Alto Networks Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) 🛡️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **TalentRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Networking & Core CS MCQs (30 mins)** – 15 to 20 MCQs covering Firewalls (Stateful vs Stateless, Deep Packet Inspection), OSI/TCP layers, Subnetting (CIDR), Operating Systems (Paging, Threading), and C++/Java fundamentals.
  2. **Section 2: Coding Assessment (60 mins, 2 Questions)** – Medium to Hard algorithmic, string parsing, and graph/network routing challenges.
- **Evaluation Criteria:**
  - Robust code correctness, thorough handling of boundary/null inputs, and clean modular code.
  - Passing both coding questions with 100% test-case coverage is standard for an interview callback.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Packet & String Parsing:** Delimiter extraction, IP validation (IPv4/IPv6), firewall rule matching, lexical decoders.
- **Trie & Prefix Routing:** Longest prefix matching (LPM) for IP route tables, bitwise tries.
- **Sliding Window & Hash Maps:** Signature detection, window substring, packet rate counters.
- **Graph BFS / Shortest Path:** Network delay time, lateral infection propagation, topological policy ordering.
- **Networking & Security MCQs:** NAT/PAT, SYN flood attacks, TLS 1.3 handshake, stateful inspection tables, subnet masks.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Validate IPv4 and IPv6 Network Addresses
- **College/Drive:** IIT Varanasi / NIT Surathkal 2024
- **Problem Statement:** Given a string `queryIP`, return `"IPv4"` if IP is a valid IPv4 address, `"IPv6"` if IP is a valid IPv6 address or `"Neither"` if IP is not a correct IP of any type.
- **LeetCode Equivalent:** [468. Validate IP Address](https://leetcode.com/problems/validate-ip-address/)
- **Approach:** String parsing: For IPv4, split by `.` into 4 tokens, ensure no leading zeroes, only digits, values in $[0, 255]$. For IPv6, split by `:` into 8 tokens, length 1–4 hexadecimal characters.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Firewall Rule Priority Packet Filter (Intervals)
- **College/Drive:** BITS Goa 2024
- **Problem Statement:** A next-generation firewall has $N$ packet filtering rules with IP port ranges $[P_{start}, P_{end}]$ and priority $W_i$. When a packet arrives on port $P$, apply the action of the highest-priority rule covering port $P$. Return the action for $Q$ queries.
- **Approach:** Interval Tree or Coordinate Compression + Segment Tree with Point Queries and Range Max updates.
- **Complexity:** $O((N + Q) \log N)$ Time.

#### 3. Longest Substring Without Repeating Characters (Token Validation)
- **College/Drive:** DTU / NSUT 2024
- **Problem Statement:** Find the length of the longest substring with unique session tokens.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with a hash map storing the latest index of each character.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 4. Connected Security Enclaves (Number of Islands)
- **College/Drive:** IIIT Bangalore 2024
- **Problem Statement:** Given a 2D grid representing physical datacenter racks where 1 represents secure connected servers and 0 represents isolated space, count the total number of independent secure enclaves.
- **LeetCode Equivalent:** [200. Number of Islands](https://leetcode.com/problems/number-of-islands/)
- **Approach:** BFS / DFS traversal modifying visited cells in-place.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 5. Longest Prefix CIDR Match (Trie-Based IP Routing)
- **College/Drive:** IIT Roorkee 2024
- **Problem Statement:** Given a routing table with $N$ CIDR prefixes (e.g. `192.168.0.0/16`, `192.168.1.0/24`) and next-hop gateways, process $Q$ destination IP queries and find the most specific matching gateway (longest prefix match).
- **LeetCode Equivalent:** Variation of [208. Implement Trie (Prefix Tree)](https://leetcode.com/problems/implement-trie-prefix-tree/)
- **Approach:** Binary Prefix Trie (depth up to 32 bits). Insert binary representation of CIDR masks; query traverse down bits $31 \dots 0$ tracking deepest matching prefix node.
- **Complexity:** $O(32)$ per query, $O(32 \cdot N)$ Space.

#### 6. Minimum Window Substring (Intrusion Detection Signature)
- **College/Drive:** BITS Pilani 2024
- **Problem Statement:** Given two strings `s` (raw packet payload) and `t` (signature character set), return the minimum window substring of `s` that contains all the characters in `t`.
- **LeetCode Equivalent:** [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- **Approach:** Sliding window with two frequency maps / arrays and a `match_count` tracker. Expand `right`, contract `left` while valid.
- **Complexity:** $O(|S| + |T|)$ Time, $O(\Sigma)$ Space.

#### 7. Network Delay Time (Firewall Routing Latency)
- **College/Drive:** IIT Kharagpur 2024
- **Problem Statement:** Given directed edges with transmission delays between $N$ firewall routers, find the time taken for a broadcast signal from router $K$ to reach all routers.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's Algorithm with Min-Priority Queue.
- **Complexity:** $O(E \log V)$ Time, $O(V + E)$ Space.

#### 8. Top K Frequent Domains / Malicious DNS Triage
- **College/Drive:** IIT Madras 2024
- **Problem Statement:** Given an array of DNS lookup strings `words` and an integer `k`, return the $k$ most frequent domains sorted by frequency from highest to lowest, breaking ties by lower alphabetical order.
- **LeetCode Equivalent:** [692. Top K Frequent Words](https://leetcode.com/problems/top-k-frequent-words/)
- **Approach:** Hash Map for frequency counting + Min-Heap of size $K$ with custom comparator (higher frequency, or lexicographically smaller).
- **Complexity:** $O(N \log K)$ Time, $O(N)$ Space.

#### 9. Subarray Sum Equals K (Flow Volume Threshold)
- **College/Drive:** NIT Trichy 2024
- **Problem Statement:** Given packet volume samples and target volume $K$, return the number of continuous windows whose traffic sum equals $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Running prefix sum with hash map frequency tracking.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Security Policy Precedence Resolution (Course Schedule II)
- **College/Drive:** IIIT Delhi 2024
- **Problem Statement:** Security policy rules must be evaluated in an order that satisfies inter-rule prerequisites. Return a valid evaluation order or empty array if cyclical dependencies exist.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Topological Sort using Kahn's algorithm (indegree tracking and BFS queue).
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Merge Intervals / Security Log Consolidator
- **College/Drive:** On-Campus Slot 1 (2023)
- **Problem Statement:** Consolidate overlapping alert timestamp ranges into non-overlapping blocks.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time.

#### 12. Two Sum II - Input Array Is Sorted
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Find two port numbers that sum to target checksum in sorted array.
- **LeetCode Equivalent:** [167. Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 13. Binary Tree Right Side View / Hierarchy Inspection
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Return node values visible from the right side of the binary tree.
- **LeetCode Equivalent:** [199. Binary Tree Right Side View](https://leetcode.com/problems/binary-tree-right-side-view/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 14. Rotated Array Binary Search
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Search for a key in a circularly shifted sorted array.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Complexity:** $O(\log N)$ Time.

#### 15. Trapping Rain Water
- **College/Drive:** NSUT Delhi 2023
- **Problem Statement:** Given an elevation profile of buffer queues, compute total trapped data volume.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers from left and right inward.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 16. Word Break / Signature Lexical Analyzer
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Given a string `s` and a dictionary of words `wordDict`, determine if `s` can be segmented into a space-separated sequence of dictionary words.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Approach:** 1D DP boolean array: `dp[i]` is true if prefix `s[0...i-1]` can be segmented.
- **Complexity:** $O(N^2)$ Time, $O(N)$ Space.

#### 17. Malware Lateral Movement Simulation (Rotting Oranges)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Statement:** Given a network grid with clean, compromised, and empty machines, find the time taken for infection to reach all connected machines.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queue.
- **Complexity:** $O(M \times N)$ Time and Space.

#### 18. LRU Session State Cache
- **College/Drive:** Campus Placement 2023
- **Problem Statement:** Implement an LRU Cache for managing active stateful firewall connections.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Hash Map combined with Doubly Linked List.
- **Complexity:** $O(1)$ Time per operation.

#### 19. Bandwidth Reorganization (Reorganize String)
- **College/Drive:** University Hiring 2023
- **Problem Statement:** Given a string `s`, rearrange the characters of `s` so that any two adjacent characters are not the same. If impossible, return `""`.
- **LeetCode Equivalent:** [767. Reorganize String](https://leetcode.com/problems/reorganize-string/)
- **Approach:** Max-Heap of character frequencies; pop two most frequent characters at a time and pair them.
- **Complexity:** $O(N \log \Sigma)$ Time.

#### 20. Encrypted Payload Unpacking (Decode String)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Decode nested string patterns like `k[encoded_string]`.
- **LeetCode Equivalent:** [394. Decode String](https://leetcode.com/problems/decode-string/)
- **Approach:** Stack storing repeat counts and string builders.
- **Complexity:** $O(\text{Output Length})$ Time and Space.

---

## 🧠 Frequent Networking & Security MCQs Asked in Palo Alto OA
1. **Stateful vs Stateless Packet Filtering:**
   - What key distinction enables a stateful firewall to prevent unsolicited inbound traffic?
   - *Answer:* A stateful firewall tracks active Layer 4 connections in a State Table (TCP sequence numbers, 5-tuple). It dynamically permits inbound packets only if they belong to an established outbound connection initiated from the trusted internal network.
2. **CIDR Subnet Mask Calculation:**
   - How many usable host IP addresses are available in a `/27` IPv4 subnet?
   - *Answer:* A `/27` subnet leaves $32 - 27 = 5$ host bits. Total IP addresses = $2^5 = 32$. Subtracting 2 for Network Address and Broadcast Address gives $32 - 2 = 30$ usable host IPs.
3. **SYN Flood Mitigation (SYN Cookies):**
   - How do SYN Cookies protect a server from connection exhaustion during a TCP SYN flood attack?
   - *Answer:* The server does not allocate memory for half-open connections in the backlog queue upon receiving a SYN packet. Instead, it encodes the connection state cryptographically into the initial sequence number (ISN) of the SYN-ACK packet and verifies it only when the client returns the ACK.
