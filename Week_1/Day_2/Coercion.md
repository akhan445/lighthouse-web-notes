# Coercion and Truthy/Falsey

## **Double Equals, Triple Equals, and Type Coercion**

`=== or !==` compares *value and type*
- Compares type then actual values- short circuit on type!

  ```javascript
  23 === "23" // false
  ```

`== or !=` compares only *value*
- Before comparison will *force two values to be same type, if possible*-  (This is **Type Coercion**)
  ```javascript
  23 == "23" // true
  ```

## Truthy and Falsey

In Javascript, everything has an inherent `Boolean` value (`Truthy` & `Falsey`)
6 that are Falsey:
```javascript
1. false        // false is false is false

2. 0            // only Falsey number

3. ""           // empty string

4. null         // null or empty value

5. undefined    // object that has not been defined

6. NaN          // not a number

```

Here is a summary of true/false values when using `===` and `==`

<img src="https://i.stack.imgur.com/yISob.png" width="70%">

https://stackoverflow.com/questions/359494/which-equals-operator-vs-should-be-used-in-javascript-comparisons/359509#359509
