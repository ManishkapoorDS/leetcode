## 198. House Robber

### Problem Link 
https://leetcode.com/problems/house-robber/

### Note
This problem is a very classic `DP` problem. Main idea is to use `dp` to store previous calculation so that next one
 can directly use it. Here're two different ways:
 
**Note**: need to pay attention to edge cases: `len(nums) == 0` and `len(nums) <= 2`.
 
#### DP 1
Here the `dp[i]` is the optimal rob gain given by `nums[:i + 1]`. Here `nums[i]` may not be robbed. 
Thus for `dp[-1]` is final result.

Note: for nums slice `[a, b, c, d]` the optimal is `max(b + d, a + c, a + d)`.

#### DP 2
Different with previous logic, here the `dp[i]` is the optimal rob gain that must include `nums[i]`.
Thus final result is `max(dp[-1], dp[-2])`.