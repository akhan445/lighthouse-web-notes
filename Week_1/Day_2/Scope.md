# Scope in Javascript

There are two levels of scope: global & local

## **Global Scope**
----
- Available anywhere in the code

## **Local Scope**
----
- only available within the function in which it's defined
- It's ideal to not access global variables within functions. Instead you should [***pass the data in as a parameter/argument to the function***](Functions.md#best-practice)
    - WHY? Makes code more reusable since they are less dependant on outer/surrounding scope
- **ReferenceError:** when you try to access variable outside its scope