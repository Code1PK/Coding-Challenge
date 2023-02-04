# [Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/description/)

### Understanding the problem

You are given two integer arrays `nums1` and `nums2`, sorted in non-decreasing order, and two integers `m` and `n`, representing the number of elements in `nums1` and `nums2` respectively.

Merge `nums1` and `nums2` into a single array sorted in non-decreasing order.

The final sorted array should not be returned by the function, but instead be stored inside the array `nums1`. To accommodate this, `nums1` has a length of `m + n`, where the first `m` elements denote the elements that should be merged, and the last `n` elements are set to `0` and should be ignored. `nums2` has a length of `n`.

<pre>
<b>Input:</b> nums1 = [1,2,3,0,0,0], m = 3, nums2 = [2,5,6], n = 3
<b>Output:</b> [1,2,2,3,5,6]
<b>Input:</b> nums1 = [1], m = 1, nums2 = [], n = 0
<b>Output:</b> [1]
<b>Input:</b> nums1 = [0], m = 0, nums2 = [1], n = 1
<b>Output:</b> [1]
</pre>

#
### Approach: Built-In Functions

### Implementation
```js
function mergeArray(num1,m,num2,n){
  num1.splice(m,n);
  num1.push(...num2);
  num1.sort((a,b) => a-b);
  return num1;
}
```
