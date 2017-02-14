#### DNA Pairing

------

The DNA strand is missing the pairing element. Take each character, get its pair, and return the results as a 2d array.

[Base pairs](http://en.wikipedia.org/wiki/Base_pair) are a pair of AT and CG. Match the missing element to the provided character.

Return the provided character as the first element in each array.

For example, for the input GCG, return [["G", "C"], ["C","G"],["G", "C"]]

The character and its pair are paired up in an array, and all the arrays are grouped into one encapsulating array.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Try to pair program. Write your own code.

Here are some helpful links:

- [Array.prototype.push()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)

- [String.prototype.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)

`pairElement("ATCGA")` should return `[["A","T"],["T","A"],["C","G"],["G","C"],["A","T"]]`.

`pairElement("TTGAG")` should return `[["T","A"],["T","A"],["G","C"],["A","T"],["G","C"]]`.

`pairElement("CTCTA")` should return `[["C","G"],["T","A"],["C","G"],["T","A"],["A","T"]]`.

```js
function pairElement(str) {
    var arr = str.split("");
    var pair = "";
    var result = arr.map(function(item, index, array) {
        if (item === "A") {
            pair = "T";
        } else if (item === "T") {
            pair = "A";
        } else if (item === "C") {
            pair = "G";
        } else if (item === "G") {
            pair = "C";
        }
        return [item, pair];
    });
    return result;
}

pairElement("GCG");
```
