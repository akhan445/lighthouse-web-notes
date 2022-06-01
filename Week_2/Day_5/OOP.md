# Object Oriented Programming

**Object Oriented Programming** one of the most popular programming paradigms in software development.

**Functional Programming** is a programming paradigm where programs are constructed by applying and composing functions.

Goals of OOP:
- code organization
- re-use
- modularity

JavaScript popularized functional programming but is also object oriented.
- JavaScript is not strictly OO like Java or Ruby


| OOP Languages | Functional Programming Languages |
|:--------------|:---------------------------------|
| Java          | Erlang                           |
| Python        | Common Lisp                      |
| C++           | Elixir                           |
| C#            | Clojure                          |
| Objective-C   | Erlang                           |
| Swift         |                                  |
| Ruby          |                                  |
| PHP           |                                  |


## OOP in JavaScript

In JS, you use objects to group related variables and functions together to keep code organized.

An object is a little bundle of information, also known as `state`.
- each property can represent the **state** of that object
- property that has value as function is called **method**
    - method represents behaviour

In addition to state, object also can do stuff (behaviour).
- method can modify the object, ask method for information etc

Everything related to dog --> in dog object
```javascript
const dog = {
  sound: "woof", //property
  dogBreed: "shih tzu",
  speak: function() { // method
    console.log(`${this.dogBreed} says ${this.dogSound}`);
  }
};
```

## **`this`**

`this` is a keyword in JS.

`this` means nothing without context. The value of `this` is determined at the time of the call and depends where and how it was called.

**`this` refers to the object that the method was called on**

```javascript
const dog = {
  sound: "woof",
  speak: function() {
    console.log(this.sound);
  },
  teachMeSomething: function() {
    if (dog === this) {
      console.log('dog === this');
    }
    this.speak();
  }
};

dog.teachMeSomething();
```





