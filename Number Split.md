# [Number Split](https://edabit.com/challenge/xsi99TwpGyFC8KS6d)

### Understanding the problem

Given a `number`, return an `array` containing the two halves of the number. If the number is odd, make the `rightmost number higher`.

<b>Notes:</b> 
- All numbers will be integers.
- You can expect negative numbers too.

<pre>
<b>Examples:</b>
<b>Input:</b> numberSplit(4) <b>Output:</b> [2, 2]
<b>Input:</b> numberSplit(11) <b>Output:</b> [5, 6]
<b>Input:</b> numberSplit(-9) <b>Output:</b> [-5, -4]
</pre>

#
### Approach 1: Built-In Functions  
The `Math.floor()` static method always rounds down and returns the largest integer less than or equal to a given number.

### Implementation 1
```js
function numberSplit(num){
  let y = Math.floor(num/2);
  let x = num - y;
  let result = [];
  result.push(Math.min(x,y));
  result.push(Math.max(x,y));
  return result;
}
```
### Implementation 2
```js
function numberSplit(num) {
  let left, right;
  if (num % 2 === 0) {
    left = right = num / 2;
  } else {
    left = Math.floor(num / 2);
    right = num - left;
  }
  return [left, right];
}
```
