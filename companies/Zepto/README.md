# Zepto Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) ⚡

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank** / **BarRaiser Assessment Platform**
- **Test Duration:** 60 to 90 minutes
- **Structure Breakdown:**
  - 2 to 3 Algorithmic Coding Problems (LeetCode Medium to Hard).
  - Quick commerce focus: Extreme priority on execution speed and optimal asymptotic complexity ($O(N)$ or $O(N \log N)$ expected immediately).
- **Hiring Tiers & Compensation:** SDE-1 / Fast-Track Fresher (28–36 LPA CTC).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Monotonic Stacks & Peak Detection:** Daily temperatures, next greater order volume, sliding window maximum with deques.
- **Interval Scheduling & Dark Store Capacities:** Platform allocation, packing docks, meeting rooms II.
- **Dynamic Programming on Time Series:** Ticket purchase, cost minimization over days, house robber.
- **Binary Search & Arrays:** Peak elements, minimum delivery times, search in rotated sorted arrays.
- **Graph & Grid Pathfinding:** Multi-source BFS, rotting inventory, dark store dispatch router.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Dark Store Delivery Partner Allocation (Meeting Rooms II)
- **College/Drive:** IIT Roorkee / BITS Pilani 2024–2025
- **Problem Summary:** A 10-minute quick-commerce dark store receives $N$ delivery partners with arrival times and departure times. Find the minimum number of parking/staging bays needed so that no delivery partner has to wait outside.
- **Constraints:** $1 \le N \le 10^4$.
- **LeetCode Equivalent:** [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- **Approach:** Separate arrivals and departures into two arrays, sort both, use Two Pointers to count overlapping intervals.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 2. Minimum Cost for Dark Store Shift Passes (DP)
- **College/Drive:** DTU / NSUT 2024–2025
- **Problem Summary:** You have planned some dark-store shifts on specified days of the year. Shift passes are sold in 1-day, 7-day, and 30-day passes. Return the minimum cost needed to cover every day in the given list of days.
- **Constraints:** $1 \le days.length \le 365$, $1 \le days[i] \le 365$.
- **LeetCode Equivalent:** [983. Minimum Cost For Tickets](https://leetcode.com/problems/minimum-cost-for-tickets/)
- **Approach:** Dynamic programming: For each day, $dp[d] = \min(dp[d-1] + \text{cost}[0], dp[\max(0, d-7)] + \text{cost}[1], dp[\max(0, d-30)] + \text{cost}[2])$.
- **Complexity:** $O(365) = O(1)$ Time.

#### 3. Daily Order Surge Temperatures (Monotonic Stack)
- **College/Drive:** IIIT Allahabad 2024–2025
- **Problem Summary:** Given an array of integers `orders` representing daily order volume, return an array `answer` such that `answer[i]` is the number of days you have to wait after the $i$-th day to get a higher daily order volume. If there is no future day with higher volume, keep `answer[i] == 0`.
- **Constraints:** $1 \le orders.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing day indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 4. Dark Store Inventory Packing Station Peak
- **College/Drive:** VIT / Thapar 2024–2025
- **Problem Summary:** An array of integers represents picking activity in dark-store aisles. Find any peak aisle index $i$ such that $A[i] > A[i-1]$ and $A[i] > A[i+1]$ in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 1000$.
- **LeetCode Equivalent:** [162. Find Peak Element](https://leetcode.com/problems/find-peak-element/)
- **Approach:** Binary Search: Compare `mid` with `mid + 1`. If $A[mid] < A[mid+1]$, the peak must lie on the right; otherwise on the left.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 5. Rabbits in Forest / Delivery Batch Estimation
- **College/Drive:** Campus Drive Slot 1 (2024–2025)
- **Problem Summary:** In a quick commerce fleet, riders report the number of other riders carrying the same zone bag. Calculate the minimum possible total riders in the zone.
- **Constraints:** $1 \le answers.length \le 1000$.
- **LeetCode Equivalent:** [781. Rabbits in Forest](https://leetcode.com/problems/rabbits-in-forest/)
- **Approach:** Frequency Map: For count $c$ riders answering $k$, groups of size $k + 1$ are formed: $\lceil \frac{c}{k+1} \rceil \times (k + 1)$.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 6. Sliding Window Maximum / Real-Time Order Monitor
- **College/Drive:** Campus Drive Slot 2 (2024)
- **Problem Summary:** Find maximum order surge in every 10-minute rolling window.
- **Constraints:** $1 \le nums.length \le 10^5$, $1 \le k \le nums.length$.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Approach:** Monotonic Decreasing Deque storing indices.
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 7. Subarray Product Less Than K
- **College/Drive:** Off-Campus Drive 2024
- **Problem Summary:** Count continuous subsegments where product of quantities is strictly less than $K$.
- **Constraints:** $1 \le nums.length \le 3 \times 10^4$.
- **LeetCode Equivalent:** [713. Subarray Product Less Than K](https://leetcode.com/problems/subarray-product-less-than-k/)
- **Approach:** Sliding window with two pointers: add `(right - left + 1)` per step.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Campus Hiring 2024
- **Problem Summary:** Find maximum profit contiguous subarray.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Approach:** Kadane's algorithm.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Rotting Oranges / Fresh Inventory Shelf Life
- **College/Drive:** Zepto Bangalore Screening 2024
- **Problem Summary:** Compute minimum minutes for inventory decay in 2D grid.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 10. Course Schedule II / Picking Dependency Flow
- **College/Drive:** Campus Drive 2024
- **Problem Summary:** Find order to pick item dependencies in dark store aisles.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **Approach:** Kahn's Algorithm using indegrees and BFS queue.
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Trapping Rain Water
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Elevation histogram water capacity.
- **Constraints:** $1 \le n \le 2 \times 10^4$.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two Pointers approach maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Network Delay Time / Dark Store Dispatch Router
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Calculate time for all hubs to receive dispatch order from origin.
- **Constraints:** $1 \le N \le 100$, $1 \le edges \le 6000$.
- **LeetCode Equivalent:** [743. Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- **Approach:** Dijkstra's algorithm with Min-Heap.
- **Complexity:** $O(E \log V)$ Time.

#### 13. Subarray Sum Equals K
- **College/Drive:** Off-Campus 2023
- **Problem Summary:** Count total continuous subarrays whose sum equals $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix sums with hash map frequency counter.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 14. Coin Change (Fewest Denominations)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Minimum coins needed to make change.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time.

#### 15. Merge Intervals / Delivery Time Slots
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Merge all overlapping delivery time slots.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time and merge overlaps.
- **Complexity:** $O(N \log N)$ Time.

#### 16. Product of Array Except Self without Division
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Output array where each index is product of all elements except itself.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Two-pass prefix/suffix products.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 17. Longest Substring Without Repeating Items
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Sliding window with hash map storing last seen indices.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Complexity:** $O(N)$ Time, $O(\min(N, \Sigma))$ Space.

#### 18. House Robber (1D Dynamic Programming)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Maximize order value without selecting two adjacent dark store aisles.
- **Constraints:** $1 \le nums.length \le 100$.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** DP: `dp[i] = max(dp[i-1], dp[i-2] + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 19. Search in Rotated Sorted Array
- **College/Drive:** Off-Campus 2023
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

## 💡 Cracking Zepto 10-Minute SDE Assessments
1. **Optimize Asymptotics:** Zepto tests stress-test hidden inputs with sizes up to $10^5$. Solutions with $O(N^2)$ will immediately receive TLE.
2. **Monotonic Queues and Stacks:** Understand `std::deque` and stack invariants intimately; real-time order window questions rely on them.
3. **Be Fast on Implementation:** Finishing both problems within 35–40 minutes dramatically improves callback rankings for Zepto's engineering interviews.
