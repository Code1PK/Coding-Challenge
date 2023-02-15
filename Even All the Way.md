# [Even All the Way](https://edabit.com/challenge/6MZx5RqKYkFaogeAQ)

### Understanding the problem

Given an `array` of numbers, return an `array` which contains all the `even` numbers in the original array, which also have even indices.

<b>Notes:</b> Arrays start at index 0.

<pre>
<b>Examples:</b>
<b>Input:</b> getOnlyEvens([1, 3, 2, 6, 4, 8]) <b>Output:</b> [2, 4]
<b>Input:</b> getOnlyEvens([0, 1, 2, 3, 4]) <b>Output:</b> [0, 2, 4]
<b>Input:</b> getOnlyEvens([1, 2, 3, 4, 5]) <b>Output:</b> []
</pre>

#
### Approach 1: For Loop 
The function first initializes an empty array `result` to store the even numbers that meet the criteria. Then, it loops through the elements of the input array `arr`, starting at index `0` and incrementing by `2` at each iteration, to only check `even indices`. If the current element is `even` (i.e., its value is divisible by 2 with no remainder), it is added to the `result` array using the `push` method.

### Implementation
```js
function getOnlyEvens(arr) {
  let result = []; 
  for (let i = 0; i < arr.length; i += 2) {
    if (arr[i] % 2 === 0) {
      result.push(arr[i]);
    }
  }
  
  return result;
}

```
#
### Approach 2: Built-In Function


### Implementation
```js
f

```
