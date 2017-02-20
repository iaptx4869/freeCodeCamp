#### Convert HTML Entities

------

Convert the characters `&`, `<`, `>`, `"` (double quote), and `'` (apostrophe), in a string to their corresponding HTML entities.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Try to pair program. Write your own code.

Here are some helpful links:

- [RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

- [HTML Entities](http://dev.w3.org/html5/html-author/charref)

- [String.prototype.replace()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace)

`convertHTML("Dolce & Gabbana")` should return `Dolce &amp; Gabbana`.

`convertHTML("Hamburgers < Pizza < Tacos")` should return`Hamburgers &​lt; Pizza &​lt; Tacos`.

`convertHTML("Sixty > twelve")` should return `Sixty &​gt; twelve`.

`convertHTML('Stuff in "quotation marks"')` should return`Stuff in &​quot;quotation marks&​quot;`.

`convertHTML("Shindler's List")` should return `Shindler&​apos;s List`.

`convertHTML("<>")` should return `&​lt;&​gt;`.

`convertHTML("abc")` should return `abc`.

```js
function convertHTML(str) {
    // &colon;&rpar;
    str = str.replace(/[&]/g, "&amp;").replace(/[<]/g, "&lt;").replace(/[>]/g, "&gt;")
        .replace(/["]/g, "&quot;").replace(/[']/g, "&apos;");
    return str;
}

convertHTML("Dolce & Gabbana");
```
