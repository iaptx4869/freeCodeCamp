#### Roman Numeral Converter

------

Convert the given number into a roman numeral.

All [roman numerals](http://www.mathsisfun.com/roman-numerals.html) answers should be provided in upper-case.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Try to pair program. Write your own code.

Here are some helpful links:

- [Roman Numerals](http://www.mathsisfun.com/roman-numerals.html)

- [Array.prototype.splice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)

- [Array.prototype.indexOf()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)

- [Array.prototype.join()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)

`convertToRoman(2)` should return "II".

`convertToRoman(3)` should return "III".

`convertToRoman(4)` should return "IV".

`convertToRoman(5)` should return "V".

`convertToRoman(9)` should return "IX".

`convertToRoman(12)` should return "XII".

`convertToRoman(16)` should return "XVI".

`convertToRoman(29)` should return "XXIX".

`convertToRoman(44)` should return "XLIV".

`convertToRoman(45)` should return "XLV"

`convertToRoman(68)` should return "LXVIII"

`convertToRoman(83)` should return "LXXXIII"

`convertToRoman(97)` should return "XCVII"

`convertToRoman(99)` should return "XCIX"

`convertToRoman(500)` should return "D"

`convertToRoman(501)` should return "DI"

`convertToRoman(649)` should return "DCXLIX"

`convertToRoman(798)` should return "DCCXCVIII"

`convertToRoman(891)` should return "DCCCXCI"

`convertToRoman(1000)` should return "M"

`convertToRoman(1004)` should return "MIV"

`convertToRoman(1006)` should return "MVI"

`convertToRoman(1023)` should return "MXXIII"

`convertToRoman(2014)` should return "MMXIV"

`convertToRoman(3999)` should return "MMMCMXCIX"

```js
function convertToRoman(num) {
    var nums = [1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1];
    var romans = ["m", "cm", "d", "cd", "c", "xc", "l", "xl", "x", "ix", "v", "iv", "i"];
    var str = '';
    nums.forEach(function(item, index, array) {
        while (num >= item) {
            str += romans[index];
            num -= item;
        }
    });
    return str.toUpperCase();
}

convertToRoman(36);
```

```js
function convertToRoman(num) {
    var nums = [1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1];
    var romans = ["M", "CM", "D", "CD", "C", "XC", "L", "XL", "X", "IX", "V", "IV", "I"];
    var str = '';
    nums.forEach(function(item, index, array) {
        while (num >= item) {
            str += romans[index];
            num -= item;
        }
    });
    return str;
}

convertToRoman(36);
```
