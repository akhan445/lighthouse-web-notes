# Objects
- everything is javascript is an Object
- Object contain `key:value` pairs, each key maps to a value
  1. key is unique
  2. keys are strings (every key is interpreted as literal string)
  3. each key has exactly one value
- value can be anything
  ```javascript
  const myObject = {
    a: 6,     // Number
    b: "abc", // String
    c: true,  // Boolean
    d: null,  // Null
    "full name": "Abdullah Khan",
    nestedObject: {
      x: 1,
      y: 2,
      z: 3
    },
    someArray: [1, 2, 3, 4],
    aFunction: function() {
      return ...;
    }
  };
  ```
- Accessing items:
  ```javascript
  myObject.d //Dot notation
  myObject["a"] //Square bracket notation
  ```
  - use dot when you know the exact key
  - use square is preferred
      - you can use variables
      - you can use keys with spaces or numbers in them
  - to call function in Object: `aFunction()`
