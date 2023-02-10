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
### Approach: For Loop

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
