#### Repeat a string repeat a string

------

Repeat a given string (first argument) `num` times (second argument). Return an empty string if `num` is not a positive number.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Write your own code.

Here are some helpful links:

- [Global String Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

`repeatStringNumTimes("*", 3)` should return `"***"`.

`repeatStringNumTimes("abc", 3)` should return`"abcabcabc"`.

`repeatStringNumTimes("abc", 4)` should return`"abcabcabcabc"`.

`repeatStringNumTimes("abc", 1)` should return `"abc"`.

`repeatStringNumTimes("*", 8)` should return `"********"`.

`repeatStringNumTimes("abc", -2)` should return `""`.

```js
function repeatStringNumTimes(str, num) {
    // repeat after me
    if (num < 0) return "";
    else {
        var s = str;
        for (var i = 0; i < num - 1; i++) {
            str += s;
        }
    }
    return str;
}

repeatStringNumTimes("abc", 3);
```

```js
function repeatStringNumTimes(str, num) {
    // repeat after me
    var a = [];
    while (a.length < num) {
        a.push(str);
    }
    return a.join('');
}

repeatStringNumTimes("abc", 3);
```
