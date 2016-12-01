#### Mutations

------

Return true if the string in the first element of the array contains all of the letters of the string in the second element of the array.

For example, `["hello", "Hello"]`, should return true because all of the letters in the second string are present in the first, ignoring case.

The arguments `["hello", "hey"]` should return false because the string "hello" does not contain a "y".

Lastly, `["Alien", "line"]`, should return true because all of the letters in "line" are present in "Alien".

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Write your own code.

Here are some helpful links:

- [String.prototype.indexOf()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf)

`mutation(["hello", "hey"])` should return false.

`mutation(["hello", "Hello"])` should return true.

`mutation(["zyxwvutsrqponmlkjihgfedcba", "qrstu"])` should return true.

`mutation(["Mary", "Army"])` should return true.

`mutation(["Mary", "Aarmy"])` should return true.

`mutation(["Alien", "line"])` should return true.

`mutation(["floor", "for"])` should return true.

`mutation(["hello", "neo"])` should return false.

`mutation(["voodoo", "no"])` should return false.

```js
function mutation(arr) {
    var m = arr[0].toLowerCase();
    var n = arr[1].toLowerCase();
    for (var i = 0; i < n.length; i++) {
        if (m.indexOf(n[i]) == -1) return false;
    }
    return true;
}

mutation(["hello", "hey"]);
```
