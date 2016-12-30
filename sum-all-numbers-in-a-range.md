#### Sum All Numbers in a Range

------

We'll pass you an array of two numbers. Return the sum of those two numbers and all numbers between them.

The lowest number will not always come first.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Try to pair program. Write your own code.

Here are some helpful links:

- [Math.max()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/max)

- [Math.min()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/min)

- [Array.prototype.reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)

`sumAll([1, 4])` should return a number.

`sumAll([1, 4])` should return 10.

`sumAll([4, 1])` should return 10.

`sumAll([5, 10])` should return 45.

`sumAll([10, 5])` should return 45.

```js
function sumAll(arr) {
    return (arr[0] + arr[1]) * (Math.abs(arr[0] - arr[1]) + 1) / 2;
}

sumAll([1, 4]);
```

```js
function sumAll(arr) {
    var result = 0;
    a_start = Math.min(arr[0], arr[1]);
    a_end = Math.max(arr[0], arr[1]);
    while (a_start <= a_end) {
        result += a_start;
        a_start++;
    }
    return result;
}

sumAll([1, 4]);
```

```js
function sumAll(arr) {
    var arryA = [];
    var max = Math.max.apply(null, arr);
    var min = Math.min.apply(null, arr);
    var sum = 0;
    var sumFun = function(max, min) {
        for (var i = 0; i < (max - min + 1); i++) {
            arryA.push(min + i);
        }
        console.log(arryA);
        var value = arryA.reduce(function(previousValue, currentValue) {
            return previousValue + currentValue;
        });
        return value;
    };
    sum = sumFun(max, min);
    return sum;
}

sumAll([1, 4]);
```
