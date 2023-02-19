# [Find the Largest Numbers in a Group of Arrays](https://edabit.com/challenge/h7LTMAFeNz79rXB2Y)

### Understanding the problem

Create a function that takes an `array of arrays` with numbers. Return a new (single) `array` with the `largest numbers` of each.

<b>Notes:</b> Watch out for `negative integers (numbers)`.

<pre>
<b>Examples:</b>
<b>Input:</b> findLargestNums([[4, 2, 7, 1], [20, 70, 40, 90], [1, 2, 0]]) <b>Output:</b> [7, 90, 2]
<b>Input:</b> findLargestNums([[-34, -54, -74], [-32, -2, -65], [-54, 7, -43]]) <b>Output:</b> [-34, -2, 7]
<b>Input:</b> findLargestNums([[0.4321, 0.7634, 0.652], [1.324, 9.32, 2.5423, 6.4314], [9, 3, 6, 3]]) <b>Output:</b> [0.7634, 9.32, 9]
</pre>

#
### Approach 1: For Loop 
This function initializes an empty array `result`, and then loops through each sub-array in the input array `arr` using a for loop. For each sub-array, it finds the largest number using the `Math.max` method and the `spread syntax`. It then pushes the largest number onto the `result` array using the `push` method. Finally, the function returns the `result` array.

### Implementation
```js
function findLargestNums(arr) {
  let result = [];
  for (let i = 0; i < arr.length; i++){
    result.push(Math.max(...arr[i]));
  }
  return result;
}
```
#
### Approach 2: Built-In Function
This function uses the `map` method to loop through each `sub-array` in the input array `arr`. For each `sub-array`, it finds the largest number using the `Math.max` method and the `spread syntax` (...subArr). It then returns a new array containing the largest number from each sub-array.

### Implementation
```js
function findLargestNums(arr) {
  return arr.map(subArr => Math.max(...subArr));
}
```
