# Zoho Corporation Online Assessment Guide & Multi-Year PYQs (2023 - 2025/2026) 🏢

## 📌 OA Overview & Test Logistics
- **Assessment Platform:** **Zoho Internal Testing Portal** / Campus Coding Portal
- **Hiring Architecture (Multi-Round Process):**
  1. **Round 1: General Aptitude & C-Output Tracing (60–90 mins)**
     - 15 Quantitative / Logical Aptitude Questions.
     - 15 C/C++ Code Snippets (Predict output: Pointers, increment operators, storage classes, macros).
  2. **Round 2: Basic Programming Round (90 mins, 5 Questions)**
     - String patterns, pattern expansion, recursion, matrix manipulations.
  3. **Round 3: Advanced Programming / Mini-Application Development (120–180 mins)**
     - Building a fully functional console application (e.g., Railway Reservation System, Taxi Booking System, Snake Game, Splitwise, Dungeon Crawl).
- **Evaluation Criteria:**
  - Zoho strictly evaluates raw logic and algorithmic implementation without reliance on built-in language helpers (often strictly tested in C, C++, or Java).

---

## 🎯 Question Pattern & Topics (Last 3 Years Analysis)
- **String Parsing & Pattern Expansions:** `a1b10` $\to$ `abbbbbbbbbb`, palindromic substring, character rotations.
- **Matrix Traversals & In-Place Manipulations:** Spiral matrix, diagonal traversals, snake patterns, boundary sums.
- **Array Leaders & Sorting:** Linear scan, two pointers, wave form sorting, merge without extra space.
- **Console Application Architecture:** Object-oriented modeling of real-world stateful reservation and booking systems.
- **C-Output Tracing:** Pointer arithmetic (`*p++`, `++*p`), pre/post increment, macro side-effects, memory leaks.

---

## 📝 Multi-Year College OA Question Bank (Past 3 Years)

### 2024 - 2025 / 2026 Campus & Off-Campus Drives

#### 1. String Pattern Expansion / Run-Length Decoder (Zoho Classic)
- **College/Drive:** Anna University / PSG Tech / Top TN Colleges 2024
- **Problem Statement:** Given an encoded string like `a1b10c2`, expand it such that each character is printed consecutively as many times as the integer following it.
- **Example:**
  - Input: `a1b10c2`
  - Output: `abbbbbbbbbbcc`
  - Input: `a2b3c4`
  - Output: `aabbbcccc`
- **Approach:** Parse character, then parse all following consecutive numeric digits into an integer using `num = num * 10 + (s[i] - '0')`. Repeat character print.
- **Complexity:** $O(\text{Output Length})$ Time, $O(1)$ Extra Space.

