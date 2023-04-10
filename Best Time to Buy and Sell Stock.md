# [ Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)

### Understanding the problem
You are given an array `prices` where `prices[i]` is the price of a given stock on the `ith` day.

You want to maximize your profit by choosing a `single day` to buy one stock and choosing a `different day in the future` to sell that stock.

Return `the maximum profit you can achieve from this transaction`. If you cannot achieve any profit, return `0`.

<b>Constraints:</b>

- 1 <= prices.length <= 105
- 0 <= prices[i] <= 104

<pre>
<b>Examples:</b>
<b>Input:</b> numRows = 5 <b>Output:</b> [[1],[1,1],[1,2,1],[1,3,3,1],[1,4,6,4,1]]
<b>Input:</b> numRows = 1 <b>Output:</b> [[1]]
</pre>

#
### Approach: Dynamic programming approach (tabulation)
`Tabulation` is an approach where you solve a dynamic programming problem by first filling up a table, and then compute the solution to the original problem based on the results in this table.

### Implementation
```js
let generate = function(numRows) {
    const table = [];
    for (let i = 0; i < numRows; i++) {
        table[i] = [];
        table[i][0] = 1;
        for (let j = 1; j < i; j++) {
            table[i][j] = table[i-1][j-1] + table[i-1][j]
        }
        table[i][i] = 1;
    }
    return table;
}
```
