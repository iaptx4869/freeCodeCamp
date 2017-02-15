#### Missing letters

------

Find the missing letter in the passed letter range and return it.

If all letters are present in the range, return undefined.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Try to pair program. Write your own code.

Here are some helpful links:

- [String.prototype.charCodeAt()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charCodeAt)

- [String.fromCharCode()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)

`fearNotLetter("abce")` should return "d".

`fearNotLetter("abcdefghjklmno")` should return "i".

`fearNotLetter("bcd")` should return undefined.

`fearNotLetter("yz")` should return undefined.

```js
function fearNotLetter(str) {
    var arr = str.split("");
    var temp = [];
    var start = str.charCodeAt(0);
    var end = str.charAt(str.length - 1).charCodeAt(0);
    for (var i = start; i < end + 1; i++) {
        var item = String.fromCharCode(i);
        if (arr[0] !== item) {
            temp.push(item);
        } else {
            arr.shift();
        }
    }
    if (temp.length === 0) {
        return undefined;
    } else {
        return temp.join("");
    }
}

fearNotLetter("abce");
```
