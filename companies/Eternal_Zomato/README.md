# Eternal (Zomato) Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🍔

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 65 to 90 minutes
- **Structure Breakdown:**
  1. **Algorithmic Coding Section:** 3 Coding Problems (Medium to Hard difficulty, 50–65 mins).
  2. **Technical MCQs Section:** 13 to 18 MCQs (20–25 mins) covering Core CS Fundamentals (DBMS, OS, Computer Networks) and Machine Learning / Data Science basics.
- **Evaluation Criteria:**
  - Zomato (Eternal group: Zomato, Blinkit, Hyperpure, District) emphasizes deep algorithmic problem-solving and clean edge-case management.
  - Test-case evaluation is strict, with hidden performance checks testing $O(N)$ or $O(N \log N)$ thresholds.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Tree Transformations & Cuts:** Minimizing tree height, subtree cut-and-attach, tree balancing, center finding.
- **In-Place Swaps & Zero-Fixing:** Sorting non-zero elements while keeping zeros stationary, array partitioning.
- **Combinatorial String Scoring:** Character frequency powers modulo $10^9+7$, rolling hashes, sliding window substrings.
- **Grid Geometry & Delivery Routing:** Delivery order batching, Cartesian movements with restricted diagonal barriers, Dijkstra.
- **Core CS & ML MCQs:** SQL joins, normalization, gradient descent, precision vs recall, AUC-ROC curve interpretation.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Sort Non-Zero Elements Keeping Zeroes Fixed
- **College/Drive:** IIT Delhi / DTU Campus Hiring 2024–2025
- **Problem Summary:** Given an array of integers containing zeroes and positive numbers. Sort the non-zero elements in non-decreasing order while keeping all zeroes in their exact original positions.
- **Constraints:** $1 \le nums.length \le 10^5$, $0 \le nums[i] \le 10^9$.
- **Approach:** Extract all non-zero elements into a separate array, sort it, and write them back sequentially into non-zero positions of the original array.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 2. Tree Rebalancing with Subtree Detachment
- **College/Drive:** BITS Pilani / IIT Roorkee 2024–2025
- **Problem Summary:** Given a tree with $N$ vertices, you are allowed to detach at most one subtree and reattach it to any other node in the tree. Minimize the resulting tree height.
- **Constraints:** $1 \le N \le 10^5$.
- **Approach:** Tree DP to find tree center/centroid and diameter. Reattaching the disconnected subtree's center to the principal component's center yields the optimal height.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 3. Delivery Order Batching & Minimum Fleet Vehicles
- **College/Drive:** NSUT / IIIT Delhi 2024–2025
- **Problem Summary:** Given $N$ delivery orders with pick-up intervals $[start_i, end_i]$, find the minimum number of delivery riders required so that no rider handles two overlapping deliveries.
- **Constraints:** $1 \le N \le 10^4$.
- **LeetCode Equivalent:** [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- **Approach:** Min-Heap storing rider end times or Sweep Line algorithm with prefix events.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 4. Stone Placement with Adjacent Unit Difference
- **College/Drive:** IIT BHU / NIT Trichy 2024–2025
- **Problem Summary:** Given a tree of $N$ nodes, place stones on nodes such that for every edge $(u, v)$, $|stones[u] - stones[v]| = 1$, and total stones placed is minimized.
- **Constraints:** $1 \le N \le 10^5$.
- **Approach:** Check bipartiteness of tree (always bipartite for trees). Color nodes with distance parity from root. Assign parity $+1$ and $0$ accordingly.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 5. String Score by Frequency Powers Modulo $10^9 + 7$
- **College/Drive:** Zomato On-Campus Slot 2024–2025
- **Problem Summary:** Given a string $S$, compute the score of all substrings, where the score of a substring is defined as $\prod (\text{char\_val})^{\text{freq}} \pmod{10^9 + 7}$.
- **Constraints:** $1 \le |S| \le 10^5$.
- **Approach:** Sliding window / Contribution method with modular exponentiation.
- **Complexity:** $O(N)$ Time, $O(\Sigma)$ Space.

#### 6. Minimum Path Cost on Delivery Grid with Roadblocks
- **College/Drive:** Campus Slot 1 (2024)
- **Problem Summary:** Minimum delivery travel cost from restaurant $(0,0)$ to customer $(M-1, N-1)$ with dynamic roadblock tolls.
- **Constraints:** $1 \le M, N \le 200$.
- **LeetCode Equivalent:** [64. Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/)
- **Approach:** Grid Dynamic Programming: `dp[i][j] = grid[i][j] + min(dp[i-1][j], dp[i][j-1])`.
- **Complexity:** $O(M \times N)$ Time, $O(N)$ Space.

#### 7. Lowest Common Ancestor in Binary Tree
- **College/Drive:** Campus Slot 2 (2024)
- **Problem Summary:** Find lowest common ancestor in binary tree.
- **Constraints:** Nodes $\le 10^5$.
- **LeetCode Equivalent:** [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- **Approach:** Post-order DFS returning non-null branch.
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 8. Longest Consecutive Sequence in Order Stream
- **College/Drive:** Off-Campus Hiring 2024
- **Problem Summary:** Length of longest sequence of consecutive integers in unsorted order IDs.
- **Constraints:** $0 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [128. Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/)
- **Approach:** Hash Set lookup; count streak only when `val - 1` is absent.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 9. Valid Parenthesis String with Wildcards
- **College/Drive:** Campus Hiring 2024
- **Problem Summary:** Validate parentheses string containing `'*'` wildcard characters.
- **Constraints:** $1 \le s.length \le 100$.
- **LeetCode Equivalent:** [678. Valid Parenthesis String](https://leetcode.com/problems/valid-parenthesis-string/)
- **Approach:** Range of open parentheses `[low, high]` tracking.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 10. Subarray Maximum Difference with Window Size K
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Find maximum difference between largest and smallest element in any window of size $K$.
- **Constraints:** $1 \le k \le n \le 10^5$.
- **Approach:** Two Monotonic Deques (one min, one max) moving across the array.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Rotting Oranges / Delivery Kitchen Spoilage
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Minimum minutes to spread spoilage across entire grid.
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

#### 14. Course Schedule II (Order Flow Staging)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Given task dependencies, find execution order.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm using indegrees and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 15. Daily Temperatures / Demand Spikes
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Find days to wait for a higher demand day.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 16. Coin Change (Fewest Coins)
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Minimum coins needed to make change.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 17. Merge Intervals
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Merge all overlapping delivery time slots.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time and merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 18. Product of Array Except Self without Division
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 19. Longest Substring Without Repeating Dishes
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Sliding window with hash map storing last seen indices.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

#### 20. House Robber (1D Dynamic Programming)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Maximize order value without selecting two adjacent restaurants.
- **Constraints:** $1 \le nums.length \le 100$.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** DP: `dp[i] = max(dp[i-1], dp[i-2] + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent CS Fundamentals & ML MCQs in Zomato OA
1. **Precision vs Recall in Fraud Detection:**
   - Why is Recall favored over Precision in transaction fraud detection?
   - *Answer:* Because the cost of missing a fraudulent transaction (false negative) is far higher than the minor inconvenience of investigating a legitimate transaction flagged as suspicious (false positive).
2. **Database Sharding vs Partitioning:**
   - What is horizontal sharding?
   - *Answer:* Splitting rows of a table across multiple independent physical database instances based on a shard key (e.g. `hash(user_id) % num_shards`) to distribute read/write load.
3. **Loss Functions in Machine Learning (Cross-Entropy vs MSE):**
   - Why is Cross-Entropy loss preferred over Mean Squared Error (MSE) for binary classification?
   - *Answer:* Cross-Entropy penalizes confident incorrect predictions exponentially and avoids vanishing gradients when paired with a sigmoid activation, providing faster gradient descent convergence.
