# Tech Mahindra Online Assessment (OA) Guide & Multi-Year PYQs (2023 - 2025/2026) 🏢

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Wheebox** / **AMCAT**
- **Test Duration:** 100 to 110 minutes
- **Structure Breakdown (Multi-Stage Assessment):**
  1. **Round 1: Cognitive Aptitude & English (50 mins)** – Quantitative Aptitude (15 Q), Logical Reasoning (15 Q), Verbal Ability (15 Q).
  2. **Round 2: Technical Competency & Pseudocode (25 mins)** – 20 to 25 MCQs covering C/C++, Java, Linux commands, and OOPs concepts.
  3. **Round 3: Hands-On Coding (45 mins, 2 Questions)** – Easy to Medium difficulty.
  4. **Round 4: Conversational English Test (Voice assessment, ~20 mins)** – Sentence reading, listening comprehension, story retelling.
- **Negative Marking:** None. High accuracy across Cognitive and Technical rounds is mandatory.

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **Basic Mathematics & Arrays:** Prime numbers, Armstrong, palindrome numbers, array balance, mean comparisons.
- **Strings & Character Parsing:** Vowel/consonant counts, word reversal, anagram verification, character frequency compression.
- **Two Pointers & In-Place Ops:** Move zeroes, remove duplicates, pair sums, odd-even segregation.
- **Technical MCQs (Linux & OOP):** File permissions (`chmod`), Linux processes (`ps`, `grep`, `kill`), OOP pillars, basic SQL.
- **Matrix Operations:** Matrix addition, diagonal sum, transpose, boundary element sum.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. Count Elements Greater Than Average
- **College/Drive:** Tech Mahindra SuperCoder Drive 2024 / Chandigarh University
- **Problem Summary:** Given an array of $N$ integers, calculate the arithmetic mean of all elements and return the count of elements strictly greater than the mean.
- **Approach:** First pass to find total sum and compute average `avg = sum / N`. Second pass to count all `nums[i] > avg`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 2. Odd-Even Array Segregation
- **College/Drive:** KIIT / SRM University 2024
- **Problem Summary:** Rearrange an array such that all even numbers appear before all odd numbers while preserving in-place memory constraints.
- **LeetCode Equivalent:** [905. Sort Array By Parity](https://leetcode.com/problems/sort-array-by-parity/)
- **Approach:** Two pointers: `left = 0`, `right = n-1`. Increment `left` while even, decrement `right` while odd; swap when out of place.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 3. Harshad (Niven) Number Verification
- **College/Drive:** LPU / Chitkara University 2024
- **Problem Summary:** An integer divisible by the sum of its digits is a Harshad number. Given an integer $X$, return `true` if it is a Harshad number, else `false`.
- **Approach:** Extract digits using modulo `% 10` and division `/ 10` to compute sum of digits. Verify if `X % digit_sum == 0`.
- **Complexity:** $O(\log_{10} X)$ Time, $O(1)$ Space.

#### 4. Move Zeroes to End of Array
- **College/Drive:** Tech Mahindra Off-Campus 2024
- **Problem Summary:** Given an integer array `nums`, move all `0`s to the end while maintaining the relative order of non-zero elements in-place.
- **LeetCode Equivalent:** [283. Move Zeroes](https://leetcode.com/problems/move-zeroes/)
- **Approach:** Two pointers: pointer $j$ keeps track of the position for the next non-zero element.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 5. Character Frequency Compression (Run-Length Encoding)
- **College/Drive:** Campus Placement 2024
- **Problem Summary:** Given a string containing consecutive duplicate characters (e.g., `"aaabbbcc"`), compress it into consecutive character-count pairs (`"a3b3c2"`).
- **LeetCode Equivalent:** [443. String Compression](https://leetcode.com/problems/string-compression/)
- **Approach:** Linear scan maintaining count of identical consecutive characters.
- **Complexity:** $O(N)$ Time, $O(1)$ Extra Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 6. Valid Palindrome After Cleaning
- **College/Drive:** Campus Slot 1 (2023)
- **Problem Summary:** Check if string is palindrome considering only alphanumeric characters and ignoring case.
- **LeetCode Equivalent:** [125. Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 7. Matrix Primary and Secondary Diagonal Sum
- **College/Drive:** Campus Slot 2 (2023)
- **Problem Summary:** Return sum of matrix diagonals without double counting center element for odd $N$.
- **LeetCode Equivalent:** [1572. Matrix Diagonal Sum](https://leetcode.com/problems/matrix-diagonal-sum/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 8. Check for Armstrong Number
- **College/Drive:** Off-Campus Hiring 2023
- **Problem Summary:** Determine if sum of each digit raised to power of total number of digits equals the number itself.
- **Complexity:** $O(\log_{10} N)$ Time, $O(1)$ Space.

#### 9. Valid Anagram Verification
- **College/Drive:** Campus Hiring 2023
- **Problem Summary:** Check if string $T$ is permutation of string $S$.
- **LeetCode Equivalent:** [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 10. Missing Number in Array Range [1, N]
- **College/Drive:** Campus Drive 2023
- **Problem Summary:** Find single missing integer from range $[1, N]$ in array of size $N-1$.
- **LeetCode Equivalent:** [268. Missing Number](https://leetcode.com/problems/missing-number/)
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

---

## 🧠 Frequent Linux & Technical MCQs in Tech Mahindra OA
1. **Linux File Permissions:**
   - What does `chmod 754 file.txt` mean?
   - *Answer:* Owner has Read/Write/Execute (`7 = 4+2+1`), Group has Read/Execute (`5 = 4+1`), Others have Read only (`4`).
2. **Process Management in Linux:**
   - What command is used to terminate a process with PID 1234 forcefully?
   - *Answer:* `kill -9 1234` (sends `SIGKILL`, which cannot be caught or ignored).
3. **Difference between Method Overloading and Method Overriding:**
   - *Answer:* Method Overloading is compile-time polymorphism (same method name, different parameter signature in the same class). Method Overriding is runtime polymorphism (same method name and signature in a subclass).
