# Errors

Errors are common part of the developer's world. Being comfortable with them is important as you will encounter them a lot. Below are a few common error types.

## **Syntax Errors**
---

This is what a common syntax error generally looks like, let's break it down:

```
node syntax-error.js
/vagrant/w1d2/syntax-error.js:4
console.log(rank name);
                 ^^^^
SyntaxError: Unexpected identifier
    at exports.runInThisContext (vm.js:73:16)
    at Module._compile (module.js:443:25)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3
```

The first line gives details on what file and the `4` tells us what line in the code caused the error

-     /vagrant/w1d2/syntax-error.js:4

The next bit highlights what part of code caused the error

-     console.log(rank name);
                     ^^^^
      SyntaxError: Unexpected identifier

The Last part is known as the **stack trace**

-     at exports.runInThisContext (vm.js:73:16)
      at Module._compile (module.js:443:25)
      at Object.Module._extensions..js (module.js:478:10)
      at Module.load (module.js:355:32)
      at Function.Module._load (module.js:310:12)
      at Function.Module.runMain (module.js:501:10)
      at startup (node.js:129:16)
      at node.js:814:3

## **Reference Errors**
----
These occur when you are trying to access the value of a variable that does not exist
```javascript
var firstName = "Jane";
var lastName = "Doe";

console.log(firstName, lasName); // lasName does not exist
```
## **Type Errors**
----
Represents an error when an operation could not be performed. Typically it is when a value is not of an expected type
```javascript
var favouriteMeal = "BREAKFAST";

console.log(favouriteMeal.toLower());
```

```
node type-error.js
/vagrant/w1d2/type-error.js:3
console.log(favouriteMeal.toLower());
                          ^
TypeError: undefined is not a function
    at Object.<anonymous> (/vagrant/w1d2/type-error.js:3:27)
    at Module._compile (module.js:460:26)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3
```