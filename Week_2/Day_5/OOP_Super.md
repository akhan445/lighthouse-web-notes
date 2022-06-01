# OOP- Super

## **Method Overriding**

Sometimes when inheriting, subclass might want to tweak/implement methods slightly different then how it is implemented in superclass.
- **Method overriding** allows you to declare methods from superclass in subclass and alter the behavior.
  - This overrides the superclass's method and when a call is made on method the subclass's method is implemented

```javascript
class Person { //superclass
  // ...
  bio() {
    return `My name is ${this.name} and here's my quirky fact: ${this.quirkyFact}`;
  }
}

class Mentor { // subclass

  // Method ovverriding
  bio() {
    return `I am a mentor. My name is ${this.name} and here's my quirky fact: ${this.quirkyFact}`;
  }
}
```

*THERE IS A BETTER WAY TO DO THIS*
- There is still duplication of code
- Method overriding might work better wehn your implementation of the method will be different than superclass's
    - Since the implementation are similar we can use `super`

## **`super`**

`super` further allows code re-use by giving subclass the ability to reference the parent class.
- We can just call the parent's bio method in our overridden method

```javascript
class Mentor {

  bio() {
    return `I am a mentor. ${super.bio()}`;
  }
}
