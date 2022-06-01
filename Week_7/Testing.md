# Testing

Manual testing is what's most familiar and is one way to test code. However, as projects grow more methods need to be adopted for testing to ensure the application is working well since we cannot simply rely on manual testing.

#### Some important points about testing:
- Testing is **repetitive work** which is why it is perfect to automate the process.

- Testing also allows us to **gain confidence in our code**.

- Ensures code is besing testing consisternly after applying changes.

**Regression testing** is the process of verifying the previously uncovered bugs have not returned all subsequent versions of the software

## Types of testing

Before you use a testing strategy like unit or integration testing, it is a good idea to having **statc code analyzers** (eslint, flow) that cover some basic testing features.

There are 4 categories of testing:
1. Static
2. Unit
3. Integration
4. End-to-End (E2E)

As we move down the list the **cost and time required** increases.

**Static**
- some initial configuation required, but very little maintenance
- integrated into code editor and provides immediate feedback
- Two common ones are static typing and linting (Prettier, eslint)
    - ***eslint*** -> identifies issued due to code inconsistency, but is more appropriate to enforce rules that identify code errors
    - ***prettier*** -> formats code into single consistent style
- You can also use a superset of JS for static type checking (Typescript and Flow)

**Unit**
- Goal with unti testing is to test a specific function or componenet in isolation
- focus on one, small consistent piece of code to gain confidence that it will work as expected

**Integration**
- **integration** is when you combine different units of code to create an application
- **integration testing** is testing whether two or more units of code work together (Jest)

**End-to-End**
- most expensive and most comprehensive (Cypress)
-  Goal is to get as close to simulated user behavior as possible 
- Simulate the behaviour by loading browser and testing, however to do so manually would take longer

#### How much to test code?

There is no set amount that one should test, it really depends on the project and its requirements. This diagram provides a framework that can be used:

![testing-trophy](https://www.datocms-assets.com/22029/1595597110-testingtrophy.png)


### What you should do in summary
1. Write test- Certain should be automated
2. Not too many, you don't need 100% coverage to ensure confidence
3. Most **integration**. Integration tests = more thorough, test how different parts of application work together

