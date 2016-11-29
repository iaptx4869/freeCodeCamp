#### Chunky Monkey

------

Write a function that splits an array (first argument) into groups the length of `size`(second argument) and returns them as a two-dimensional array.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Write your own code.

Here are some helpful links:

- [Array.prototype.push()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)


- [Array.prototype.slice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)


```js
function chunkArrayInGroups(arr, size) {
    // Break it up.
    var newArr = [];
    for (var i = 0; i < arr.length / size; i++) {
        var tempArr = arr.slice(size * i, size * (i + 1));
        newArr.push(tempArr);
    }
    return newArr;
}

chunkArrayInGroups(["a", "b", "c", "d"], 2);
```
```js
function chunkArrayInGroups(arr, size) {
    // Break it up.
    var temp = [];
    for (var i = 0; i < arr.length; i += size) {
        temp.push(arr.slice(i, i + size));
    }
    return temp;
}

chunkArrayInGroups(["a", "b", "c", "d"], 2);
```
