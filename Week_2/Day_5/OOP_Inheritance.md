# OOP- Inheritance

Code redundancy can also occur with classes.
- Multiple classes can share similar properties/methods

Use **inheritance** to build class based on an existing class.
- A general class can be declared with the *shared* information and the more specific classes can **extend** this general class

General Class (`Person`)                -->  **superclass**

Specific Class (`Student` or `Mentor`)  -->  **subclass**
- extentions of the superclass

```javascript
// General Class: This class represents all that is common between Student and Mentor
class Person {
  // moved here b/c it was identical
  constructor(name, quirkyFact) {
    this.name = name;
    this.quirkyFact = quirkyFact;
  }

  // moved here b/c it was identical
  bio() {
    return `My name is ${this.name} and here's my quirky fact: ${this.quirkyFact}`;
  }
}
```

```javascript
// Specific Class: pulls the data from the Person class and adds own specific properties/methods
class Student extends Person {
  // stays in Student class since it's specific to students only
  enroll(cohort) {
    this.cohort = cohort;
  }
}

class Mentor extends Person {
  // specific to mentors
  goOnShift() {
    this.onShift = true;
  }

  // specific to mentors
  goOffShift() {
    this.onShift = false;
  }
}
```