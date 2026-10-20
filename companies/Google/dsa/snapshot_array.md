# Snapshot Array (Google PYQ)

- **Company:** Google
- **Difficulty:** Medium
- **Tags:** Array, Binary Search, Design, Hash Table
- **LeetCode Reference:** [1146. Snapshot Array](https://leetcode.com/problems/snapshot-array/)

---

## 📌 Problem Statement
Implement a `SnapshotArray` that supports the following interface:
- `SnapshotArray(int length)`: initializes an array-like data structure with the given length. Initially, each element equals 0.
- `void set(index, val)`: sets the element at the given index to be equal to `val`.
- `int snap()`: takes a snapshot of the array and returns the `snap_id`: the total number of times we called `snap()` minus 1.
- `int get(index, snap_id)`: returns the value at the given `index`, at the time we took the snapshot with the given `snap_id`.

---

## 💡 Optimal Approach: Binary Search on History List
Storing a full copy of the array on every `snap()` call causes $O(N \times S)$ space complexity, leading to Memory Limit Exceeded (MLE).

Instead:
- Maintain a list of `(snap_id, value)` pairs for each index.
- In `set(index, val)`: Append or update `(current_snap_id, val)` for `index`.
- In `snap()`: Increment `current_snap_id` by 1 and return previous value.
- In `get(index, snap_id)`: Use **Binary Search (upper_bound / bisect)** on the history of `index` to find the value at or immediately prior to `snap_id`.

### Complexity
- **Time Complexity:**
  - `set`: $O(1)$ amortized
  - `snap`: $O(1)$
  - `get`: $O(\log K)$ where $K$ is the number of updates at that index
- **Space Complexity:** $O(\text{Total updates})$

---

## 💻 Implementation (Python 3)

```python
import bisect

class SnapshotArray:

    def __init__(self, length: int):
        self.snap_id = 0
        # For each index, store a list of [snap_id, val] pairs
        self.history = [[[-1, 0]] for _ in range(length)]

    def set(self, index: int, val: int) -> None:
        if self.history[index][-1][0] == self.snap_id:
            self.history[index][-1][1] = val
        else:
            self.history[index].append([self.snap_id, val])

    def snap(self) -> int:
        self.snap_id += 1
        return self.snap_id - 1

    def get(self, index: int, snap_id: int) -> int:
        records = self.history[index]
        # Binary search for rightmost record with record[0] <= snap_id
        idx = bisect.bisect_right(records, [snap_id, float('inf')]) - 1
        return records[idx][1]
```
