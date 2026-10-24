# Flipkart Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🛒

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **SHL** (Primary for SDE-1) / **HackerEarth** (Flipkart GRiD Hackathon)
- **Duration:** 90 minutes (3 Coding Questions)
- **Difficulty Breakdown:**
  - Question 1: Easy to Medium (Arrays, Strings, Greedy logic)
  - Question 2: Medium (Trees, Graphs, Sorting, Interval Scheduling)
  - Question 3: Hard (Complex 2D Dynamic Programming, Matrix Paths, Constructive Algorithms)
- **Scoring & Cutoff:** 
  - Partial marks are awarded based on hidden test cases cleared.
  - Solving 2 questions completely + partial test cases on the 3rd usually guarantees an interview shortlist.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Dynamic Programming:** 2D/3D state DP, 2D knapsack (ones and zeroes), frog jump, burst balloons, interval DP.
- **Graphs & BFS/DFS:** Shortest path with fuel/noise limits, component counting, topological order in supply chains.
- **Greedy & Interval Scheduling:** Order batching, warehouse delivery intervals, meeting room variants.
- **Strings & Frequency Matching:** Substring permutation queries, anagram substrings under threshold, longest string chain.
- **Monotonic Deque & Sliding Window:** Shortest subarray with sum $\ge K$, subarrays with $K$ different integers.

---

## 📝 Verified Multi-Year OA Question Bank (Past 3 Years)
*Every problem listed below is a distinct, verified question sourced from 2023, 2024, and 2025/2026 campus placement drives (IITs, NITs, BITS, DTU) and Flipkart GRiD national hackathons. Duplicates across college slots have been strictly merged.*

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Delivery Drone Path / Minimum Fuel Route (Flipkart GRiD 2024)
- **College/Drive:** Flipkart GRiD National Finals 2024
- **Problem Summary:** A drone must deliver packages between cities connected by bi-directional flight routes with fuel costs. At each city, the drone can refuel up to a tank capacity $C$. Find the minimum total fuel cost or return -1 if impossible.
- **Approach:** Modified Dijkstra's Algorithm maintaining `(current_cost, city, fuel_remaining)` state in a priority queue.
- **Complexity:** $O(E \log(V \times C))$.

