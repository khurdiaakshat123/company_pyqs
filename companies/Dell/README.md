# Dell Technologies Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 💻

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **HackerEarth** / **AMCAT**
- **Test Duration:** 90 to 105 minutes
- **Structure Breakdown:**
  1. **Cognitive Aptitude Section (30 mins):** Quantitative Ability (15 Q), Logical Reasoning (15 Q), Verbal Ability (15 Q).
  2. **Technical MCQs Section (30 mins):** 20 to 25 MCQs covering Operating Systems (Storage systems, RAID levels, Paging), Computer Networks, C++/Java OOPs, and Cloud Infrastructure basics.
  3. **Hands-On Coding Assessment (45 mins, 2 Questions):** LeetCode Easy to Medium difficulty.
- **Passing Cutoff:** Balanced score across Technical MCQs and Coding is required for interview shortlisting.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Operating Systems & Storage MCQs | Medium | RAID levels (0, 1, 5, 10), Disk scheduling (SCAN, C-SCAN), Inodes, File systems |
| **Very High** | Arrays & Two Pointers | Easy - Medium | Subarray sums, in-place element removals, pair sum target |
| **High** | Strings & Character Counting | Easy | Anagram verification, palindrome construction, substring counts |
| **High** | Linked Lists | Easy - Medium | Middle element, detect cycle, reverse linked list |
| **Medium** | Basic Dynamic Programming | Medium | Climbing stairs, house robber, minimum path sum |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. RAID Disk Redundancy & Storage Efficiency
- **Problem Summary:** Given a total of $N$ physical storage disks each of capacity $C$ GB, calculate the usable storage capacity and fault tolerance (number of disks that can fail without data loss) under RAID 0, RAID 1, RAID 5, and RAID 6 configurations.
- **Formulas:**
  - RAID 0: Capacity = $N \times C$, Fault Tolerance = 0 disks.
  - RAID 1: Capacity = $C$, Fault Tolerance = $N - 1$ disks.
  - RAID 5: Capacity = $(N - 1) \times C$, Fault Tolerance = 1 disk (requires $N \ge 3$).
  - RAID 6: Capacity = $(N - 2) \times C$, Fault Tolerance = 2 disks (requires $N \ge 4$).

### 2. Reverse Linked List in Place
- **Problem Summary:** Given the head of a singly linked list, reverse the list, and return the reversed list.
- **LeetCode Equivalent:** [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
- **Approach:** Three pointers (`prev`, `curr`, `next_node`).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 3. Maximum Subarray Sum (Kadane's Algorithm)
- **Problem Summary:** Given an integer array `nums`, find the subarray with the largest sum, and return its sum.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 4. Disk Track Seeking Order (SCAN / Elevator Simulation)
- **Problem Summary:** Given a series of cylinder requests on a disk and the initial head position, simulate the SCAN disk scheduling algorithm to compute the total track head movements.
- **Complexity:** $O(N \log N)$ Time.