#### 2. Spiral Matrix Traversal in Clockwise Order
- **College/Drive:** Campus Drive 2024
- **Problem Statement:** Given an $M \times N$ matrix, return all elements of the matrix in spiral order.
- **LeetCode Equivalent:** [54. Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
- **Approach:** Maintain 4 boundary pointers: `top = 0`, `bottom = m - 1`, `left = 0`, `right = n - 1`. Traverse left $\to$ right, top $\to$ bottom, right $\to$ left, bottom $\to$ top, shrinking boundaries.
- **Complexity:** $O(M \times N)$ Time, $O(1)$ Extra Space.

#### 3. Trapping Rain Water (Two Pointers)
- **College/Drive:** Off-Campus Drive 2024
- **Problem Statement:** Given $n$ non-negative integers representing elevation map, compute trapped rainwater.
- **LeetCode Equivalent:** [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- **Approach:** Two pointers from ends maintaining `left_max` and `right_max`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 4. Round 3 Application: Railway Ticket Reservation System
- **College/Drive:** SDE Drive 2024
- **Problem Statement:** Build a console application supporting:
  - 63 Confirmed berths (Lower, Middle, Upper).
  - 18 RAC (Reservation Against Cancellation) berths.
  - 10 Waiting List (WL) tickets.
  - Operations: `BookTicket(name, age, gender, berth_pref)`, `CancelTicket(ticket_id)`, `PrintBookedTickets()`, `PrintAvailableTickets()`. Handle automatic promotion from RAC to Confirmed and WL to RAC upon cancellation.
- **Approach:** Class-based design using Queues for Waiting List and Lists for confirmed passengers.

#### 5. Diagonal Traverse of a Matrix (Zigzag Order)
- **College/Drive:** SASTRA / SSN College 2024
- **Problem Statement:** Given an $M \times N$ matrix `mat`, return an array of all the elements of the array in a diagonal order.
- **LeetCode Equivalent:** [498. Diagonal Traverse](https://leetcode.com/problems/diagonal-traverse/)
- **Approach:** Track sum $S = r + c$. Even sums move up-right, odd sums move down-left, with boundary overflow clamping.
- **Complexity:** $O(M \times N)$ Time, $O(1)$ Space.

#### 6. Longest Palindromic Substring (Expand Around Center)
- **College/Drive:** Anna University 2024
- **Problem Statement:** Given a string `s`, return the longest palindromic substring in `s` without using built-in string reverse helpers.
- **LeetCode Equivalent:** [5. Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/)
- **Approach:** Expand around each index $i$ for odd palindromes and $(i, i+1)$ for even palindromes.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Space.

#### 7. Word Search in 2D Character Grid (Boggle)
- **College/Drive:** PSG College of Technology 2024
- **Problem Statement:** Given an $M \times N$ grid of characters `board` and a string `word`, return `true` if `word` exists in the grid.
- **LeetCode Equivalent:** [79. Word Search](https://leetcode.com/problems/word-search/)
- **Approach:** Backtracking DFS with temporary in-place character masking (`board[r][c] = '#'`).
- **Complexity:** $O(M \times N \times 3^L)$ Time where $L$ is word length.

#### 8. Sort Array in Wave Form (Alternate High-Low)
- **College/Drive:** VIT Vellore 2024
- **Problem Statement:** Given an unsorted array of integers, sort the array into a wave-like array: `arr[0] >= arr[1] <= arr[2] >= arr[3] <= arr[4]...`
- **Approach:** Single-pass scan: for even indices $i$, ensure `arr[i] >= arr[i-1]` and `arr[i] >= arr[i+1]` by swapping when violated.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 9. Round 3 Application: Splitwise / Expense Sharing System
- **College/Drive:** Zoho Advanced Coding Round 2024
- **Problem Statement:** Design a console application to track expenses between friends:
  - Add users.
  - Add expense with splits: `EQUAL`, `EXACT`, or `PERCENT`.
  - Show balances for a user or all balances (`UserA owes UserB: Rs. 250`).
- **Approach:** OOP modeling with `User`, `Expense`, and `Split` subclasses, using a 2D balance map `map<int, map<int, double>>`.

#### 10. Search Target in 2D Matrix
- **College/Drive:** SRM University 2024
- **Problem Statement:** Integers in each row are sorted from left to right. First integer of each row is greater than last integer of previous row. Search for target.
- **LeetCode Equivalent:** [74. Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/)
- **Approach:** Binary search on virtual 1D array index: `r = mid / cols`, `c = mid % cols`.
- **Complexity:** $O(\log(M \times N))$ Time, $O(1)$ Space.

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 11. Find Leaders in Array
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** An element is a leader if it is greater than or equal to all the elements to its right side. Find all leaders in an array.
- **Approach:** Scan from right to left tracking `max_so_far`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 12. Snake Pattern Matrix Printing
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Print $N \times N$ matrix elements in snake pattern: left-to-right for even rows, right-to-left for odd rows.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Space.

#### 13. Round 3 Application: Taxi Booking System
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Design a taxi booking system with 4 points (A, B, C, D, E, F) 15 km apart. 4 taxis stationed at point A initially. Booking charges: Rs. 100 for first 5 km, Rs. 10 per km thereafter. Assign free taxi at nearest point with lowest total earnings.
- **Complexity:** Simulation using Taxi objects and priority sorting.

#### 14. Remove Palindromic Words from Sentence
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Given a sentence, remove all words that are palindromes.
- **Complexity:** $O(N)$ Time.

#### 15. Valid Sudoku Validator
- **College/Drive:** Zoho On-Campus 2023
- **Problem Statement:** Determine if a $9 \times 9$ Sudoku board is valid according to rules (no duplicate digits in any row, column, or $3 \times 3$ sub-box).
- **LeetCode Equivalent:** [36. Valid Sudoku](https://leetcode.com/problems/valid-sudoku/)
- **Approach:** 3 boolean / bitmask matrices tracking seen numbers for rows, columns, and boxes.
- **Complexity:** $O(1)$ Time, $O(1)$ Space.

#### 16. Round 3 Application: Dungeon Crawl (Gold & Monster Grid)
- **College/Drive:** Advanced Round 2023
- **Problem Statement:** Adventurer and monster start at coordinates $(A_r, A_c)$ and $(M_r, M_c)$. Gold is placed at $(G_r, G_c)$. Adventurer and monster move 1 step per turn. Adventurer wins if reaching gold in fewer steps than the monster; else eaten. Output path taken.
- **Approach:** BFS calculating Manhattan distances and coordinate steps.

#### 17. Merge Two Sorted Arrays Without Extra Space
- **College/Drive:** Campus Drive 2023
- **Problem Statement:** Merge `nums2` into `nums1` as one sorted array in-place.
- **LeetCode Equivalent:** [88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)
- **Approach:** Three pointers filling from the back (`k = m + n - 1`).
- **Complexity:** $O(M + N)$ Time, $O(1)$ Space.

#### 18. Next Greater Element Using Monotonic Stack
- **College/Drive:** University Drive 2023
- **Problem Statement:** Find the first greater element to the right for each element in an array. If none, return -1.
- **LeetCode Equivalent:** [496. Next Greater Element I](https://leetcode.com/problems/next-greater-element-i/)
- **Approach:** Monotonic Decreasing Stack storing elements/indices scanned from right to left.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 19. Evaluate Reverse Polish Notation (Postfix Expression)
- **College/Drive:** Campus Placement 2023
- **Problem Statement:** Evaluate the value of an arithmetic expression in Reverse Polish Notation.
- **LeetCode Equivalent:** [150. Evaluate Reverse Polish Notation](https://leetcode.com/problems/evaluate-reverse-polish-notation/)
- **Approach:** Stack storing operands. On encountering an operator, pop two operands, evaluate, and push result.
- **Complexity:** $O(N)$ Time, $O(N)$ Space.

#### 20. Check if String is Rotation of Another
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Given strings $s_1$ and $s_2$, determine if $s_2$ is a rotation of $s_1$ using only one call to `isSubstring`.
- **Approach:** Check if lengths match and if $s_2$ is a substring of $s_1 + s_1$.
- **Complexity:** $O(N)$ Time.

---

## 🧠 Frequent C-Output Tracing Snippets Asked in Zoho Round 1
```c
// Snippet 1: Pointer increment precedence
int arr[] = {10, 20, 30};
int *ptr = arr;
*ptr++;
printf("%d %d\n", *ptr, arr[0]); 
// Output: 20 10 (ptr is incremented to point to arr[1])

// Snippet 2: Macro expansion side effect
#define SQUARE(x) x * x
int a = 5;
int res = SQUARE(a + 1); // Expands to: 5 + 1 * 5 + 1 = 11
printf("%d\n", res); // Output: 11 (Not 36)
```
