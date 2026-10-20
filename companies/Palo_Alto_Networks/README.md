# Palo Alto Networks Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) 🛡️

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **TalentRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Networking & Core CS MCQs (30 mins)** – 15 to 20 MCQs covering Firewalls, OSI/TCP layers, Subnetting, Operating Systems (Memory, Threads), and C++/Java fundamentals.
  2. **Section 2: Coding Assessment (60 mins, 2 Questions)** – Medium difficulty algorithmic and string/matrix manipulation challenges.
- **Evaluation Criteria:**
  - Robust code correctness, thorough handling of boundary/null inputs, and clean modular code.
  - Passing both coding questions with 100% test-case coverage is standard for an interview callback.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Packet & String Parsing:** Delimiter extraction, IP validation, firewall rule matching.
- **Matrix Operations & Grid Traversals:** Connected networks, routing matrices.
- **Sliding Window & HashMaps:** Frequency counting, threshold checks.
- **Trees & Binary Search:** Rule lookup trees, interval lookups.

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

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Merge Intervals / Security Log Consolidator
- **College/Drive:** On-Campus Slot 1 (2023)
- **Problem Statement:** Consolidate overlapping alert timestamp ranges into non-overlapping blocks.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time.

#### 6. Two Sum II - Input Array Is Sorted
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Find two port numbers that sum to target checksum in sorted array.
- **LeetCode Equivalent:** [167. Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Binary Tree Right Side View / Hierarchy Inspection
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Return node values visible from the right side of the binary tree.
- **LeetCode Equivalent:** [199. Binary Tree Right Side View](https://leetcode.com/problems/binary-tree-right-side-view/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 8. Rotated Array Binary Search
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Search for a key in a circularly shifted sorted array.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Complexity:** $O(\log N)$ Time.
