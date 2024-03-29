# [Tuck in Array](https://edabit.com/challenge/7ysTEDruHz2prcJQ9)

### Understanding the problem

Create a function that takes two arrays and insert the second array in the middle of the first array.

<b>Notes:</b>
- The first array always has two elements.
- Use the spread syntax to solve this challenge.

<pre>
<b>Input:</b> tuckIn([1, 10], [2, 3, 4, 5, 6, 7, 8, 9])
<b>Output:</b> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
<b>Input:</b> tuckIn([15,150], [45, 75, 35])
<b>Output:</b> [15, 45, 75, 35, 150]
<b>Input:</b> tuckIn([[1, 2], [5, 6]], [[3, 4]])
<b>Output:</b> [[1, 2], [3, 4], [5, 6]]
</pre>

#
### Approach: Built-In Function

### Implementation
```js
function tuckIn(arr1, arr2){

  return [...arr1.slice(0,1),...arr2,...arr1.slice(1,2)];
}
```
