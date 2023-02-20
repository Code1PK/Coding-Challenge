# [Absolute Sum](https://edabit.com/challenge/rCmEy2AQYLbRGgKyL)

### Understanding the problem

Take an `array` of integers (positive or negative or both) and return the `sum` of the absolute value of each element.

<b>Notes:</b> 
- The term "absolute value" means to remove any negative sign in front of a number, and to think of all numbers as positive (or zero).
- All the elements in the given array are integers.

<pre>
<b>Examples:</b>
<b>Input:</b> getAbsSum([2, -1, 4, 8, 10]) <b>Output:</b> 25
<b>Input:</b> getAbsSum([-3, -4, -10, -2, -3]) <b>Output:</b> 22
<b>Input:</b> getAbsSum([-1]) <b>Output:</b> 1
</pre>

#
### Approach 1: For Loop 
The `Math.abs()` function is used to get the absolute value of each element. It returns the absolute value of a number, which is the number itself if it's positive, or the negative of the number if it's negative.

### Implementation
```js
function getAbsSum(arr){
  let sum = 0;
  for(let i = 0; i < arr.length; i++){ 
    sum += Math.abs(arr[i]);
  }
  return sum;
}
```

