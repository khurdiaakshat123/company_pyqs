# Oracle Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🔴

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerRank**
- **Test Duration:** 90 to 105 minutes
- **Structure Breakdown:**
  - **Part 1: Coding Assessment** (1 to 2 Coding Questions, 45–60 mins) – Focuses on Arrays, Prefix Sums, Intervals, and Binary Search.
  - **Part 2: Core CS & Aptitude MCQs** (15 to 35 Questions, 30–45 mins) – OS, DBMS, Computer Networks, OOPs (Java focus), and Quantitative Aptitude.
- **Scoring & Cutoff:** Oracle strictly evaluates the MCQ section alongside coding. Candidates passing all coding test cases but scoring poorly on OS/DBMS MCQs are frequently screened out.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Core CS MCQs (DBMS / OS) | Medium | SQL joins, normalization (3NF/BCNF), ACID, Semaphores, Paging, Page Faults |
| **Very High** | Arrays & Prefix Sums | Easy - Medium | Partition index, balanced even/odd sums, subarray equals K |
| **High** | Binary Search on Answer | Medium | Aggressive cows variation, allocation/capacity limits |
| **High** | Java / OOP Fundamentals | Medium | Immutability, String pool, Garbage collection, Exception hierarchy |
| **Medium** | Matrix Traversals & BFS | Medium | Grid reachability, boundary island tracking |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Fair Indices / Even-Odd Balance Index
- **Problem Summary:** Given an array $A$ of size $N$, find the number of indices $i$ such that removing $A[i]$ makes the sum of elements at even positions equal to the sum of elements at odd positions.
- **Approach:** Maintain `even_prefix`, `odd_prefix`, `even_suffix`, `odd_suffix`. When removing index $i$, suffix elements flip their parity. Check in $O(1)$ per index.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

### 2. Minimum Reduction Cost (Greedy Array Reduction)
- **Problem Summary:** Repeatedly pick the two minimum elements in an array, remove them, and insert their sum back into the array until one element remains. Calculate the minimum total cost of all operations.
- **LeetCode Equivalent:** [1167. Minimum Cost to Connect Sticks](https://leetcode.com/problems/minimum-cost-to-connect-sticks/)
- **Approach:** Min-Heap (`priority_queue`).
- **Complexity:** $O(N \log N)$ Time, $O(N)$ Space.

### 3. Server Allocation / Capacity Optimization
- **Problem Summary:** Allocate $M$ requests across $N$ servers such that the maximum load on any single server is minimized.
- **Approach:** Binary Search on maximum capacity (`low = max(requests)`, `high = sum(requests)`).
- **Complexity:** $O(N \log(\text{sum}))$.

### 4. Matrix Path with Turn Restrictions
- **Problem Summary:** Given an $M \times N$ grid, find the number of paths from $(0, 0)$ to $(M-1, N-1)$ where moving right or down is permitted, but consecutive turns in the same direction are bounded by $K$.
- **Approach:** 3D Dynamic Programming: `dp[r][c][consecutive_turns]`.
- **Complexity:** $O(M \times N \times K)$ Time.

---

## 🧠 Frequent Core CS MCQs in Oracle OA
1. **SQL 2nd Highest Salary Query:**
   ```sql
   SELECT MAX(salary) FROM Employee 
   WHERE salary < (SELECT MAX(salary) FROM Employee);
   ```
2. **Java String Pool:**
   ```java
   String s1 = "Oracle";
   String s2 = new String("Oracle");
   System.out.println(s1 == s2); // false (Heap vs Pool)
   System.out.println(s1.equals(s2)); // true (Content equality)
   ```
3. **Database Normalization:** A table with composite candidate key $(A, B)$ has functional dependency $A \to C$. Which normal form is violated? (Violates 2NF due to partial dependency).
