#### Find the Longest Word in a String

------

Return the length of the longest word in the provided sentence.

Your response should be a number.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Write your own code.

Here are some helpful links:

- [String.prototype.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)

- [String.length](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/length)

`findLongestWord("The quick brown fox jumped over the lazy dog")` should return a number.

`findLongestWord("The quick brown fox jumped over the lazy dog")` should return 6.

`findLongestWord("May the force be with you")` should return 5.

`findLongestWord("Google do a barrel roll")` should return 6.

`findLongestWord("What is the average airspeed velocity of an unladen swallow")` should return 8.

`findLongestWord("What if we try a super-long word such as otorhinolaryngology")` should return 19.

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
