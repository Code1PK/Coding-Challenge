# [First Reverse](https://www.coderbyte.com/editor/First%20Reverse:JavaScript)

### Understanding the problem

Have the `function FirstReverse(str)` take the `str` parameter being passed and return the string in reversed order. For example: if the input string is `"Hello World and Coders"` then your program should return the string `sredoC dna dlroW olleH`.

<pre>
<b>Input:</b> "coderbyte"
<b>Output:</b> etybredoc
<b>Input:</b> "I Love Code"
<b>Output:</b> edoC evoL I
</pre>
#

### Approach 1: Reverse a String With Built-In Functions

For this solution, we will use three methods: the `String.prototype.split()` method, the `Array.prototype.reverse()` method and the `Array.prototype.join()` method.

- The `split()` method splits a String object into an array of string by separating the string into sub strings.  
- The `reverse()` method reverses an array in place. The first array element becomes the last and the last becomes the first.   
- The `join()` method joins all elements of an array into a string.  

### Implementation

```js
function FirstReverse(str) {
    return str.split("").reverse().join("");
}
console.log(FirstReverse("coderbyte"));
```
#
### Approach 2: Reverse a String With a Decrementing For Loop

The starting point of the loop will be `(str.length - 1)` which corresponds to the last character of the string, `"e"`.
As long as `i` is greater than or equals `0`, the loop will go on. We decrement `i` after each iteration.

### Implementation
```js
function FirstReverse(str) {
    let newString = "";
    for (let i = str.length - 1; i >= 0; i--) {
        newString += str[i];
    }
    return newString;
}
console.log(FirstReverse("coderbyte"));
```
#
### Approach 3: Reverse a String With Recursion

For this solution, we will use two methods: the `String.prototype.substr()` method and the `String.prototype.charAt()` method.

- The `substr()` method returns the characters in a string beginning at the specified location through the specified number of characters.
  - `"coderbyte".substr(1); // "oderbyte"`
- The `charAt()` method returns the specified character from a string.
  - `"coderbyte".charAt(0); // "c"`
 
The depth of the recursion is equal to the length of the String. This solution is not the best one and will be really slow if the String is very long and the stack size is of major concern.

### Implementation

```js
function FirstReverse(str) {
  if (str === "")
    return "";
  else
    return FirstReverse(str.substr(1)) + str.charAt(0);
}
console.log(FirstReverse("coderbyte"));
```
