# [ Majority Element](https://leetcode.com/problems/majority-element/)

### Understanding the problem
Given an array `nums` of size `n`, return the `majority` element.

The majority element is the element that appears more than `⌊n / 2⌋` times. You may assume that the majority element always exists in the array.

<b>Constraints:</b>
- n == nums.length
- 1 <= n <= 5 * 104
- -109 <= nums[i] <= 109

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
