#### Smallest Common Multiple

------

Find the smallest common multiple of the provided parameters that can be evenly divided by both, as well as by all sequential numbers in the range between these parameters.

The range will be an array of two numbers that will not necessarily be in numerical order.

e.g. for 1 and 3 - find the smallest common multiple of both 1 and 3 that is evenly divisible by all numbers *between* 1 and 3.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Try to pair program. Write your own code.

Here are some helpful links:

- [Smallest Common Multiple](https://www.mathsisfun.com/least-common-multiple.html)

`smallestCommons([1, 5])` should return a number.

`smallestCommons([1, 5])` should return 60.

`smallestCommons([5, 1])` should return 60.

`smallestCommons([1, 13])` should return 360360.

`smallestCommons([23, 18])` should return 6056820.

```js
function smallestCommons(arr) {
	var min = Math.min(arr[0], arr[1]);
	var max = Math.max(arr[0], arr[1]);
	var _arr = [];
	for (var i = min; i <= max; i++) {
		_arr.push(i);
	}
	var gcd = function(a, b) {
		if (b) {
			return gcd(b, a % b);
		}
		return a;
	};
	return _arr.reduce(function(prev, cur, index, array) {
		return prev * cur / gcd(prev, cur);
	});
}

smallestCommons([1,5]);
```