#### 2. Maximum Delivery Slots (Weighted Job Scheduling)
- **College/Drive:** IIT Roorkee / IIT Kharagpur 2024
- **Problem Summary:** Given $N$ delivery requests with start time, end time, and customer value. Find the maximum total value such that no two delivery slots overlap.
- **LeetCode Equivalent:** [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)
- **Approach:** Dynamic Programming combined with Binary Search (sort jobs by end time, `dp[i] = max(dp[i-1], job.val + dp[prev_non_overlapping])`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 3. K-Consecutive Array Reconstruction (Constructive Algorithm)
- **College/Drive:** BITS Pilani 2024
- **Problem Summary:** Given integers $N$ and $K$. Rearrange elements from $1$ to $N$ such that for any two consecutive segments of size $K$, the difference between their sums is at most 1.
- **Approach:** Mathematical pattern and constructive sorting balancing alternate odd/even index placements.
- **Complexity:** $O(N)$ Time.

#### 4. Maximum String Subsets Matching Binary Constraints (2D Knapsack)
- **College/Drive:** NIT Trichy / DTU 2024
- **Problem Summary:** You are given an array of binary strings `strs` and two integers $m$ and $n$. Return the size of the largest subset of `strs` such that there are at most $m$ 0's and $n$ 1's in the subset.
- **LeetCode Equivalent:** [474. Ones and Zeroes](https://leetcode.com/problems/ones-and-zeroes/)
- **Approach:** 2D Knapsack DP: iterate strings from right to left, `dp[i][j] = max(dp[i][j], 1 + dp[i - zeros][j - ones])`.
- **Complexity:** $O(L \cdot m \cdot n)$ Time where $L$ is number of strings.

#### 5. Warehouse Order Batching / Smallest Range from K Lists
- **College/Drive:** IIIT Allahabad / NSUT 2024
- **Problem Summary:** Given $K$ sorted lists of package order timestamps from $K$ warehouse zones, find the smallest time interval $[a, b]$ that includes at least one timestamp from each of the $K$ lists.
- **LeetCode Equivalent:** [632. Smallest Range Covering Elements from K Lists](https://leetcode.com/problems/smallest-range-covering-elements-from-k-lists/)
- **Approach:** Min-Heap storing `(timestamp, list_idx, elem_idx)` with running `max_val` tracker.
- **Complexity:** $O(N \log K)$ Time.

#### 6. Jump Game VI (Sliding Window Maximum DP)
- **College/Drive:** Flipkart Campus Slot 2024
- **Problem Summary:** Given array `nums` and integer $k$. You start at index 0 and can jump at most $k$ steps forward. Maximize total score accumulated.
- **LeetCode Equivalent:** [1696. Jump Game VI](https://leetcode.com/problems/jump-game-vi/)
- **Approach:** Dynamic programming with Monotonic Decreasing Deque storing `(dp_val, index)` to query max in sliding window of size $k$ in $O(1)$.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 7. Minimum Time to Finish All Tasks (Parallel Workers Binary Search)
- **College/Drive:** Flipkart SDE-1 Hiring 2024
- **Problem Summary:** There are $N$ warehouse picking tasks with times $T_i$ and $K$ workers. Tasks cannot be split. Find minimum time for all workers to finish when tasks must be assigned in contiguous blocks.
- **LeetCode Equivalent:** [410. Split Array Largest Sum](https://leetcode.com/problems/split-array-largest-sum/)
- **Approach:** Binary Search on answer space in range $[\max(T), \sum T]$. Greedily count workers needed.
- **Complexity:** $O(N \log(\sum T))$ Time.

#### 8. Shortest Subarray with Sum at Least K (Monotonic Deque)
- **College/Drive:** Flipkart GRiD Track 2024
- **Problem Summary:** Given an integer array `nums` that may contain negative values, return the length of the shortest non-empty subarray with sum $\ge K$.
- **LeetCode Equivalent:** [862. Shortest Subarray with Sum at Least K](https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/)
- **Approach:** Prefix sum array combined with Monotonic Increasing Deque of prefix sum indices. Pop from front while `prefix[i] - prefix[deque.front()] >= K`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 9. Subarrays with K Different Integers
- **College/Drive:** Campus Placement Drive 2024
- **Problem Summary:** Given an array of integers, count the number of good subarrays that contain exactly $K$ different integers.
- **LeetCode Equivalent:** [992. Subarrays with K Different Integers](https://leetcode.com/problems/subarrays-with-k-different-integers/)
- **Approach:** Reduction: $\text{exact}(K) = \text{atMost}(K) - \text{atMost}(K - 1)$ using sliding window with frequency map.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Optimal Account Balancing (Delivery Agent Settlements)
- **College/Drive:** Flipkart Logistics Tech 2024
- **Problem Summary:** Given delivery payments between agents where agent $A$ owes agent $B$ cash, find the minimum number of transactions needed to settle all debts.
- **LeetCode Equivalent:** [465. Optimal Account Balancing](https://leetcode.com/problems/optimal-account-balancing/)
- **Approach:** Filter non-zero net balances. DFS Backtracking with branch-and-bound pruning or Bitmask DP finding maximum disjoint zero-sum subsets.
- **Complexity:** $O(2^N)$ for $N \le 14$.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Longest String Chain (Subsequence Chain DP)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Longest chain of words where each word is formed by adding one letter to previous word.
- **LeetCode Equivalent:** [1048. Longest String Chain](https://leetcode.com/problems/longest-string-chain/)
- **Complexity:** $O(N \log N + N \cdot L^2)$ Time.

#### 12. Network Signal Distortions (Shortest Path with Noise Limit)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Find shortest path from origin to destination such that accumulated noise $\le \text{Threshold}$.
- **Approach:** Dijkstra on expanded state `(node, noise_level)`.
- **Complexity:** $O(T \cdot (V + E) \log(T \cdot V))$ Time.

#### 13. Encrypted String Anagram Match (Sliding Window)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Determine if encrypted payload contains substring that is an anagram of target pattern.
- **LeetCode Equivalent:** [438. Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string/)
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

#### 14. Frog Jump (River Stones DP)
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** A frog crosses a river with stones at given units. If last jump was $k$ units, next jump must be $k-1, k,$ or $k+1$ units. Determine if frog can reach the last stone.
- **LeetCode Equivalent:** [403. Frog Jump](https://leetcode.com/problems/frog-jump/)
- **Approach:** Hash Map mapping `stone_position -> set of valid jump sizes`.
- **Complexity:** $O(N^2)$ Time, $O(N^2)$ Space.

#### 15. Burst Balloons (Interval DP)
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Burst balloons to collect maximum coins where coins for balloon $i$ are $nums[i-1] \times nums[i] \times nums[i+1]$.
- **LeetCode Equivalent:** [312. Burst Balloons](https://leetcode.com/problems/burst-balloons/)
- **Approach:** Interval DP: `dp[left][right] = max(dp[left][i-1] + nums[left-1]*nums[i]*nums[right+1] + dp[i+1][right])`.
- **Complexity:** $O(N^3)$ Time, $O(N^2)$ Space.

#### 16. Rotting Oranges / Warehouse Spoilage
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Compute minimum minutes to spoil all fresh goods on $M \times N$ warehouse grid.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 17. Course Schedule with Priority Execution
- **College/Drive:** Advanced SDE Slot 2023
- **Problem Summary:** Schedule prerequisite workflows where workflows ready at the same time must execute in order of highest priority ID first.
- **Approach:** Kahn's Algorithm for Topological Sort using Max-Heap Priority Queue.
- **Complexity:** $O(V \log V + E)$ Time.

#### 18. Number of Subsequences with Product Less Than K
- **College/Drive:** Flipkart Tech 2023
- **Problem Summary:** Given an array of positive integers, count non-empty subsequences whose product is $\le K$.
- **Approach:** Meet-in-the-middle if $N \le 30$, or dynamic programming with logarithm transformations.
- **Complexity:** $O(2^{N/2} \log(2^{N/2}))$ Time.

#### 19. Trapping Rain Water II (3D Warehouse Layout)
- **College/Drive:** Flipkart GRiD 2023
- **Problem Summary:** Calculate volume of water trapped in a 3D elevation matrix.
- **LeetCode Equivalent:** [407. Trapping Rain Water II](https://leetcode.com/problems/trapping-rain-water-ii/)
- **Approach:** Min-Heap storing boundary cells; expand lowest boundary inward.
- **Complexity:** $O(M \cdot N \log(M \cdot N))$ Time.

#### 20. Count Subarrays with Median K
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Return number of non-empty subarrays that have median equal to $K$.
- **LeetCode Equivalent:** [2448. Count Subarrays With Median K](https://leetcode.com/problems/count-subarrays-with-median-k/)
- **Approach:** Prefix sums on mapped array: $+1$ if $>K$, $-1$ if $<K$, $0$ if $==K$.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.
