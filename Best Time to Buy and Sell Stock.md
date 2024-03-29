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
<b>Input:</b> prices = [7,1,5,3,6,4] <b>Output:</b> 5 <b>Explanation:</b> Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.
Note that buying on day 2 and selling on day 1 is not allowed because you must buy before you sell.
<b>Input:</b> prices = [7,6,4,3,1] <b>Output:</b> 0 <b>Explanation:</b> In this case, no transactions are done and the max profit = 0.
</pre>

#
### Approach: For Loop


### Implementation
```js
function maxProfit(prices) {
	let profit = 0;
	for (let i = 0; i < prices.length - 1; i++) {
		for (let j = i + 1; j < prices.length; j++) {
			const currentProfit = prices[j] - prices[i];

			if (currentProfit > profit) {
				profit = currentProfit;
			}
		}
	}

	return profit;
}
```
