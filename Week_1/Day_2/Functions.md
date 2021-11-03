# Functions

## **Best Practices**
---
1. Gives functions ***precise*** verb/action based names
2. Use ***camelCasedNames***
3. Properly ***indent*** function code
4. Each function should focus on a ***single task***. Either:
      - return a value
      - cause a side effect (i.e log a message)
5. Ideal for functions to try to avoid reading outer scope variables. If function needs some information, ***it should be passed to function as a parameter***

## **Functions**
---
<br>

### **Declarative Function**
```javascript
function foo() {
  return 'bar'
}
```

### **Expression Function**
```javascript
const foo = function() {
  return 'bar';
}

// OR es6
const foo = () => 'bar'; // one line return
```
### **High Order Function and Callbacks**
- A function that takes a function as a parameter
- A callback is a function that is passed into another function as an argument
```javascript
// high order function
const map = (arr, cb) => {
  let result = [];
  for (let element of arr) {
    result.push(cb(element));
  }
  return result;
}

const arr = [1,2,3,4,5,6,7,8,9];
                     // callack function
console.log(map(arr, (x) => x * 2));
//2,4,6,8,10,12...
```
