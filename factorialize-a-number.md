#### Factorialize a Number

------

Return the factorial of the provided integer.

If the integer is represented with the letter n, a factorial is the product of all positive integers less than or equal to n.

Factorials are often represented with the shorthand notation `n!`

For example: `5! = 1 * 2 * 3 * 4 * 5 = 120`

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Write your own code.

Here are some helpful links:

- [Arithmetic Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators)

`factorialize(5)` should return a number.

`factorialize(5)` should return 120.

`factorialize(10)` should return 3628800.

`factorialize(20)` should return 2432902008176640000.

`factorialize(0)` should return 1.

```js
function factorialize(num) {
    if (num <= 1) {
        return 1;
    } else {
        return num * factorialize(num - 1);
    }
}

factorialize(5);
```
