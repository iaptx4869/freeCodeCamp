#### Steamroller

------

Flatten a nested array. You must account for varying levels of nesting.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Try to pair program. Write your own code.

Here are some helpful links:

- [Array.isArray()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/isArray)

`steamrollArray([[["a"]], [["b"]]])` should return `["a", "b"]`.

`steamrollArray([1, [2], [3, [[4]]]])` should return `[1, 2, 3, 4]`.

`steamrollArray([1, [], [3, [[4]]]])` should return `[1, 3, 4]`.

`steamrollArray([1, {}, [3, [[4]]]])` should return `[1, {}, 3, 4]`.

```js
function steamrollArray(arr) {
    // I'm a steamroller, baby
    var result = [];
    for (var i = 0; i < arr.length; i++) {
        if (Array.isArray(arr[i])) {
            result = result.concat(steamrollArray(arr[i]));
        } else {
            result.push(arr[i]);
        }
    }
    return result;
}

steamrollArray([1, [2], [3, [[4]]]]);
```
