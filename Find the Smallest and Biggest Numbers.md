# Find the Smallest and Biggest Numbers
### Understanding the problem
Create a function that takes an array of numbers and return both the minimum and maximum numbers, in that order.

<pre>
<b>Input:</b> minMax([1, 2, 3, 4, 5])
<b>Output:</b> [1, 5]
<b>Input:</b> minMax([2334454, 5])
<b>Output:</b> [5, 2334454]
<b>Input:</b> minMax([1])
<b>Output:</b> [1, 1]
</pre>
<b>Notes:</b> All test arrays will have at least one element and are valid.
#

### Approach : Built-In Functions
### Implementation
```js
function minMax(arr){
  let arrResult = [];
  arrResult.push(Math.min(...arr));
  arrResult.push(Math.max(...arr));
  return arrResult;
}

console.log(minMax([1, 2, 3, 4, 5]));
console.log(minMax([2334454, 5]));
console.log(minMax([1]));
```
