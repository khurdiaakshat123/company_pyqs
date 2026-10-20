# Cisco Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🌐

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **SHL**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Computer Science & Networking MCQs** (~35 to 40 Questions, 45 mins) – Massive focus on **Computer Networks** (IP addressing, Subnetting, Routing protocols, TCP/UDP, OSI layers), **Operating Systems** (Paging, Semaphores, Multithreading), and **C++/Java OOPs**.
  2. **Section 2: Coding Assessment** (2 to 3 Coding Problems, 45 mins) – Medium to Hard difficulty.
- **Evaluation Criteria:** Passing the MCQ cutoff is mandatory. Due to high applicant volume, automated screening filters out candidates scoring $< 75\%$ on the networking/CS fundamental MCQs even if coding passes 100%.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Computer Networks MCQs | Medium | Subnet masks, CIDR notation, OSPF vs BGP, TCP 3-way handshake, ARP/RARP |
| **Very High** | Graph Algorithms | Medium - Hard | Shortest Path (Dijkstra), Minimum Spanning Tree (Prim/Kruskal), BFS network hops |
| **High** | Dynamic Programming | Medium - Hard | Grid paths with obstacles, longest common subsequence, knapsack |
| **High** | Strings & Matrix Manipulations | Medium | Substring permutation checks, 2D matrix rotations, boundary traversals |
| **Medium** | Tree Traversals | Medium | Diameter of tree, Lowest Common Ancestor (LCA), Level order |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Optimal Network Packet Router / Minimum Hop Latency
- **Problem Summary:** Given $N$ network routers connected by weighted bidirectional edges representing transmission latency. Packets must travel from router $S$ to router $D$. If each intermediate router introduces a processing delay $P_i$, calculate the minimum total latency.
- **Approach:** Modified Dijkstra's Algorithm adding vertex processing weights $P_i$ to edge weights.
- **Complexity:** $O((V + E) \log V)$ Time.

### 2. Network Redundancy / Critical Cable Identification (Bridges)
- **Problem Summary:** An IT infrastructure has $N$ servers connected by $M$ network cables. Find all critical connections (cables whose failure disconnects the network into two or more components).
- **LeetCode Equivalent:** [1192. Critical Connections in a Network](https://leetcode.com/problems/critical-connections-in-a-network/)
- **Approach:** Tarjan's Bridge-Finding Algorithm using `discovery_time` and `low` arrays.
- **Complexity:** $O(V + E)$ Time, $O(V)$ Space.

### 3. Subnetting & CIDR Calculation
- **Problem Summary:** Given an IPv4 address and CIDR prefix (e.g., `192.168.10.45/27`), calculate the network address, broadcast address, and total usable host IPs.
- **Approach:** Bitwise bitmask operations on 32-bit unsigned integer representation of the IP.
- **Complexity:** $O(1)$ Time.

### 4. Maximum Subarray Sum with Circular Array
- **Problem Summary:** Given a circular integer array `nums` of length $n$, return the maximum possible sum of a non-empty subarray of `nums`.
- **LeetCode Equivalent:** [918. Maximum Sum Circular Subarray](https://leetcode.com/problems/maximum-sum-circular-subarray/)
- **Approach:** $\max(\text{KadaneMax}, \text{TotalSum} - \text{KadaneMin})$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent Networking Questions Asked in Cisco OA
1. **CIDR Subnetting:** How many usable host IP addresses are in a `/28` subnet?
   - *Formula:* $2^{(32 - 28)} - 2 = 2^4 - 2 = 14$ usable hosts (subtracting network and broadcast addresses).
2. **TCP Windowing:** What is the purpose of the sliding window mechanism in TCP? (Flow control—ensures sender does not overwhelm receiver buffer).
3. **OSPF Protocol:** What routing algorithm does OSPF use? (Dijkstra's Link-State algorithm).
