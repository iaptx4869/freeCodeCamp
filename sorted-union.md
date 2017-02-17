#### Sorted Union

------

Write a function that takes two or more arrays and returns a new array of unique values in the order of the original provided arrays.

In other words, all values present from all arrays should be included in their original order, but with no duplicates in the final array.

The unique numbers should be sorted by their original order, but the final array should not be sorted in numerical order.

Check the assertion tests for examples.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Try to pair program. Write your own code.

Here are some helpful links:

- [Arguments object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments)

- [Array.prototype.reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)

`uniteUnique([1, 3, 2], [5, 2, 1, 4], [2, 1])` should return `[1, 3, 2, 5, 4]`.

`uniteUnique([1, 3, 2], [1, [5]], [2, [4]])` should return`[1, 3, 2, [5], [4]]`.

`uniteUnique([1, 2, 3], [5, 2, 1])` should return `[1, 2, 3, 5]`.

`uniteUnique([1, 2, 3], [5, 2, 1, 4], [2, 1], [6, 7, 8])`should return `[1, 2, 3, 5, 4, 6, 7, 8]`.

```js
function uniteUnique(arr) {
    var args = Array.from(arguments);
    arr = args.reduce(function(prev, cur, index, array) {
        return prev.concat(cur);
    });
    return arr.filter(function(item, index, array) {
        return array.indexOf(item) === index;
    });
}

uniteUnique([1, 3, 2], [5, 2, 1, 4], [2, 1]);
```
