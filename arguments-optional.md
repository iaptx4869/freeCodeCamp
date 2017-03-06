#### Arguments Optional

------

Create a function that sums two arguments together. If only one argument is provided, then return a function that expects one argument and returns the sum.

For example, `addTogether(2, 3)` should return `5`, and `addTogether(2)` should return a function.

Calling this returned function with a single argument will then return the sum:

`var sumTwoAnd = addTogether(2);`

`sumTwoAnd(3)` returns `5`.

If either argument isn't a valid number, return undefined.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Try to pair program. Write your own code.

Here are some helpful links:

- [Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)

- [Arguments object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments)

`addTogether(2, 3)` should return 5.

`addTogether(2)(3)` should return 5.

`addTogether("http://bit.ly/IqT6zt")`should return undefined.

`addTogether(2, "3")` should return undefined.

`addTogether(2)([3])` should return undefined.

```js
function addTogether() {
    if (typeof arguments[0] !== "number" || (arguments.length > 1 && typeof arguments[1] !== "number")) {
        return undefined;
    }
    if (arguments.length == 1) {
        var arg0 = arguments[0];
        return function (num) {
            if (typeof num !== "number") {
                return undefined;
            }
            return arg0 + num;
        };
    } else {
        return arguments[0] + arguments[1];
    }
}

addTogether(2, 3);
```
