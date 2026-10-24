# Cisco Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🌐

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **SHL**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Computer Science & Networking MCQs** (~35 to 40 Questions, 45 mins) – Massive focus on **Computer Networks** (IP addressing, Subnetting, Routing protocols, TCP/UDP, OSI layers), **Operating Systems** (Paging, Semaphores, Multithreading), and **C++/Java OOPs**.
  2. **Section 2: Coding Assessment** (2 to 3 Coding Problems, 45 mins) – Medium to Hard difficulty.
- **Evaluation Criteria:** Passing the MCQ cutoff is mandatory. Due to high applicant volume, automated screening filters out candidates scoring $< 75\%$ on the networking/CS fundamental MCQs even if coding passes 100%.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Computer Networks MCQs:** Subnet masks, CIDR notation, OSPF vs BGP, TCP 3-way handshake, ARP/RARP, sliding window flow control.
- **Graph Algorithms:** Shortest Path (Dijkstra), Minimum Spanning Tree (Prim/Kruskal), BFS network hops, Tarjan's bridges.
- **Dynamic Programming:** Grid paths with obstacles, longest common subsequence, knapsack, circular subarray sum.
- **Strings & Matrix Manipulations:** Substring permutation checks, 2D matrix rotations, boundary traversals.
- **Bitwise Operations:** Subnet parsing, IP conversion, bit reversals.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Optimal Network Packet Router / Minimum Hop Latency (Dijkstra)
- **College/Drive:** IIT Roorkee / BITS Pilani 2024–2025
- **Problem Summary:** Given $N$ network routers connected by weighted bidirectional edges representing transmission latency. Packets must travel from router $S$ to router $D$. If each intermediate router introduces a processing delay $P_i$, calculate the minimum total latency.
- **Constraints:** $1 \le N \le 10^4$, $1 \le edges \le 5 \times 10^4$.
- **Approach:** Modified Dijkstra's Algorithm adding vertex processing weights $P_i$ to edge weights.
- **Complexity:** $O((V + E) \log V)$ Time.

