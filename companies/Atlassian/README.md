# Atlassian Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🔷

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  - 3 Algorithmic Coding Questions (LeetCode Medium to Hard).
  - Strict computational limits, clean code structure, and adherence to edge cases.
- **Hiring Tiers & Compensation:** Associate Software Engineer (Graduates: 45–70 LPA CTC).
- **Cutoff Benchmark:** Clearing 3/3 problems completely is typical for an interview call, though strong 2.5/3 can occasionally qualify based on speed.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Rate Limiters & Sliding Windows:** Token bucket, sliding window counters, hit counters.
- **Custom Voting & Priority Ranking:** Multi-round elections, custom comparators, tie-breakers.
- **Graph & Interval Scheduling:** Bus routes, meeting rooms, topological scheduling, multi-source BFS.
- **Concurrency & State Simulation:** Snake game, file system mockups, circular buffers.
- **Design Problems:** LRU cache, hit counters, rate limiters, nested iterators.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Rate Limiter (Token Bucket / Sliding Window Log)
- **College/Drive:** IITs / NITs On-Campus 2024
- **Problem Statement:** Design a distributed Rate Limiter that supports `allowRequest(clientId, timestamp)`. Each client is permitted at most $R$ requests within a rolling window of $W$ seconds. Requests outside the window expire.
- **Approach:** Sliding window deque per `clientId` storing timestamps. Evict timestamps $< \text{timestamp} - W$. If `deque.size() < R`, append current timestamp and return `true`, else `false`.
- **Complexity:** $O(1)$ amortized per request.

