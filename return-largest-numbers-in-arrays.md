#### Return Largest Numbers in Arrays

------

Return an array consisting of the largest number from each provided sub-array. For simplicity, the provided array will contain exactly 4 sub-arrays.

Remember, you can iterate through an array with a simple for loop, and access each member with array syntax `arr[i]`.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Write your own code.

Here are some helpful links:

- [Comparison Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators)


```js
function largestOfFour(arr) {
    // You can do this!
    var m = [0, 0, 0, 0];
    for (var i = 0; i < 4; i++) {
        for (var j = 0; j < arr[i].length; j++) {
            m[i] = arr[i][j] > m[i] ? arr[i][j] : m[i];
        }
    }
    return m;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```
```js
function largestOfFour(arr) {
    // You can do this!
    var temp = [];
    for (var i = 0; i < arr.length; i++) {
        arr[i].sort(function(v1, v2) {
            return v2 - v1;
        });
        temp.push(arr[i][0]);
    }
    return temp;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```
```js
function largestOfFour(arr) {
    // You can do this!
    var temp = [];
    for (var i = 0; i < arr.length; i++) {
        var l = arr[i].reduce(function(prev, cur, index, array) {
            return prev > cur ? prev : cur;
        });
        temp.push(l);
    }
    return temp;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```
