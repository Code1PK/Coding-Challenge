# [Array of Multiples](https://edabit.com/challenge/ebcd4Xu8TLizaj6dm)

### Understanding the problem

Create a function that takes two numbers as arguments (`num`, `length`) and returns an array of multiples of `num` until the array length reaches `length`. Notice that `num` is also included in the returned array.

<pre>
<b>Input:</b> (7, 5)
<b>Output:</b> [7, 14, 21, 28, 35]
<b>Input:</b> (17, 6)
<b>Output:</b> [17, 34, 51, 68, 85, 102]
</pre>

#
### Approach: 


### Implementation
```js
function arrayOfMultiples (num, length) {
  let arr = [];
  for(i = 1; i <= length; i ++){
    let number = i*num;
    arr.push(number);
  }
	return arr;
}

console.log(arrayOfMultiples(7,5));
console.log(arrayOfMultiples(17,6));
```
