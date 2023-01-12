# [How Much is True?](How%20Much%20is%20True%3F.md)

### Understanding the problem

Create a function which returns the number of `true` values there are in an array.
Return `0` if given an empty array.
All array items are of the type `bool` (true or false).

<pre>
<b>Input:</b> [true, false, false, true, false]
<b>Output:</b> 2
<b>Input:</b> []
<b>Output:</b> 0
</pre>

#
### Approach 1: For Loop

### Implementation

```js
function countTrue(arr) {
  let count = 0;
	for(i = 0; i < arr.length; i++){
		if(arr[i] === true){
			count++
		}
	}
	return count;
}
```
#
### Approach 2: Built-In Functions
- The `filter()` method return value, that is a shallow copy of a portion of the given array, filtered down to just the elements from the given array that pass the test implemented by the provided function. If no elements pass the test, an empty array will be returned.

### Implementation
```js
const count = arr.filter(Boolean).length;
```
