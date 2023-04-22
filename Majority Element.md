# [ Single Number](https://leetcode.com/problems/single-number/)

### Understanding the problem
Given a non-empty array of integers `nums`, every element appears twice except for one. Find that single one.

You must implement a solution with a linear runtime complexity and use only constant extra space.

<b>Constraints:</b>
- 1 <= nums.length <= 3 * 104
- -3 * 104 <= nums[i] <= 3 * 104
- Each element in the array appears twice except for one element which appears only once.

<pre>
<b>Examples:</b>
<b>Input:</b> nums = [2,2,1] <b>Output:</b> 1 
<b>Input:</b> nums = [4,1,2,1,2] <b>Output:</b> 4 
<b>Input:</b> nums = [1] <b>Output:</b> 1 
</pre>

#
### Approach: Bit Manipulation
The `bitwise XOR (^)` operator returns a number or BigInt whose binary representation has a `1` in each bit position for which the corresponding bits of either but not both operands are `1`.

### Implementation
```js
function singleNumber(nums){
  let result = 0;
  for(let i = 0; i < nums.length; i++){
    result ^= nums[i];
  }
  return result;
}

```
