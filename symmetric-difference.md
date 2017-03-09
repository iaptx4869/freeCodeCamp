#### Symmetric Difference

------

Create a function that takes two or more arrays and returns an array of thesymmetric difference (`△` or `⊕`) of the provided arrays.

Given two sets (for example set `A = {1, 2, 3}` and set `B = {2, 3, 4}`), the mathematical term "symmetric difference" of two sets is the set of elements which are in either of the two sets, but not in both (`A △ B = C = {1, 4}`). For every additional symmetric difference you take (say on a set `D = {2, 3}`), you should get the set with elements which are in either of the two the sets but not both (`C △ D = {1, 4} △ {2, 3} = {1, 2, 3, 4}`).

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Try to pair program. Write your own code.

Here are some helpful links:

- [Array.prototype.reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)

- [Symmetric Difference](https://www.youtube.com/watch?v=PxffSUQRkG4)

`sym([1, 2, 3], [5, 2, 1, 4])` should return `[3, 4, 5]`.

`sym([1, 2, 3], [5, 2, 1, 4])` should contain only three elements.

`sym([1, 2, 5], [2, 3, 5], [3, 4, 5])` should return `[1, 4, 5]`

`sym([1, 2, 5], [2, 3, 5], [3, 4, 5])` should contain only three elements.

`sym([1, 1, 2, 5], [2, 2, 3, 5], [3, 4, 5, 5])` should return `[1, 4, 5]`.

`sym([1, 1, 2, 5], [2, 2, 3, 5], [3, 4, 5, 5])` should contain only three elements.

`sym([3, 3, 3, 2, 5], [2, 1, 5, 7], [3, 4, 6, 6], [1, 2, 3])` should return `[2, 3, 4, 6, 7]`.

`sym([3, 3, 3, 2, 5], [2, 1, 5, 7], [3, 4, 6, 6], [1, 2, 3])` should contain only five elements.

`sym([3, 3, 3, 2, 5], [2, 1, 5, 7], [3, 4, 6, 6], [1, 2, 3], [5, 3, 9, 8], [1])` should return `[1, 2, 4, 5, 6, 7, 8, 9]`.

`sym([3, 3, 3, 2, 5], [2, 1, 5, 7], [3, 4, 6, 6], [1, 2, 3], [5, 3, 9, 8], [1])` should contain only eight elements.

```js
function sym(args) {
    var arr = [];
    for (var i = 0; i < arguments.length; i++) {
        arr.push(arguments[i]);
    }
    var temp = arr.reduce(function (prev, cur, index, array) {
        var a = prev.filter(function (item) {
            return cur.indexOf(item) < 0;
        });
        var b = cur.filter(function (item) {
            return prev.indexOf(item) < 0;
        });
        return a.concat(b);
    });
    return temp.filter(function (item, index, array) {
        return array.indexOf(item) == index;
    });
}

sym([1, 2, 3], [5, 2, 1, 4]);
```
```js
function sym(args) {
    var arr = [];
    for (var i = 0; i < arguments.length; i++) {
        arr.push(arguments[i]);
    }
    var temp = arr.reduce(function (prev, cur, index, array) {
        var a = prev.filter(function (item) {
            return cur.indexOf(item) < 0;
        });
        var b = cur.filter(function (item) {
            return prev.indexOf(item) < 0;
        });
        return a.concat(b);
    });
    return unique(temp);
}
function unique(array) {
    var n = [];
    for (var i = 0; i < array.length; i++) {
        if (n.indexOf(array[i]) == -1) {
            n.push(array[i]);
        }
    }
    return n;
}

sym([1, 2, 3], [5, 2, 1, 4]);
```