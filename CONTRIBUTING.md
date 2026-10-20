# Contributing to Company PYQs 🤝

Thank you for contributing! Your input helps students and working professionals prepare effectively for technical interviews.

---

## 📌 How to Contribute

1. **Fork the Repository**:
   Click on the **Fork** button at the top right of this page.

2. **Clone your Fork**:
   ```bash
   git clone https://github.com/<your-username>/company_pyqs.git
   cd company_pyqs
   ```

3. **Create a Feature Branch**:
   ```bash
   git checkout -b add/google-lru-cache-pyq
   ```

4. **Add Your Changes**:
   - Place company-specific questions in `companies/<Company_Name>/`.
   - Place general topic or core CS questions in `topics/<topic_name>/`.
   - Follow the template below for consistency.

5. **Commit and Push**:
   ```bash
   git add .
   git commit -m "feat(google): add LRU cache problem with optimal solution"
   git push origin add/google-lru-cache-pyq
   ```

6. **Submit a Pull Request (PR)**:
   Open a PR against the `main` branch with a clear description of what you've added.

---

## 📝 Problem Contribution Template

When adding a question, please follow this format:

```markdown
# [Problem Name]

- **Company:** [e.g. Google]
- **Role & Level:** [e.g. Software Engineer - L3/L4 / Campus Placement]
- **Date/Year:** [e.g. 2024 / 2025]
- **Difficulty:** [Easy / Medium / Hard]
- **Tags:** [Arrays, HashMaps, Sliding Window]

## Problem Statement
[Detailed description of the problem along with constraints]

## Example
**Input:**
```
nums = [2, 7, 11, 15], target = 9
```
**Output:**
```
[0, 1]
```

## Constraints
- 2 <= nums.length <= 10^5
- -10^9 <= nums[i] <= 10^9

## Approach 1: Brute Force
- **Intuition:** ...
- **Time Complexity:** O(N^2)
- **Space Complexity:** O(1)

## Approach 2: Optimal
- **Intuition:** ...
- **Time Complexity:** O(N)
- **Space Complexity:** O(N)

### Code (C++ / Python / Java)
```cpp
// Your solution code here
```
```

---

## 🛡️ Code Guidelines
- Write clean, commented, and readable code.
- Ensure time and space complexities are mentioned.
- Do not paste copyrighted proprietary internal question text directly if restricted by NDA; summarize the algorithmic problem conceptually.
