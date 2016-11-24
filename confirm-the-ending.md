#### Confirm the Ending

------

Check if a string (first argument, `str`) ends with the given target string (second argument, `target`).

This challenge *can* be solved with the `.endsWith()` method, which was introduced in ES2015. But for the purpose of this challenge, we would like you to use one of the JavaScript substring methods instead.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Write your own code.

Here are some helpful links:

- [String.prototype.substr()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substr)


- [String.prototype.substring()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substring)


```js
function confirmEnding(str, target) {
    // "Never give up and good luck will find you."
    // -- Falcor
    var l = -target.length;
    if (str.substr(l) === target) return true;
    else return false;
}

confirmEnding("Bastian", "n");
```
```js
function confirmEnding(str, target) {
    // "Never give up and good luck will find you."
    // -- Falcor
    return str.substr(-target.length, target.length) === target;
}

confirmEnding("Bastian", "n");
```
