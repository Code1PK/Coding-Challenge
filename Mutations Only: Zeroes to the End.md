# [Mutations Only: Zeroes to the End](https://edabit.com/challenge/XR4suWJok9wdaNJ5j)

### Understanding the problem

Write a function that moves all the zeroes to the end of an array. Do this `without` returning a `copy` of the input array. You must `mutate` the original array. Keep the relative order of the `non-zero` elements the same.

<pre>
<b>Input:</b> [1, 2, 0, 0, 4, 0, 5]
<b>Output:</b> [1, 2, 4, 5, 0, 0, 0]
<b>Input:</b> [0, 0, 2, 0, 5]
<b>Output:</b> [2, 5, 0, 0, 0]
<b>Input:</b> [4, 4, 5]
<b>Output:</b> [4, 4, 5]
</pre>

#
### Approach: For Loop

### Implementation
```js
function zeroesToEnd(a) {
  let count = 0;
  for(i = 0; i < a.length; i ++){
    if(a[i] !== 0){
     a[count++] = a[i];
    } 
  }
  for(i = count; i < a.length; i ++){
    a[i] = 0;
  }
   return a;
}
```
