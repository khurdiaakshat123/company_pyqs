# LTIMindtree Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 💼

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Mercer Mettl** / **TalentNext** / **POD Assessment Platform**
- **Test Duration:** 90 to 120 minutes
- **Structure Breakdown (Multi-Stage Assessment):**
  1. **Cognitive Aptitude Section (40 mins):** Quantitative Aptitude (Time & Work, Speed-Distance, Percentages, Ratios), Logical Reasoning (Coding-Decoding, Seating Arrangements), Verbal English (Reading comprehension, Error spotting).
  2. **Technical & Pseudocode Section (35 mins):** 20 to 25 MCQs on Pseudocode output tracing, Data Structures (Stacks, Queues, Binary Trees), Database SQL queries, and Operating Systems.
  3. **Hands-On Coding Assessment (45 mins, 1 to 2 Questions):** Easy to Medium difficulty.
  4. **Spoken English / Communication Assessment (~20 mins):** Automated voice testing (reading sentences aloud, listening comprehension, retelling stories).
- **Negative Marking:** None. Speed and accuracy in the aptitude and pseudocode sections determine shortlisting into higher compensation bands.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Pseudocode Output Prediction | Easy - Medium | Bitwise operations, recursive function tracing, loop step counter |
| **Very High** | Basic Math & Number Theory | Easy | Prime factorization, Fibonacci, Armstrong numbers, GCD/LCM |
| **High** | Strings & Palindromes | Easy | Character counting, vowel removal, anagram detection, string reversal |
| **High** | Arrays & Two Pointers | Easy | Move zeroes, find second maximum, pair sum target |
| **Medium** | Database SQL MCQs | Easy - Medium | Joins, `GROUP BY`, `COUNT(*)`, primary key vs unique constraints |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Second Most Frequent Character in String
- **Problem Summary:** Given a string $s$, find the second most frequently occurring character in it. If no such character exists, return `NULL` or `-1`.
- **Approach:** 256-element frequency array; sort frequencies or maintain two running maximums `first_max` and `second_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 2. Move All Negative Numbers to One Side
- **Problem Summary:** Given an array of integers containing both positive and negative values, shift all negative numbers to the left side and positive numbers to the right side of the array in-place.
- **Approach:** Two pointers (`left = 0`, `right = n-1`).
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 3. Armstrong Number Verification
- **Problem Summary:** An $n$-digit number is an Armstrong number if the sum of its digits raised to the $n$-th power equals the number itself. Verify if a given number $X$ is an Armstrong number.
- **Complexity:** $O(\log_{10} X)$ Time, $O(1)$ Space.

### 4. Matrix Boundary Element Sum
- **Problem Summary:** Given an $M \times N$ matrix, calculate the sum of all elements situated along the outer boundary of the matrix.
- **Complexity:** $O(M + N)$ Time, $O(1)$ Space.

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
*Tracing:* `p + q = 8`, `r - p = 3`. Since `8 < 3` is false, `r = 8 + 3 = 11`. Output is `5 + 3 + 11 = 19`.
