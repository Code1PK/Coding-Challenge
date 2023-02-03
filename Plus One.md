# [Plus One](https://leetcode.com/problems/plus-one/)

### Understanding the problem

You are given a `large integer` represented as an integer array `digits`, where each `digits[i]` is the `ith` digit of the integer. The digits are ordered from most significant to least significant in left-to-right order. The large integer does not contain any leading `0`'s.
Increment the large integer by one and return the `resulting array of digits`.

<pre>
<b>Input:</b> digits = [1,2,3]
<b>Output:</b> [1,2,4]
<b>Explanation:</b> The array represents the integer 123. Incrementing by one gives 123 + 1 = 124. Thus, the result should be [1,2,4].

<b>Input:</b> digits = [4,3,2,1]
<b>Output:</b> [4,3,2,2]
<b>Explanation:</b> The array represents the integer 4321. Incrementing by one gives 4321 + 1 = 4322. Thus, the result should be [4,3,2,2].
</pre>

#
### Approach: For Loop With Built-In Function

This function loops through the digits array starting from the rightmost digit (the least significant digit) and incrementing the digit by one. If the digit is 9, it is reset to 0 and the loop continues to the next digit to the left. If a digit less than 9 is found, it is incremented by one and the loop returns the resulting array. If all digits are 9, a 1 is added to the beginning of the array to represent the carry-over.

- The `unshift()` method is used in the code to add the value 1 to the beginning of the digits array in the case where all of the digits are 9. This is necessary because the incrementation of the last digit (which is 9) results in a carry-over that adds a leading digit of 1 to the number.

For example, if the original array digits is [9, 9, 9], after the loop has completed, the array will be [0, 0, 0]. To correctly represent the incremented number, which is 1000, the unshift() method is used to add 1 to the beginning of the array, resulting in [1, 0, 0, 0].

### Implementation
```js
function plusOne(digits) {
  for (let i = digits.length - 1; i >= 0; i--) {
    if (digits[i] === 9) {
      digits[i] = 0;
    } else {
      digits[i]++;
      return digits;
    }
  }
  digits.unshift(1);
  return digits;
}

```
