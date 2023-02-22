# [Add up the Numbers from a Single Number](https://edabit.com/challenge/4gzDuDkompAqujpRi)

### Understanding the problem

Create a function that takes a number as an argument. Add up all the numbers from 1 to the number you passed to the function. For example, if the input is 4 then your function should return 10 because 1 + 2 + 3 + 4 = 10.

<b>Notes:</b> Expect any positive number between 1 and 1000.

<pre>
<b>Examples:</b>
<b>Input:</b> addUp(4) <b>Output:</b> 10
<b>Input:</b> addUp(13) <b>Output:</b> 91
<b>Input:</b> addUp(600) <b>Output:</b> 180300
</pre>

#
### Approach: For Loop 


### Implementation
```js
function addUp(number){
  let sum = 0;
  for(let i=1; i<=number; i++){
    sum += i;
  }
  return sum;
}
```
