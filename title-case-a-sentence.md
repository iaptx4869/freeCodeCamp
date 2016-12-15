#### Title Case a Sentence

------

Return the provided string with the first letter of each word capitalized. Make sure the rest of the word is in lower case.

For the purpose of this exercise, you should also capitalize connecting words like "the" and "of".

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Write your own code.

Here are some helpful links:

- [String.prototype.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)

`titleCase("I'm a little tea pot")` should return a string.

`titleCase("I'm a little tea pot")` should return "I'm A Little Tea Pot".

`titleCase("sHoRt AnD sToUt")` should return "Short And Stout".

`titleCase("HERE IS MY HANDLE HERE IS MY SPOUT")` should return "Here Is My Handle Here Is My Spout".

```js
function titleCase(str) {
    var arr = str.split(" ");
    arr = arr.map(function(elem) {
        return elem[0].toUpperCase() + elem.substr(1).toLowerCase();
    });
    str = arr.join(" ");
    return str;
}

titleCase("I'm a little tea pot");
```

```js
function titleCase(str) {
    return str.toLowerCase().replace(/\b([\w|']+)\b/g, function(word) {
        return word.replace(word.charAt(0), word.charAt(0).toUpperCase());
    });
}

titleCase("I'm a little tea pot");
```
