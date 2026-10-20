# Rotting Oranges (Amazon PYQ)

- **Company:** Amazon
- **Difficulty:** Medium
- **Tags:** Breadth-First Search (BFS), Matrix
- **LeetCode Reference:** [994. Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)

---

## 📌 Problem Statement
You are given an `m x n` grid where each cell can have one of three values:
- `0` representing an empty cell,
- `1` representing a fresh orange, or
- `2` representing a rotten orange.

Every minute, any fresh orange that is 4-directionally adjacent to a rotten orange becomes rotten.

Return the minimum number of minutes that must elapse until no cell has a fresh orange. If this is impossible, return `-1`.

---

## 💡 Optimal Approach: Multi-Source BFS
Since all initially rotten oranges rot their adjacent fresh neighbors concurrently, this is a classic **Multi-Source BFS**:
1. Scan the grid to count all fresh oranges and enqueue coordinates of all initially rotten oranges (`grid[r][c] == 2`).
2. If `fresh_count == 0`, return `0` immediately.
3. Traverse level-by-level (minute-by-minute) using a queue:
   - For each rotten orange, explore its 4 neighbors (Up, Down, Left, Right).
   - If an adjacent cell is a fresh orange, mark it rotten (`grid[nr][nc] = 2`), decrement `fresh_count`, and push `(nr, nc)` to the queue.
4. After BFS finishes, if `fresh_count > 0`, return `-1` (unreachable oranges). Otherwise, return `minutes_elapsed`.

### Complexity
- **Time Complexity:** $O(M \times N)$ since each cell is visited at most once.
- **Space Complexity:** $O(M \times N)$ in the worst case for the BFS queue.

---

## 💻 Implementation (C++)

```cpp
#include <vector>
#include <queue>

using namespace std;

class Solution {
public:
    int orangesRotting(vector<vector<int>>& grid) {
        int m = grid.size();
        int n = grid[0].size();
        
        queue<pair<int, int>> q;
        int fresh = 0;
        
        for (int r = 0; r < m; ++r) {
            for (int c = 0; c < n; ++c) {
                if (grid[r][c] == 2) {
                    q.push({r, c});
                } else if (grid[r][c] == 1) {
                    fresh++;
                }
            }
        }
        
        if (fresh == 0) return 0;
        
        int minutes = 0;
        int dirs[4][2] = {{-1, 0}, {1, 0}, {0, -1}, {0, 1}};
        
        while (!q.empty() && fresh > 0) {
            int size = q.size();
            for (int i = 0; i < size; ++i) {
                auto [r, c] = q.front();
                q.pop();
                
                for (auto& d : dirs) {
                    int nr = r + d[0];
                    int nc = c + d[1];
                    
                    if (nr >= 0 && nr < m && nc >= 0 && nc < n && grid[nr][nc] == 1) {
                        grid[nr][nc] = 2;
                        fresh--;
                        q.push({nr, nc});
                    }
                }
            }
            minutes++;
        }
        
        return fresh == 0 ? minutes : -1;
    }
};
```
