# [Filter out Strings from an Array](https://edabit.com/challenge/b2NdDSdkjqFnCTfS8)

### Understanding the problem

Create a function that takes an `array` of non-negative integers and strings and return a `new array` without the strings.

<b>Notes:</b>
- Zero is a non-negative integer.
- The given array only has integers and strings.
- Numbers in the array should not repeat.
- The original order must be maintained.

<pre>
<b>Input:</b> filterArray([1, 2, "a", "b"])
<b>Output:</b> [1, 2]
<b>Input:</b> filterArray([1, "a", "b", 0, 15])
<b>Output:</b> [1, 0, 15]
<b>Input:</b> filterArray([1, 2, "aasf", "1", "123", 123])
<b>Output:</b> [1, 2, 123]
</pre>

#
### Approach 1: For Loop

### Implementation
```js
function filterArray(arr){
  let filteredArray = [];
  for (let i = 0; i < arr.length; i++){
    if (Number.isInteger(arr[i]) === true){
      filteredArray.push(arr[i])
    }
  }
  let uniqueNumbers; 
  return uniqueNumbers = [...new Set(filteredArray)];
}
```
#
### Approach 2: Built-In Functions
In this function, we initialize an empty array `uniqueNumbers` to store the unique non-negative integers. Then, we use the `forEach` method to iterate over the input array `arr`. For each element in the array, the function checks if its type is `'number'` and if it is not already in the `uniqueNumbers` array (using the `includes` method). If both conditions are satisfied, the `number` is added to the `uniqueNumbers` array. Finally, the `uniqueNumbers` array is returned as the result.

### Implementation
```js
function filterArray(arr) {
  let uniqueNumbers = [];
  arr.forEach(function(val) {
    if (typeof val === 'number' && !uniqueNumbers.includes(val)) {
      uniqueNumbers.push(val);
    }
  });
  return uniqueNumbers;
}

```
