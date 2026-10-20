# TCS, Infosys, Wipro & Cognizant Interview Questions & PYQs 💼

## 🎯 Hiring Process Overview
Mass recruitment & differential hiring drives (e.g., TCS Ninja/Digital/Prime, Infosys SP/DSE, Wipro Turbo):
1. **Round 1 - Cognitive & Aptitude Assessment:**
   - Numerical Ability (Percentages, Ratios, Speed-Time-Distance, Work-Time)
   - Verbal Ability (Reading Comprehension, Sentence Correction, Vocabulary)
   - Reasoning Ability (Blood relations, Syllogisms, Coding-Decoding)
2. **Round 2 - Technical Assessment / Hands-on Coding:**
   - 2 to 3 coding questions (ranging from basic loops/arrays to intermediate DP/Graphs for high packages)
3. **Round 3 - Technical & HR Interview:**
   - Fundamentals of C/C++/Java/Python
   - SQL queries and database basics
   - Final year academic project explanation

---

## 📝 Frequently Asked Coding Questions

| Problem | Difficulty | Key Concept |
|---|---|---|
| Find Second Largest Element in Array | Easy | Array Traversal without Sorting |
| Check for Palindrome (Number & String) | Easy | Two Pointers / Modulo Arithmetic |
| Matrix Rotation (90 degrees clockwise) | Medium | Transpose + Reverse Rows |
| Longest Palindromic Substring | Medium | Two Pointers (Expand from Center) |
| Balanced Parentheses | Easy | Stack |
| Remove Duplicates from Sorted Array | Easy | Two Pointers in-place |
| Armstrong Number & Fibonacci Series | Easy | Math / Recursion |
| Majority Element (Moore's Voting Algorithm) | Easy | Boyer-Moore Algorithm |

---

## 🧠 Frequently Asked SQL & DBMS Questions
1. Write a query to find the 2nd highest salary from an Employee table:
   ```sql
   SELECT MAX(salary) 
   FROM Employee 
   WHERE salary < (SELECT MAX(salary) FROM Employee);
   ```
2. What is the difference between `DELETE`, `TRUNCATE`, and `DROP`?
3. Explain Inner Join vs Left Join with examples.
4. What are ACID properties in a database?
