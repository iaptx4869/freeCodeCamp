#### Caesars Cipher

------

One of the simplest and most widely known ciphers is a `Caesar cipher`, also known as a `shift cipher`. In a `shift cipher` the meanings of the letters are shifted by some set amount.

A common modern use is the [ROT13](https://en.wikipedia.org/wiki/ROT13) cipher, where the values of the letters are shifted by 13 places. Thus 'A' ↔ 'N', 'B' ↔ 'O' and so on.

Write a function which takes a [ROT13](https://en.wikipedia.org/wiki/ROT13) encoded string as input and returns a decoded string.

All letters will be uppercase. Do not transform any non-alphabetic character (i.e. spaces, punctuation), but do pass them on.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Try to pair program. Write your own code.

Here are some helpful links:

- [String.prototype.charCodeAt()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charCodeAt)

- [String.fromCharCode()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)

`rot13("SERR PBQR PNZC")` should decode to `"FREE CODE CAMP"`

`rot13("SERR CVMMN!")` should decode to `"FREE PIZZA!"`

`rot13("SERR YBIR?")` should decode to `"FREE LOVE?"`

`rot13("GUR DHVPX OEBJA QBT WHZCRQ BIRE GUR YNML SBK.")`should decode to `"THE QUICK BROWN DOG JUMPED OVER THE LAZY FOX."`

```js
function rot13(str) {
    var newString = "";
    for (var i in str) {
        var temp = str.charCodeAt(i);
        if (temp < 65 || temp > 91) {
            newString += str[i];
            continue;
        }
        if (temp > 77) {
            newString += String.fromCharCode(temp - 13);
        } else {
            newString += String.fromCharCode(temp + 13);
        }
    }
    return newString;
}

// Change the inputs below to test
rot13("SERR PBQR PNZC");
```

```js
function rot13(str) { // LBH QVQ VG!
    var index = null;
    var temp = "";
    var _A = "A".charCodeAt(0);
    var _Z = "Z".charCodeAt(0);
    var mid = (_A + _Z) / 2;
    for (var i = 0; i < str.length; i++) {
        index = str.charCodeAt(i);
        if (index >= _A && index <= mid) {
            temp += String.fromCharCode(index + 13);
        } else if (index <= _Z && index > mid) {
            temp += String.fromCharCode(index - 13);
        } else {
            temp += String.fromCharCode(index);
        }
    }
    return temp;
}

// Change the inputs below to test
rot13("SERR PBQR PNZC");
```
