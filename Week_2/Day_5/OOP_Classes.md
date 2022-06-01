# OOP- Classes and Instances

Classes are blueprints.
- Blueprint is the **template** for creating the object
    - Gives you all the instruction needed but is not the actual object (like a guide)

You use the blueprints to create the objects and those are called **instances** of t*he object.
- every instance is a *unique* object derived from the blueprint (class)

![classes-and-objects](https://i.imgur.com/n4NnXSL.png)

### ***Methods and Properties***

use `class` to declare a new class

```javascript
// Declare a class
class Pizza {
  // Every object will start off with cheese
  constructor() {
    this.toppings = ["cheese"]; // Creating a property, just use this
  }

  // Creating methods
  methodName(parameters) {
    // this is a method
  }

  addTopping(topping) {
    this.toppings.push(topping);
  }
}

// Create instance of a class
let pizza1 = new Pizza();
let pizza2 = new Pizza();

pizza.addTopiing("pepperoni"); // calling method on object
```

### ***Constructor***

This is a special method which gets executed **when an object instance is created**.
- happens when you call `new Pizza()`
- these are the default values on an object
- every class can take **ONE** `constructor` method

The new instance of the object `Pizza` behaves like this:
- uses Classes just allows us to DRY up our code

```javascript
const pizza1 = {
  toppings: ["cheese"],
  addTopping: function(topping) {
    this.toppings.push(topping);
  }
}
```

### ***Primitives as Objects***

Each primitive (excluding `symbol`) has a corresponding object constructor.

```javascript
typeof(true); 
// "boolean" 
typeof(Boolean(true)); 
// => "boolean" 
typeof(new Boolean(true));
// => "object"
```

Using the `new` invokes a object constructor and creates a unique object.
- Compaing this with identical looking primitives will yield a falsey value
  
  ```javascript
  const greeting = "Hello, world!" 
  const objGreeting = new String("Hello, world!");

  greeting == objGreeting; 
  // => true

  greeting === objGreeting; 
  // => false
  ```

## **Getters and Setters**

Getters and setters are special methods that are used to get/set values of a property.

```javascript
class Pizza {

  // ...

  setSize(size) {
    this.size = size;
  }
  getSize() {
    return this.size;
  }
}

// DRIVER CODE
const pizza = new Pizza();
pizza.setSize('m');
pizza.getSize(); // m
```

### ***Why do this?***

One might think this is unnecessary because you can just access the property directly.

Benefits of doing it this way:
1. Validating data before assigning to a property
    - i.e `setSize()` --> you can check to make sure it's a valid size (`s`, `m`, `l`) before setting it
    ```javascript
    setSize(size) {
    if (size === 's' || size === 'm' || size === 'l') {
      this.size = size;
    }

    ```
2. Computing a value on the fly instead of simply pulling it out of property
    - i.e if price of pizza keeps changing (adding/removing topping, changing size etc..) you need to calculate the price and update it everytime you change something but through designated method you can simply **calculate when needed**
    ```javascript
    getPrice() {
      const basePrice = 10;
      const toppingPrice = 2;
      return basePrice + (this.toppings.length * toppingPrice);
    }
    ```

### `get` ***and*** `set` ***keywords***

Since these are common conventions, js allows you to use `get` and `set` to implement getters and setters easily.
- the property has to be different name then the setter/getter
- JS allows you to access them as properties instead of methods

```javascript
class Pizza {
  // ...

  get price() {
    // ...
  }

  set size(size) {
    // ...
  }
}

// DRIVER 
let pizza = new Pizza();

pizza.price;      // instead of getPrice()
pizza.size = 's'; // instead of setSize(size)
```