#### 2. Network Redundancy / Critical Cable Identification (Tarjan's Bridges)
- **College/Drive:** NIT Trichy / NIT Surathkal 2024–2025
- **Problem Summary:** An IT infrastructure has $N$ servers connected by $M$ network cables. Find all critical connections (cables whose failure disconnects the network into two or more components).
- **Constraints:** $1 \le N \le 10^5$, $M \le 10^5$.
- **LeetCode Equivalent:** [1192. Critical Connections in a Network](https://leetcode.com/problems/critical-connections-in-a-network/)
- **Approach:** Tarjan's Bridge-Finding Algorithm using `discovery_time` and `low` arrays.
- **Complexity:** $O(V + E)$ Time, $O(V)$ Space.

#### 3. Subnetting & CIDR Calculation in Software
- **College/Drive:** DTU / NSUT 2024–2025
- **Problem Summary:** Given an IPv4 address and CIDR prefix (e.g., `192.168.10.45/27`), calculate the network address, broadcast address, and total usable host IPs.
- **Constraints:** Valid IPv4 strings.
- **Approach:** Bitwise bitmask operations on 32-bit unsigned integer representation of the IP. Mask is `~((1 << (32 - prefix)) - 1)`.
- **Complexity:** $O(1)$ Time.

#### 4. Maximum Subarray Sum with Circular Array (Ring Buffer)
- **College/Drive:** IIIT Hyderabad 2024–2025
- **Problem Summary:** Given a circular integer array `nums` of length $n$, return the maximum possible sum of a non-empty subarray of `nums`.
- **Constraints:** $1 \le n \le 3 \times 10^4$.
- **LeetCode Equivalent:** [918. Maximum Sum Circular Subarray](https://leetcode.com/problems/maximum-sum-circular-subarray/)
- **Approach:** $\max(\text{KadaneMax}, \text{TotalSum} - \text{KadaneMin})$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Network Delay Time (Cisco Signature)
- **College/Drive:** Campus Placement 2024–2025
- **Problem Summary:** Time taken for all $N$ nodes to receive signal from source $K$.
- **Constraints:** $1 \le N \le 100$, $1 \le edges \le 6000$.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's algorithm with Min-Heap.
- **Complexity:** $O(E \log V)$ Time.

#### 6. Course Schedule (Topological Sort)
- **College/Drive:** Campus Slot 1 (2024)
- **Problem Summary:** Detect if routing dependency graph has cycles.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Kahn's Algorithm using indegrees and BFS queue.
- **Complexity:** $O(V + E)$ Time.

#### 7. Rotate Image (Matrix 90 Degree Rotation)
- **College/Drive:** Campus Slot 2 (2024)
- **Problem Summary:** In-place clockwise 90 degree matrix rotation.
- **Constraints:** $1 \le N \le 100$.
- **LeetCode Equivalent:** [48. Rotate Image](https://leetcode.com/problems/rotate-image/)
- **Approach:** Transpose matrix along main diagonal, then reverse each row horizontally.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Space.

#### 8. Longest Common Subsequence
- **College/Drive:** Off-Campus 2024
- **Problem Summary:** Longest common packet payload sequence.
- **Constraints:** $1 \le |text1|, |text2| \le 1000$.
- **LeetCode Equivalent:** [1143. Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/)
- **Approach:** 2D DP table: `dp[i][j] = dp[i-1][j-1] + 1` if match, else `max(dp[i-1][j], dp[i][j-1])`.
- **Complexity:** $O(M \times N)$ Time.

#### 9. Minimum Spanning Tree (Kruskal's / Prim's)
- **College/Drive:** Campus Hiring 2024
- **Problem Summary:** Connect all network switches with minimal fiber cost.
- **Constraints:** $1 \le N \le 1000$.
- **LeetCode Equivalent:** [1584. Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)
- **Approach:** Kruskal's algorithm with Disjoint Set Union (DSU).
- **Complexity:** $O(E \log V)$ Time.

#### 10. Valid Palindrome II (At Most One Deletion)
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Palindrome check with 1 character removal tolerance.
- **Constraints:** $1 \le s.length \le 10^5$.
- **LeetCode Equivalent:** [680. Valid Palindrome II](https://leetcode.com/problems/valid-palindrome-ii/)
- **Approach:** Two pointers checking mismatch; test skipping left or right character.
- **Complexity:** $O(N)$ Time.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Rotting Oranges / Packet Contagion
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Minimum minutes to spread infection across entire 2D matrix.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 12. Trapping Rain Water
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 13. Subarray Sum Equals K
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Count total continuous subarrays whose sum equals $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency counter.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 14. Daily Temperatures / Congestion Metrics
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Find days to wait for a higher value.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 15. Coin Change (Fewest Coins)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Minimum coins needed to make change.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 16. Merge Intervals (Network Maintenance Windows)
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Merge all overlapping maintenance intervals.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time; merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 17. Product of Array Except Self without Division
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 18. Longest Substring Without Repeating Characters
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Sliding window with hash map storing last seen indices.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

#### 19. Search in Rotated Sorted Array
- **College/Drive:** Technical Assessment 2023
- **Problem Summary:** Find target in rotated sorted array in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 5000$.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking sorted half.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 20. Container With Most Water
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Two pointers inward maximizing area between vertical lines.
- **Constraints:** $2 \le heights.length \le 10^5$.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent Networking Questions Asked in Cisco OA
1. **CIDR Subnetting:** How many usable host IP addresses are in a `/28` subnet?
   - *Formula:* $2^{(32 - 28)} - 2 = 2^4 - 2 = 14$ usable hosts (subtracting network and broadcast addresses).
2. **TCP Windowing:** What is the purpose of the sliding window mechanism in TCP?
   - *Answer:* Flow control—ensures sender does not overwhelm receiver's buffer capacity.
3. **OSPF Protocol:** What routing algorithm does OSPF use?
   - *Answer:* Dijkstra's Link-State algorithm (Shortest Path First).
4. **ARP vs RARP:**
   - What is the difference between ARP and RARP?
   - *Answer:* ARP (Address Resolution Protocol) resolves a known IP address to a physical MAC address. RARP (Reverse ARP) resolves a known physical MAC address to an assigned IP address.
