# [Converting Objects to Arrays](https://edabit.com/challenge/pPNAs5PvB3WvnDwDM)

### Understanding the problem

Write a function that converts an object into an array, where each element represents a key-value pair in the form of an array. Return an empty array if the object is empty.

<pre>
<b>Input:</b> { a: 1, b: 2 }
<b>Output:</b> ["a", 1], ["b", 2]
<b>Input:</b> { shrimp: 15, tots: 12 }
<b>Output:</b> ["shrimp", 15], ["tots", 12]
</pre>

#
### Approach: 
The `Object.entries()` static method returns an array of a given object's own enumerable string-keyed property key-value pairs.

### Implementation
```js
function toArray(obj) {
  let newArr = Object.entries(obj);
	return newArr;
}

console.log(toArray({ a: 1, b: 2 }));
console.log(toArray({ shrimp: 15, tots: 12 }));
console.log(toArray({}));
```
