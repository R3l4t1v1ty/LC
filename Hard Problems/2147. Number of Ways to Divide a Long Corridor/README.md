## 2147. Number of Ways to Divide a Long Corridor

link: https://leetcode.com/problems/number-of-ways-to-divide-a-long-corridor/description/

### Problem:

Along a long library corridor, there is a line of seats and decorative plants. You are given a 0-indexed string corridor of length n consisting of letters 'S' and 'P' where each 'S' represents a seat and each 'P' represents a plant.

One room divider has already been installed to the left of index 0, and another to the right of index n - 1. Additional room dividers can be installed. For each position between indices i - 1 and i (1 <= i <= n - 1), at most one divider can be installed.

Divide the corridor into non-overlapping sections, where each section has exactly two seats with any number of plants. There may be multiple ways to perform the division. Two ways are different if there is a position with a room divider installed in the first way but not in the second way.

Return the number of ways to divide the corridor. Since the answer may be very large, return it modulo 109 + 7. If there is no way, return 0.

### Constraints:

- n == corridor.length
- 1 <= n <= 10^5
- corridor[i] is either 'S' or 'P'.

### Discussing Solution:

We count chairs. Every time we are at 2 chairs we count plants.
When we reach 3rd chair we multiply our solution with the plant
count. We reset chair counter to 1 and plant counter to 0.

We repeat that until the end.

If number of chairs in the end is not 2, the task is impossible
and the solution is 0. Otherwise, we return our result.


### Complexities:

- Time: O(n)
- Space: O(1)