# Cohesity Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💾

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **CodeSignal** / **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  - 2 to 3 Algorithmic Coding Problems (LeetCode Medium to Hard).
  - Heavy focus on data storage, cache management, and multi-node synchronization algorithms.
- **Evaluation Criteria:**
  - Cohesity specializes in AI-powered data security and enterprise backup management (45+ LPA CTC).
  - Clean code, thread safety awareness, and robust algorithmic complexity are heavily weighted.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Binary Search on Answer Space:** Minimum days to make bouquets, storage allocation.
- **Cache Eviction & Design:** LRU Cache, LFU Cache, Time-based key-value stores.
- **Sliding Window & Monotonic Deques:** Window extrema over backup streams.
- **Graph BFS / Grid Search:** Shortest path in binary matrix, infection spreads.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Minimum Days to Backup Files (Bouquets Binary Search Classic)
- **College/Drive:** IIT Roorkee / IIT Kharagpur 2024
- **Problem Statement:** You have $N$ files that need to be backed up on day `bloomDay[i]`. A snapshot requires $K$ adjacent files that are ready on the same day. You need to take $M$ total snapshots. Return the minimum number of days you need to wait to be able to take $M$ snapshots. If impossible, return -1.
- **LeetCode Equivalent:** [1482. Minimum Number of Days to Make m Bouquets](https://leetcode.com/problems/minimum-number-of-days-to-make-m-bouquets/)
- **Approach:** Binary Search on days in range $[\min, \max]$. Greedy verification counting contiguous blocks of size $K$.
- **Complexity:** $O(N \log(\max - \min))$ Time.

#### 2. LFU (Least Frequently Used) Cache Implementation
- **College/Drive:** BITS Pilani / IIIT Hyderabad 2024
- **Problem Statement:** Design and implement a data structure for a Least Frequently Used (LFU) cache with `get(key)` and `put(key, value)` running in $O(1)$ average time complexity.
- **LeetCode Equivalent:** [460. LFU Cache](https://leetcode.com/problems/lfu-cache/)
- **Approach:** Two Hash Maps: `key_table` mapping `key -> (value, freq, iterator)` and `freq_table` mapping `freq -> DoublyLinkedList<key>`. Maintain `min_freq` integer.
- **Complexity:** $O(1)$ Time per operation, $O(\text{Capacity})$ Space.

#### 3. Word Ladder / Incremental Data Block Transformation
- **College/Drive:** NIT Surathkal / DTU 2024
- **Problem Statement:** Given two file checksum strings `beginWord` and `endWord`, and a dictionary `wordList`, return the number of words in the shortest transformation sequence from `beginWord` to `endWord`.
- **LeetCode Equivalent:** [127. Word Ladder](https://leetcode.com/problems/word-ladder/)
- **Approach:** Bidirectional BFS or BFS with wildcard Hash Map.
- **Complexity:** $O(M^2 \times N)$ Time where $M$ is word length.

#### 4. Time-Based Key-Value Store (Snapshot Versioning)
- **College/Drive:** NSUT / IIIT Delhi 2024
- **Problem Statement:** Design a time-based key-value data structure that can store multiple values for the same key at different time stamps and retrieve the key's value at a certain timestamp.
- **LeetCode Equivalent:** [981. Time Based Key-Value Store](https://leetcode.com/problems/time-based-key-value-store/)
- **Approach:** Hash Map mapping `key -> vector<pair<timestamp, value>>`. Use `std::upper_bound` for $O(\log K)$ lookups.
- **Complexity:** $O(1)$ `set`, $O(\log K)$ `get`.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Shortest Path in Binary Matrix (Storage Grid)
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** Find shortest path in 8-directional binary grid from $(0, 0)$ to $(N-1, N-1)$.
- **LeetCode Equivalent:** [1091. Shortest Path in Binary Matrix](https://leetcode.com/problems/shortest-path-in-binary-matrix/)
- **Complexity:** $O(N^2)$ Time.

#### 6. House Robber III (Tree Independent Node Sum)
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Maximum node sum in binary tree with no two directly connected nodes picked.
- **LeetCode Equivalent:** [337. House Robber III](https://leetcode.com/problems/house-robber-iii/)
- **Complexity:** $O(N)$ Time.

#### 7. Sliding Window Maximum (I/O Stream)
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Maximum write burst in every sliding window of size $K$.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Complexity:** $O(N)$ Time.

#### 8. Merge Intervals (Backup Window De-duplication)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Merge overlapping backup schedule intervals.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Complexity:** $O(N \log N)$ Time.
