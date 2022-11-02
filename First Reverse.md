# [First Reverse](https://www.coderbyte.com/editor/First%20Reverse:JavaScript)

### Understanding the problem

Have the function FirstReverse(str) take the str parameter being passed and return the string in reversed order. For example: if the input string is "Hello World and Coders" then your program should return the string sredoC dna dlroW olleH.

```
Input: "coderbyte"
Output: etybredoc
Input: "I Love Code"
Output: edoC evoL I
```
#

### Approach 1: Reverse a String With Built-In Functions

For this solution, we will use three methods: the String.prototype.split() method, the Array.prototype.reverse() method and the Array.prototype.join() method.

- The split() method splits a String object into an array of string by separating the string into sub strings.  
- The reverse() method reverses an array in place. The first array element becomes the last and the last becomes the first.   
- The join() method joins all elements of an array into a string.  

### Implementation

```js
function FirstReverse(str) {
    return str.split("").reverse().join("");
}
FirstReverse("coderbyte");
```

### Approach 2: Reverse a String With a Decrementing For Loop
### Implementation
```js
function FirstReverse(str) {
    let newString = "";
    for (let i = str.length - 1; i >= 0; i--) {
        newString += str[i];
    }
    return newString;
}
FirstReverse("coderbyte");
```



