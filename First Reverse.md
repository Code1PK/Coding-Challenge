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

### Approach 1: Iterative

The Binary Search algorithm works by dividing the search space into halves, and based on the value of the middle element, it eliminates half of the search space.

We maintain two pointers `left` and `right` that are going to define the current search space. Initially, the search space is the entire list. We find the middle value using the two pointers and compare it to the search target. If the middle value is equal to the target value, we've found the target. If the middle value is greater than the target, then it means the target value cannot lie in the right half of the search space. Because the list is sorted, all the values that come after the middle value must be greater than the middle value and even greater than the target, so we can remove the entire right half, narrowing down the search space to the left half. If the middle value is smaller than the target, then we can discard the entire left half and search for the target value in the right half. We repeat this process until the target value is found, or our search space is exhausted.

### Implementation

```js
function binarySearch(array, target) {
  let left = 0;
  let right = array.length - 1;

  while (left <= right) {
    // Avoid overflow
    const mid = left + Math.floor((right - left) / 2);

    if (target === array[mid]) return mid;

    if (target < array[mid]) {
      right = mid - 1;
    } else {
      left = mid + 1;
    }
  }
  return -1;
}
```

### Complexity Analysis

- Time Complexity: O(log(N)), where N is the number of integers in the input array.

- Space Complexity: O(1).

#

### Approach 2: Recursive
