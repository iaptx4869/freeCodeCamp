#### Find the Longest Word in a String

------

Return the length of the longest word in the provided sentence.

Your response should be a number.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Write your own code.

Here are some helpful links:

- [String.prototype.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)


- [String.length](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/length)


```js
function findLongestWord(str) {
    var arr = str.split(" ");
    var max = 0;
    for (var i = 0; i < arr.length; i++) {
        if (arr[i].length > max) max = arr[i].length;
    }
    return max;
}

findLongestWord("The quick brown fox jumped over the lazy dog");
```
