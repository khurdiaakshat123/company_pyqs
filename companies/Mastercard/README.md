# Mastercard Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💳

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 minutes
- **Structure Breakdown:**
  1. **Section 1: Core CS & Aptitude MCQs (30 mins)** – 15 to 20 MCQs covering Operating Systems, DBMS/SQL, OOPs (Java focus), Computer Networks, and Quantitative Aptitude.
  2. **Section 2: Hands-On Coding (60 mins, 2 Questions)** – LeetCode Easy to Medium difficulty.
- **Passing Cutoff:** Full test-case clearance on both coding problems + solid performance on Core CS MCQs (>75%).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Arrays & Two Pointers:** Sliding window, subarray sums, running transactions, Kadane's maximum sum, prefix products.
- **Strings & HashMaps:** Character frequency balancing, anagram verification, Luhn algorithm validation, valid parentheses.
- **SQL Queries & DBMS MCQs:** Joins, `GROUP BY`, indexing, ACID properties, transaction rollback, isolation levels.
- **Trees & Binary Search Trees:** Tree traversals, lowest common ancestor, symmetric tree, BST search.
- **Basic Dynamic Programming:** House robber, coin change, climbing stairs, maximum profit.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Credit Card Luhn Algorithm Validation
- **College/Drive:** BITS Pilani / VIT Vellore 2024–2025
- **Problem Summary:** Implement the Luhn algorithm to check whether a given 16-digit credit card number string is valid.
- **Constraints:** Number string length 13 to 19 digits.
- **Approach:** Process digits from right to left. Double every second digit; if doubled value $> 9$, subtract 9. Sum all digits and verify if total sum $\pmod{10} == 0$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Subarray Sum Equals K (Transaction Matching)
- **College/Drive:** Thapar University / Manipal 2024–2025
- **Problem Summary:** Given an array of transaction amounts and integer $K$, return total number of continuous subarrays whose sum equals $K$.
- **Constraints:** $1 \le nums.length \le 2 \times 10^4$.
- **LeetCode Equivalent:** [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- **Approach:** Prefix Sum combined with a Hash Map storing frequency of prefix sums.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 3. Symmetric Binary Tree Verification
- **College/Drive:** DTU / NSUT 2024–2025
- **Problem Summary:** Given the root of a binary tree, check whether it is a mirror of itself (symmetric around center).
- **Constraints:** Number of nodes $\le 1000$.
- **LeetCode Equivalent:** [101. Symmetric Tree](https://leetcode.com/problems/symmetric-tree/)
- **Approach:** Recursive DFS comparing left subtree with right subtree (`left->val == right->val && isMirror(left->left, right->right) && isMirror(left->right, right->left)`).
- **Complexity:** $O(N)$ Time, $O(H)$ Space.

#### 4. Minimum Steps to Make Two Strings Anagram
- **College/Drive:** SRM University / PES 2024–2025
- **Problem Summary:** Given two strings $s$ and $t$ of equal length, return the minimum character replacements in $t$ to make it an anagram of $s$.
- **Constraints:** $1 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [1347. Minimum Number of Steps to Make Two Strings Anagram](https://leetcode.com/problems/minimum-number-of-steps-to-make-two-strings-anagram/)
- **Approach:** Frequency count array of 26 letters; sum differences where `count_s > count_t`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Longest Substring Without Repeating Characters
- **College/Drive:** Mastercard Accelerate Campus 2024–2025
- **Problem Summary:** Given a transaction string, find length of longest substring without repeating characters.
- **Constraints:** $0 \le s.length \le 5 \times 10^4$.
- **LeetCode Equivalent:** [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- **Approach:** Sliding window with a hash map / 128-element array tracking the last seen index of each character.
- **Complexity:** $O(N)$ Time, $O(1)$ Auxiliary Space.

#### 6. Course Schedule (Prerequisite Cycle Detection)
- **College/Drive:** Mastercard Pune Drive 2024
- **Problem Summary:** Determine if all tasks can be finished given prerequisite relations.
- **Constraints:** $1 \le numCourses \le 2000$.
- **LeetCode Equivalent:** [207. Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Approach:** Kahn's Algorithm (BFS topological sort indegree tracking).
- **Complexity:** $O(V + E)$ Time, $O(V + E)$ Space.

#### 7. Rotting Oranges / Multi-Source Contagion
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Compute minimum time for contagion to spread across entire 2D matrix.
- **Constraints:** $1 \le M, N \le 10$.
- **LeetCode Equivalent:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- **Approach:** Multi-source BFS queuing initially rotten items at time 0.
- **Complexity:** $O(M \times N)$ Time, $O(M \times N)$ Space.

#### 8. Merge Intervals / Settlement Batches
- **College/Drive:** Mastercard Accelerate 2024
- **Problem Summary:** Merge all overlapping settlement time windows.
- **Constraints:** $1 \le intervals.length \le 10^4$.
- **LeetCode Equivalent:** [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- **Approach:** Sort by start time; merge overlapping intervals.
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

#### 9. Daily Temperatures / Transaction Spikes
- **College/Drive:** Campus Slot 2024
- **Problem Summary:** Find days to wait for a higher transaction volume day.
- **Constraints:** $1 \le temperatures.length \le 10^5$.
- **LeetCode Equivalent:** [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- **Approach:** Monotonic Decreasing Stack storing indices.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 10. Valid Parentheses
- **College/Drive:** Off-Campus Screening 2024
- **Problem Summary:** Check if string brackets are balanced.
- **Constraints:** $1 \le s.length \le 10^4$.
- **LeetCode Equivalent:** [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- **Approach:** Stack matching opening brackets with closing pairs.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Maximum Subarray Sum (Kadane's Algorithm)
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Find contiguous subarray with largest sum.
- **Constraints:** $1 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- **Approach:** Running sum: `curr = max(x, curr + x)`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. House Robber (Maximum Cash Optimization)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Maximize cash robbed without alerting security on adjacent houses.
- **Constraints:** $1 \le nums.length \le 100$.
- **LeetCode Equivalent:** [198. House Robber](https://leetcode.com/problems/house-robber/)
- **Approach:** Dynamic Programming: `dp = max(prev1, prev2 + nums[i])`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 13. Merge Two Sorted Linked Lists
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Merge two sorted linked lists into one sorted linked list in-place.
- **Constraints:** Total nodes $\le 100$.
- **LeetCode Equivalent:** [21. Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
- **Approach:** Iterative merge with dummy head pointer.
- **Complexity:** $O(M + N)$ Time, $O(1)$ Space.

#### 14. Lowest Common Ancestor in a Binary Search Tree
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Find lowest common ancestor in BST.
- **Constraints:** Nodes $\le 10^5$.
- **LeetCode Equivalent:** [235. Lowest Common Ancestor of a Binary Search Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/)
- **Approach:** Compare node value with $p$ and $q$. If both greater, go right; if both smaller, go left; else current node is LCA.
- **Complexity:** $O(H)$ Time, $O(1)$ Space.

#### 15. Coin Change (Fewest Coins)
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find minimum number of coins to make up given amount.
- **Constraints:** $1 \le amount \le 10^4$.
- **LeetCode Equivalent:** [322. Coin Change](https://leetcode.com/problems/coin-change/)
- **Approach:** 1D DP table.
- **Complexity:** $O(N \times \text{amount})$ Time, $O(\text{amount})$ Space.

#### 16. Product of Array Except Self without Division
- **College/Drive:** Campus Slot 2023
- **Problem Summary:** Compute array product except self in $O(N)$ time.
- **Constraints:** $2 \le nums.length \le 10^5$.
- **LeetCode Equivalent:** [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- **Approach:** Prefix product pass from left, running suffix product from right.
- **Complexity:** $O(N)$ Time, $O(1)$ extra Space.

#### 17. Two Sum
- **College/Drive:** Technical Screening 2023
- **Problem Summary:** Return indices of two numbers that add up to target.
- **Constraints:** $2 \le nums.length \le 10^4$.
- **LeetCode Equivalent:** [1. Two Sum](https://leetcode.com/problems/two-sum/)
- **Approach:** Hash Map lookup for `target - num`.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 18. Search in Rotated Sorted Array
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find target in rotated sorted array in $O(\log N)$ time.
- **Constraints:** $1 \le nums.length \le 5000$.
- **LeetCode Equivalent:** [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- **Approach:** Binary search checking sorted half.
- **Complexity:** $O(\log N)$ Time, $O(1)$ Space.

#### 19. Best Time to Buy and Sell Stock
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Maximize profit with a single transaction.
- **Constraints:** $1 \le prices.length \le 10^5$.
- **LeetCode Equivalent:** [121. Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 20. Container With Most Water
- **College/Drive:** Campus Placement 2023
- **Problem Summary:** Two pointers inward maximizing area between vertical lines.
- **Constraints:** $2 \le heights.length \le 10^5$.
- **LeetCode Equivalent:** [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent CS Fundamentals & SQL MCQs in Mastercard OA
1. **Database ACID Properties:**
   - What does Atomicity guarantee in banking transactions?
   - *Answer:* All operations within a transaction either execute completely or roll back entirely with no intermediate or partial updates left behind.
2. **REST API Idempotency:**
   - Which HTTP methods are inherently idempotent according to RFC specifications?
   - *Answer:* `GET`, `PUT`, `DELETE`, and `HEAD` are idempotent. `POST` is NOT idempotent.
3. **Java Strings & Garbage Collection:**
   - Why are Strings immutable in Java?
   - *Answer:* Security (network connections, file paths), caching in the String Pool, thread safety without synchronization, and hash code caching for collections.
4. **JWT (JSON Web Token) Security:**
   - Where should sensitive financial session tokens be stored on the client side to prevent XSS attacks?
   - *Answer:* In `HttpOnly` and `Secure` cookies with `SameSite=Strict`, preventing JavaScript from accessing the token via `document.cookie`.
