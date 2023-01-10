# [Pair Management](https://edabit.com/challenge/BFnsRqe8PFvEwcRNt)

### Understanding the problem

Given two arguments, return an array which contains these two arguments.

<pre>
<b>Input:</b> 1, 2
<b>Output:</b> [1, 2]
<b>Input:</b> 51, 21
<b>Output:</b> [51, 21]
</pre>

#
### Approach 1: Spread syntax

The `spread syntax` is a new addition to the set of operators in JavaScript ES6. It takes in an iterable (e.g an array) and expands it into individual elements.

### Implementation
```js
function makePair(num1, num2) {
	return [...arguments]
}
```
#
### Approach 2: Built-In Functions

For this solution, we will use `push` method.

- The `push()` method adds one or more elements to the end of an array and returns the new length of the array. 

### Implementation

```js
function makePair(num1, num2) {
	let result = [];
	result.push(num1);
	result.push(num2);
	return result;
}
```
#
### Approach 3:
### Implementation
```js
function makePair(num1, num2) {
	return [num1,num2];
}
```
