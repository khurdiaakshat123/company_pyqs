# Tech Mahindra Online Assessment (OA) Guide & PYQs (2023 - 2025/2026) 🏢

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Wheebox** / **AMCAT**
- **Test Duration:** 100 to 110 minutes
- **Structure Breakdown (Multi-Stage Assessment):**
  1. **Round 1: Cognitive Aptitude & English (50 mins)** – Quantitative Aptitude, Logical Reasoning, Verbal Ability.
  2. **Round 2: Technical Competency & Pseudocode (25 mins)** – 20 to 25 MCQs covering C/C++, Java, Linux commands, and OOPs concepts.
  3. **Round 3: Hands-On Coding (45 mins, 2 Questions)** – Easy to Medium difficulty.
  4. **Round 4: Conversational English Test (Voice assessment, ~20 mins)** – Sentence reading, listening comprehension, story retelling.
- **Negative Marking:** None. High accuracy across Cognitive and Technical rounds is mandatory.

---

## 🎯 Exam Pattern & Question Topics (Last 3 Years Analysis)

| Frequency | Topic | Typical Difficulty | Key Concepts Tested |
|---|---|---|---|
| **Very High** | Basic Mathematics & Arrays | Easy | Prime numbers, Armstrong, palindrome numbers, array balance |
| **Very High** | Strings & Character Parsing | Easy | Vowel/consonant counts, word reversal, anagram verification |
| **High** | Two Pointers & In-Place Ops | Easy | Move zeroes, remove duplicates, pair sums |
| **High** | Technical MCQs (Linux & OOP) | Easy - Medium | File permissions (`chmod`), Linux processes (`ps`, `grep`), OOP pillars |
| **Medium** | Matrix Basics | Easy - Medium | Matrix addition, diagonal sum, transpose |

---

## 📝 Recent Real OA Questions Asked (2023, 2024, 2025)

### 1. Count Elements Greater Than Average
- **Problem Summary:** Given an array of integers, calculate the arithmetic mean of all elements and return the count of elements strictly greater than the mean.
- **Approach:** First pass to find sum and mean; second pass to count elements $> \text{mean}$.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 2. Odd-Even Array Segregation
- **Problem Summary:** Rearrange an array such that all even numbers appear before all odd numbers while preserving relative order (or in-place without order preservation).
- **Approach:** Two pointers from left and right.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 3. Palindrome String Validation
- **Problem Summary:** Given a string, verify whether it is a palindrome ignoring special characters and case.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

### 4. Harshad Number / Niven Number Verification
- **Problem Summary:** An integer divisible by the sum of its digits is a Harshad number. Given an integer $X$, return `true` if it is a Harshad number, else `false`.
- **Complexity:** $O(\log_{10} X)$ Time, $O(1)$ Space.
