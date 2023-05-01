# [ Majority Element](https://leetcode.com/problems/majority-element/)

### Understanding the problem
Given an array `nums` of size `n`, return the `majority` element.

The majority element is the element that appears more than `⌊n / 2⌋` times. You may assume that the majority element always exists in the array.

<b>Constraints:</b>
- n == nums.length
- 1 <= n <= 5 * 104
- -109 <= nums[i] <= 109

<b>Notes: </b>Could you solve the problem in linear time and in O(1) space?

<pre>
<b>Examples:</b>
<b>Input:</b> nums = [3,2,3] <b>Output:</b> 3 
<b>Input:</b> nums = [2,2,1,1,1,2,2] <b>Output:</b> 2 
</pre>

#
### Approach 1: For Loop

### Implementation
```js
function majorityElement(nums){
  let maxTimes = Math.floor(nums.length / 2);
  for(let i = 0; i < nums.length; i++){
    count = 0;
    for(let j = 0; j < nums.length; j++){
      if(nums[i] === nums[j]){
        count ++;
      }
    if(count > maxTimes){
      return nums[i];
    }
    }
  }
}
```
#
### Approach 2: Boyer–Moore Majority Vote Algorithm

The `Boyer–Moore majority vote algorithm` is an algorithm for finding the `majority` of a sequence of elements using `linear time` and `constant space`. It is named after Robert S. Boyer and J Strother Moore, who published it in 1981, and is a prototypical example of a streaming algorithm.

This solution uses a variable `majority` to keep track of the current candidate for the majority element, and a variable count to keep track of the number of times that candidate has been seen so far.

The function starts by assuming that the first element in the array is the majority element, and sets count to 1. Then, it loops through the rest of the elements in the array and updates majority and count accordingly.

If the current element is the same as the current candidate majority, then count is incremented. If the current element is different from majority and count is greater than 1, then count is decremented to "cancel out" the previous element seen.

If count reaches 0, then the current element becomes the new candidate for the majority element, and count is reset to 1.

At the end of the loop, majority should contain the majority element.

### Implementation
```js
function majorityElement(nums) {
  let majority = nums[0];
  let count = 1;
  
  for (let i = 1; i < nums.length; i++) {
    if (nums[i] === majority) {
      count++;
    } else if (count > 1) {
      count--;
    } else {
      majority = nums[i];
      count = 1;
    }
  }
  
  return majority;
}
```
