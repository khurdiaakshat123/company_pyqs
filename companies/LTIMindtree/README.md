# LTIMindtree Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 💼

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Mercer Mettl** / **TalentNext** / **POD Assessment Platform**
- **Test Duration:** 90 to 120 minutes
- **Structure Breakdown (Multi-Stage Assessment):**
  1. **Cognitive Aptitude Section (40 mins):** Quantitative Aptitude (Time & Work, Speed-Distance, Percentages, Ratios), Logical Reasoning (Coding-Decoding, Seating Arrangements), Verbal English (Reading comprehension, Error spotting).
  2. **Technical & Pseudocode Section (35 mins):** 20 to 25 MCQs on Pseudocode output tracing, Data Structures (Stacks, Queues, Binary Trees), Database SQL queries, and Operating Systems.
  3. **Hands-On Coding Assessment (45 mins, 2 Questions):** Easy to Medium difficulty.
  4. **Spoken English / Communication Assessment (~20 mins):** Automated voice testing (reading sentences aloud, listening comprehension, retelling stories).
- **Negative Marking:** None. Speed and accuracy in the aptitude and pseudocode sections determine shortlisting into higher compensation bands (e.g. Elevate / Turbo profiles).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Pseudocode Output Prediction:** Bitwise operations, recursive function tracing, loop step counter, pointer arithmetic.
- **Basic Math & Number Theory:** Prime factorization, Fibonacci, Armstrong numbers, GCD/LCM, factorial trailing zeroes.
- **Strings & Palindromes:** Character counting, vowel removal, anagram detection, string reversal, longest common prefix.
- **Arrays & Two Pointers:** Move zeroes, find second maximum, pair sum target, negative element segregation.
- **Database SQL MCQs:** Joins, `GROUP BY`, `COUNT(*)`, primary key vs unique constraints.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Second Most Frequent Character in String
- **College/Drive:** LTIMindtree Elevate Drive 2024 / SRM University
- **Problem Summary:** Given a string $s$, find the second most frequently occurring character in it. If no such character exists, return `NULL` or `-1`.
- **Approach:** 256-element frequency array; sort frequencies or maintain two running maximums `first_max` and `second_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Move All Negative Numbers to One Side In-Place
- **College/Drive:** Amity University / KIIT 2024
- **Problem Summary:** Given an array of integers containing both positive and negative values, shift all negative numbers to the left side and positive numbers to the right side of the array in-place.
- **Approach:** Two pointers (`left = 0`, `right = n-1`). Partition array similar to quicksort partition.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. Armstrong Number Verification
- **College/Drive:** LPU / Chandigarh University 2024
- **Problem Summary:** An $n$-digit number is an Armstrong number if the sum of its digits raised to the $n$-th power equals the number itself. Verify if a given number $X$ is an Armstrong number.
- **Approach:** Count total digits $d = \lfloor \log_{10} X \rfloor + 1$. Sum $digit^d$ for all digits and compare against original number.
- **Complexity:** $O(\log_{10} X)$ Time, $O(1)$ Space.

#### 4. Matrix Boundary Element Sum
- **College/Drive:** Chitkara / Poornima University 2024
- **Problem Summary:** Given an $M \times N$ matrix, calculate the sum of all elements situated along the outer boundary of the matrix.
- **Approach:** Iterate row 0, row $M-1$, column 0, column $N-1$, ensuring corners are not double-counted.
- **Complexity:** $O(M + N)$ Time, $O(1)$ Space.

#### 5. Find the Missing Number in Range [1, N]
- **College/Drive:** Campus Placement Drive 2024
- **Problem Summary:** Given an array of size $N-1$ with numbers in range $[1, N]$, find the missing number.
- **LeetCode Equivalent:** [268. Missing Number](https://leetcode.com/problems/missing-number/)
- **Approach:** Sum formula $\frac{N(N+1)}{2} - \sum \text{nums}$ or XOR sum.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Reverse Words in a Given String
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Reverse words in a string without reversing individual characters.
- **LeetCode Equivalent:** [151. Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/)
- **Complexity:** $O(N)$ Time, $O(1)$ Auxiliary Space.

#### 7. Count Pairs with Given Sum (Two Sum Variation)
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Count pairs of elements in array that add up to target $K$.
- **LeetCode Equivalent:** [1. Two Sum](https://leetcode.com/problems/two-sum/)
- **Approach:** Hash Map frequency counter: add `freq[target - nums[i]]` to count.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 8. Longest Common Prefix
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Find longest common prefix string among array of strings.
- **LeetCode Equivalent:** [14. Longest Common Prefix](https://leetcode.com/problems/longest-common-prefix/)
- **Complexity:** $O(S)$ Time where $S$ is sum of all characters.

#### 9. Check if Linked List Has a Cycle
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Detect cycle in singly linked list.
- **LeetCode Equivalent:** [141. Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/)
- **Approach:** Floyd’s Cycle Detection (Tortoise and Hare).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 10. Valid Anagram String Verification
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Check if string $T$ is permutation of string $S$.
- **LeetCode Equivalent:** [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent Pseudocode Snippet in LTIMindtree OA
```text
Integer p, q, r
Set p = 5, q = 3, r = 8
if ((p + q) < (r - p))
    p = p + 2
else
    r = r + q
End if
Print p + q + r
```
*Tracing:* `p + q = 8`, `r - p = 3`. Since `8 < 3` is false, the `else` branch executes: `r = 8 + 3 = 11`. Output is `5 + 3 + 11 = 19`.
