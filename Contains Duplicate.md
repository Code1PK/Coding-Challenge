# [ Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)

### Understanding the problem
Given an integer array `nums`, return `true` if any value appears at least twice in the array, and return `false` if every element is distinct.

<b>Constraints:</b>
- 1 <= nums.length <= 105
- -109 <= nums[i] <= 109

<pre>
<b>Examples:</b>
<b>Input:</b>  nums = [1,2,3,1] <b>Output:</b> true 
<b>Input:</b> nums = [1,2,3,4] <b>Output:</b> false 
<b>Input:</b> nums = [1,1,1,3,3,4,3,2,4,2] <b>Output:</b> true 
</pre>

#
### Approach 1: Brute Force with For Loop

### Implementation
```js
function containsDuplicate(arr){
  let duplicate;
  for(let i = 0; i < arr.length; i ++){
    for(let j = 1; j < arr.length; j ++){
      if(arr[i] === arr[j]){
         duplicate = true;
        break;
      } else {
        duplicate = false;
      }
    }
    return duplicate;
  }
}
```
#
### Approach 2: For Loop

### Implementation
```js
function containsDuplicate(arr){
  let duplicate = false; 
  arr.sort((a,b) => a-b);
  let element = arr[0];
  for(let i = 1; i < arr.length; i ++){
    if ( arr[i] === element){
      duplicate = true;
    } else {
      element = arr[i];
    }
  }
  return duplicate;
}
```
