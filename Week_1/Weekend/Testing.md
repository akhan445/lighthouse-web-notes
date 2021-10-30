# Testing

   ### ***1. Unit Testing (CODE testing)***

  - testing small piecs of code (individual units of code like functions)
    - isolated from other components
  - simple to write --> so lots of them
  - great for preventing **regressions**- bugs that occur repeatedly
  - Testing using Mocha, Jasmine and Tape

### ***2. Integration Testing (CODE testing)***

  - testing how parts of a system work together
    - **NOT** isolated. i.e Testing code accessing database
  - usually more complex & hence slower than unit tests and testing involves seperate systems working together
  - same tools as unit testing

### ***3. Functional Testing (UI testing)***

  - aka E2E testing, browser testing
  - testing the complete functionality of application
    - user accesing application
  - very few in number usually
  - Selenium, PhantomJS or CasperJS

***

### The Happy Path
- path through the system where everything works
- Don't test the happy path- diverge ('wander the weeds') and test and try to think of various scenarios where your code will crash
  

