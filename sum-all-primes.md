#### Sum All Primes

------

Sum all the prime numbers up to and including the provided number.

A prime number is defined as a number greater than one and having only two divisors, one and itself. For example, 2 is a prime number because it's only divisible by one and two.

The provided number may not be a prime.

Remember to use [Read-Search-Ask](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help) if you get stuck. Try to pair program. Write your own code.

Here are some helpful links:

- [For Loops](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for)

- [Array.prototype.push()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)

`sumPrimes(10)` should return a number.

`sumPrimes(10)` should return 17.

`sumPrimes(977)` should return 73156.

```js
function sumPrimes(num) {
    var arr = [];
    var ifPrime = function(num) {
        if (num < 2) {
            return false;
        }
        if (num === 2) {
            return true;
        }
        if (num % 2 === 0) {
            return false;
        }
        for (var i = 3; i <= Math.sqrt(num); i += 2) {
            if (num % i === 0) {
                return false;
            }
        }
        return true;
    };
    for (var i = 2; i <= num; i++) {
        if (ifPrime(i)) {
            arr.push(i);
        }
    }
    return arr.reduce(function(prev, cur, index, array) {
        return prev + cur;
    }, 0);
}

sumPrimes(10);
```
