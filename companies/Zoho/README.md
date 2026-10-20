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
- **String Parsing & Pattern Expansions:** `a1b10` $\to$ `abbbbbbbbbb`.
- **Matrix Traversals & In-Place Manipulations:** Spiral matrix, diagonal reversals, boundary sums.
- **Array Leaders & Trapping Rain Water:** Linear scan, two pointers.
- **Console Application Architecture:** Object-oriented modeling of real-world stateful reservation and booking systems.

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

---

### 2023 - 2024 Campus & Off-Campus Drives

#### 5. Find Leaders in Array
- **College/Drive:** Campus Drive Slot 1 (2023)
- **Problem Statement:** An element is a leader if it is greater than or equal to all the elements to its right side. Find all leaders in an array.
- **Approach:** Scan from right to left tracking `max_so_far`.
- **Complexity:** $O(N)$ Time, $O(1)$ Space.

#### 6. Snake Pattern Matrix Printing
- **College/Drive:** Campus Drive Slot 2 (2023)
- **Problem Statement:** Print $N \times N$ matrix elements in snake pattern: left-to-right for even rows, right-to-left for odd rows.
- **Complexity:** $O(N^2)$ Time, $O(1)$ Space.

#### 7. Round 3 Application: Taxi Booking System
- **College/Drive:** Campus Hiring 2023
- **Problem Statement:** Design a taxi booking system with 4 points (A, B, C, D, E, F) 15 km apart. 4 taxis stationed at point A initially. Booking charges: Rs. 100 for first 5 km, Rs. 10 per km thereafter. Assign free taxi at nearest point with lowest total earnings.
- **Complexity:** Simulation using Taxi objects and priority sorting.

#### 8. Remove Palindromic Words from Sentence
- **College/Drive:** Off-Campus 2023
- **Problem Statement:** Given a sentence, remove all words that are palindromes.
- **Complexity:** $O(N)$ Time.