#### 2. Rank Teams by Votes (Multi-Tier Custom Sorting)
- **College/Drive:** BITS Pilani / IIIT Hyderabad 2024
- **Problem Statement:** In a special election, each voter ranks teams from highest to lowest. Rank teams according to votes received: most 1st place votes; tie-breaker: 2nd place votes, etc. If teams are still tied, sort alphabetically.
- **LeetCode Equivalent:** [1366. Rank Teams by Votes](https://leetcode.com/problems/rank-teams-by-votes/)
- **Approach:** Array of size 26 for each team tracking votes at each rank position, sorted using custom comparator.
- **Complexity:** $O(N \cdot M + 26^2 \log 26)$ Time.

#### 3. Bus Routes / Minimum Route Transfers
- **College/Drive:** Off-Campus Drive 2024
- **Problem Statement:** Given bus routes `routes[i]` where each route is a cycle of bus stops, return the least number of buses required to travel from `source` to `target`.
- **LeetCode Equivalent:** [815. Bus Routes](https://leetcode.com/problems/bus-routes/)
- **Approach:** BFS over routes instead of stops to keep graph vertices $\le 500$.
- **Complexity:** $O(\sum |routes[i]|)$.

#### 4. Design Hit Counter (Concurrency & Circular Buffer)
- **College/Drive:** DTU / NSUT 2024
- **Problem Statement:** Design a hit counter which counts the number of hits received in the past 5 minutes (300 seconds).
- **LeetCode Equivalent:** [362. Design Hit Counter](https://leetcode.com/problems/design-hit-counter/)
- **Approach:** Circular array of size 300 storing pairs of `(timestamp, hit_count)` modulo 300.
- **Complexity:** $O(1)$ Time per `hit()` and `getHits()`.

#### 5. Merge Intervals (Jira Sprint Schedule Planner)
- **College/Drive:** IIT Roorkee 2024
- **Problem Statement:** Merge overlapping time intervals representing team sprint availability windows.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort intervals by start time; iteratively merge overlapping segments.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 6. Confluence Page Link Ordering (Course Schedule II)
- **College/Drive:** IIT Delhi 2024
- **Problem Statement:** Given $N$ documentation pages and prerequisite links, determine a linear reading sequence. If cyclic dependencies exist, return empty array.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's algorithm for topological sorting using in-degrees and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 7. LRU Document Cache Implementation
- **College/Drive:** IIT Bombay 2024
- **Problem Statement:** Implement an LRU Cache for managing cached Jira issue representations with $O(1)$ `get` and `put`.
- **LeetCode Equivalent:** [146. LRU Cache](https://leetcode.com/problems/lru-cache/)
- **Approach:** Hash Map pointing to Doubly Linked List nodes with dummy head and tail.
- **Complexity:** $O(1)$ Time per operation, $O(\text{Capacity})$ Space.

#### 8. Trapping Rain Water
- **College/Drive:** IIT Kharagpur 2024
- **Problem Statement:** Compute total water trapped by elevation map bars.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers inward from boundaries.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Subarray Sum Equals K (Issue Event Log Analysis)
- **College/Drive:** BITS Pilani 2024
- **Problem Statement:** Return the total number of continuous subarrays whose sum equals target $K$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Running prefix sum with hash map frequency tracking.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Search in Rotated Sorted Array
- **College/Drive:** IIIT Hyderabad 2024
- **Problem Statement:** Find target in circularly rotated sorted array in $O(\log N)$ time.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Modified binary search checking if left or right half is monotonically sorted.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Find All Anagrams in a String
- **College/Drive:** On-Campus Slot 1 (2023)
- **Problem Statement:** Given two strings `s` and `p`, return an array of all the start indices of `p`'s anagrams in `s`.
- **LeetCode Equivalent:** [438. Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string/)
- **Approach:** Fixed-size sliding window of length $|p|$ with 26-element frequency count comparison.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 12. Design Snake Game
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Design a Snake game played on a grid of size $R \times C$. Snake moves in 4 directions, grows upon eating food, dies if it collides with boundaries or its own body.
- **LeetCode Equivalent:** [353. Design Snake Game](https://leetcode.com/problems/design-snake-game/)
- **Approach:** Deque storing `(row, col)` body segments + Hash Set of encoded coordinates for $O(1)$ self-collision checks.
- **Complexity:** $O(1)$ Time per move.

#### 13. File System Storage & Quota Allocator
- **College/Drive:** On-Campus Slot 2 (2023)
- **Problem Statement:** Implement a mock file system allocating storage blocks. Handle `createDirectory`, `createFile(path, size)`, and `getQuota(dir)` validating parent storage limits.
- **Approach:** Tree structure with Trie-like path traversal and recursive size aggregation.
- **Complexity:** $O(L)$ where $L$ is path depth.

#### 14. Minimum Operations to Transform String with Substring Reversals
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Given two binary strings $A$ and $B$, find the minimum operations to convert $A$ to $B$ where each operation allows inverting or reversing a continuous segment of 1s.
- **Approach:** Greedy transition state scanner counting contiguous mismatched blocks.
- **Complexity:** $O(N)$ Time.

#### 15. Top K Frequent Words / Jira Issue Tag Ranking
- **College/Drive:** NIT Trichy 2024
- **Problem Statement:** Return the $k$ most frequent words sorted by highest frequency and lower alphabetical order for ties.
- **LeetCode Equivalent:** [692. Top K Frequent Words](https://leetcode.com/problems/top-k-frequent-words/)
- **Approach:** Hash Map frequency count + Min-Heap of size $K$.
- **Complexity:** $O(N \log K)$ Time.

#### 16. Incident Propagation in Distributed System (Rotting Oranges)
- **College/Drive:** DTU Delhi 2023
- **Problem Statement:** Multi-source BFS to calculate minutes required for an incident alert to propagate through all connected infrastructure nodes.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time and Space.

#### 17. Word Break (Jira Title Tokenizer)
- **College/Drive:** NSUT Delhi 2023
- **Problem Statement:** Determine if text string can be segmented into a space-separated sequence of dictionary words.
- **LeetCode Equivalent:** [139. Word Break](https://leetcode.com/problems/word-break/)
- **Complexity:** $O(N^2)$ Time, $O(N)$ Space.

#### 18. Lowest Common Ancestor of a Binary Tree
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Find lowest common ancestor node of two given nodes in a binary tree.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 19. Load Balancer Slot Ordering (Reorganize String)
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Rearrange characters so that no two identical characters are adjacent.
- **LeetCode Equivalent:** [767. Reorganize String](https://leetcode.com/problems/reorganize-string/)
- **Complexity:** $O(N \log \Sigma)$ Time.

#### 20. Markdown Macro Expansion (Decode String)
- **College/Drive:** University Hiring 2023
- **Problem Statement:** Decode nested string encoding format `k[string]`.
- **LeetCode Equivalent:** [394. Decode String](https://leetcode.com/problems/decode-string/)
- **Approach:** Dual stack for counts and strings.
- **Complexity:** $O(\text{Output Length})$ Time.

---

## 🧠 Frequent Architecture & Concurrency MCQs Asked in Atlassian OA
1. **Sliding Window Log vs Token Bucket Rate Limiting:**
   - Why does the Token Bucket algorithm consume less memory than the Sliding Window Log algorithm in high-throughput systems?
   - *Answer:* The Sliding Window Log records the exact timestamp of every individual request in a list or deque (memory scales with request count). The Token Bucket stores only two numbers per client: the available token count and the timestamp of the last token refill (memory is $O(1)$ per client).
2. **Eventual Consistency in Distributed Collaborative Editing:**
   - How does Conflict-Free Replicated Data Types (CRDTs) enable conflict-free concurrent editing without a central locking server?
   - *Answer:* CRDTs structure data mutations as mathematically commutative, associative, and idempotent operations. Regardless of network packet reordering or network delays, all replicas converge to the exact same state once all operations are received.
