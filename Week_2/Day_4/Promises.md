# Promises

A **promise** represents the eventual result of an asynchronous operation.
- Primary way of interacting through promise is through `then` method

`then` method registers callbacks to recieve either a promise's eventual value or the reason why the promise cannot be fulfilled.

Promises are:
- objects
- don't rely on anything other than basic Javascript
- As of ES6, Promises are built into the JS language

Promises also make:
- error handling much simpler
- asynchronous code easier to unit test

`Promise.all` can be used to run multiple async operations in paralleland have a single callback to see all the results  together