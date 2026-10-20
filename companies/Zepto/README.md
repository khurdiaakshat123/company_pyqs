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
- **Monotonic Stacks & Peak Detection:** Daily temperatures, next greater order volume.
- **Interval Scheduling & Dark Store Capacities:** Platform allocation, packing docks.
- **Dynamic Programming on Time Series:** Ticket purchase, cost minimization over days.
- **Binary Search & Arrays:** Peak elements, minimum delivery times, search partitions.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Dark Store Delivery Partner Allocation (Train Platform / Interval Classic)
- **College/Drive:** IIT Roorkee / BITS Pilani 2024
- **Problem Statement:** A 10-minute quick-commerce dark store receives $N$ delivery partners with arrival times and departure times. Find the minimum number of parking/staging bays needed so that no delivery partner has to wait outside.
- **LeetCode Equivalent:** [Minimum Platforms / Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- **Approach:** Separate arrivals and departures into two arrays, sort both, use Two Pointers to count overlapping intervals.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 2. Minimum Cost for Dark Store Shift Passes (DP)
- **College/Drive:** DTU / NSUT 2024
- **Problem Statement:** You have planned some dark-store shifts on specified days of the year. Shift passes are sold in 1-day, 7-day, and 30-day passes. Return the minimum cost needed to cover every day in the given list of days.
- **LeetCode Equivalent:** [983. Minimum Cost For Tickets](https://leetcode.com/problems/minimum-cost-for-tickets/)
- **Approach:** Dynamic programming: For each day, $dp[d] = \min(dp[d-1] + \text{cost}[0], dp[\max(0, d-7)] + \text{cost}[1], dp[\max(0, d-30)] + \text{cost}[2])$.
- **Complexity:** $O(365) = O(1)$ Time.

#### 3. Daily Order Surge Temperatures (Monotonic Stack)
- **College/Drive:** IIIT Allahabad 2024
- **Problem Statement:** Given an array of integers `orders` representing daily order volume, return an array `answer` such that `answer[i]` is the number of days you have to wait after the $i$-th day to get a higher daily order volume. If there is no future day with higher volume, keep `answer[i] == 0`.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing day indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 4. Dark Store Inventory Packing Station Peak
- **College/Drive:** VIT / Thapar 2024
- **Problem Statement:** An array of integers represents picking activity in dark-store aisles. Find any peak aisle index $i$ such that $A[i] > A[i-1]$ and $A[i] > A[i+1]$ in $O(\log N)$ time.
- **LeetCode Equivalent:** [162. Find Peak Element](https://leetcode.com/problems/find-peak-element/)
- **Approach:** Binary Search: Compare `mid` with `mid + 1`. If $A[mid] < A[mid+1]$, the peak must lie on the right; otherwise on the left.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Rabbits in Forest / Delivery Batch Estimation
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** In a quick commerce fleet, riders report the number of other riders carrying the same zone bag. Calculate the minimum possible total riders in the zone.
- **LeetCode Equivalent:** [781. Rabbits in Forest](https://leetcode.com/problems/rabbits-in-forest/)
- **Approach:** Frequency Map: For count $c$ riders answering $k$, groups of size $k + 1$ are formed: $\lceil \frac{c}{k+1} \rceil \times (k + 1)$.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 6. Sliding Window Maximum / Real-Time Order Monitor
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Find maximum order surge in every 10-minute rolling window.
- **LeetCode Equivalent:** [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- **Complexity:** $O(N)$ Time, $O(K)$ Space.

#### 7. Subarray Product Less Than K
- **College/Drive:** Off-Campus Drive 2023
- **Problem Statement:** Count continuous subsegments where product of quantities is strictly less than $K$.
- **LeetCode Equivalent:** [713. Subarray Product Less Than K](https://leetcode.com/problems/subarray-product-less-than-k/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Find maximum profit contiguous subarray.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.
