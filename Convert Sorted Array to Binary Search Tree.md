# [ Convert Sorted Array to Binary Search Tree](https://leetcode.com/problems/convert-sorted-array-to-binary-search-tree/)

### Understanding the problem

Given an integer array `nums` where the elements are sorted in `ascending` order, convert it to a 
height-balanced `binary search tree`.

<b>Constraints:</b>

- 1 <= nums.length <= 104
- -104 <= nums[i] <= 104
- nums is sorted in a strictly `increasing` order.

<pre>
<b>Examples:</b>
<b>Input:</b> nums = [-10,-3,0,5,9] <b>Output:</b> [0,-3,9,-10,null,5], [0,-10,5,null,-3,null,9]
<b>Input:</b> nums = [1,3] <b>Output:</b> [3,1], [1,null,3]
</pre>

#
### Approach: 


### Implementation
```js
function TreeNode(val) {
   this.val = val;
   this.left = null;
   this.right = null
}

function sortedArrayToBST(nums) {
    if (!nums.length) return null;

    const mid = Math.floor(nums.length / 2);
    const root = new TreeNode(nums[mid]);

    // Call the function recursively on each subtree
    root.left = sortedArrayToBST(nums.slice(0, mid));
    root.right = sortedArrayToBST(nums.slice(mid + 1));

    return root;
};
```
