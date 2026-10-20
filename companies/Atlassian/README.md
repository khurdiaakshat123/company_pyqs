# Atlassian Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🔷

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  - 3 Algorithmic Coding Questions (Medium to Hard).
  - Strict computational limits, clean code structure, and adherence to edge cases.
- **Hiring Tiers & Compensation:** Associate Software Engineer (Graduates: 45–70 LPA CTC).
- **Cutoff Benchmark:** Clearing 3/3 problems completely is typical for an interview call, though strong 2.5/3 can occasionally qualify based on speed.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Rate Limiters & Sliding Windows:** Token bucket, sliding window counters, hit counters.
- **Custom Voting & Priority Ranking:** Multi-round elections, custom comparators.
- **Graph & Interval Scheduling:** Bus routes, meeting rooms, topological scheduling.
- **Concurrency & State Simulation:** Snake game, file system mockups.

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

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Find All Anagrams in a String
- **College/Drive:** On-Campus Slot 1 (2023)
- **Problem Statement:** Given two strings `s` and `p`, return an array of all the start indices of `p`'s anagrams in `s`.
- **LeetCode Equivalent:** [438. Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string/)
- **Approach:** Fixed-size sliding window of length $|p|$ with 26-element frequency count comparison.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 6. Design Snake Game
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Design a Snake game played on a grid of size $R \times C$. Snake moves in 4 directions, grows upon eating food, dies if it collides with boundaries or its own body.
- **LeetCode Equivalent:** [353. Design Snake Game](https://leetcode.com/problems/design-snake-game/)
- **Approach:** Deque storing `(row, col)` body segments + Hash Set of encoded coordinates for $O(1)$ self-collision checks.
- **Complexity:** $O(1)$ Time per move.

#### 7. File System Storage & Quota Allocator
- **College/Drive:** On-Campus Slot 2 (2023)
- **Problem Statement:** Implement a mock file system allocating storage blocks. Handle `createDirectory`, `createFile(path, size)`, and `getQuota(dir)` validating parent storage limits.
- **Approach:** Tree structure with Trie-like path traversal and recursive size aggregation.
- **Complexity:** $O(L)$ where $L$ is path depth.

#### 8. Minimum Operations to Transform String with Substring Reversals
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Given two binary strings $A$ and $B$, find the minimum operations to convert $A$ to $B$ where each operation allows inverting or reversing a continuous segment of 1s.
- **Approach:** Greedy transition state scanner counting contiguous mismatched blocks.
- **Complexity:** $O(N)$ Time.
