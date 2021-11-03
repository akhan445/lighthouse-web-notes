# Asynchronous Control Flow

Usually code behaves in a sequential/linear manner. Top to bottom and as functions get called, jumps to the functions, executes them and then returns back to function call and to continue.

This is important to know because JavaScript runs in a single thread, so it can only do one operation at a time.
- Avoid blocking that thread whenever possible.

Review function types from Week 1 [here](/Week_1/Day_2/Functions.md#Functions).

## **Async vs Sync**

The main difference is that in synchronous programming, the main thread would wait (**idle** or **blocked**) despite having other tasks to complete.

Sync
- Start Task1, wait to complete, start Task2, wait complete...

Async 
- Start Task1, go do something else, come back when finished and complete Task1

## **Asynchronous Programming**

Asynchronous behavior is when things occur out of order.

***Asynchronous Programming*** is when a unit of work performs outside the main thread and notifies the program upon completion.

In JS, this is usually for longer tasks such as reading a file, waiting for input, getting information from a server.
- Main program thread continues to run while these tasks are pushed to an event queue (event loop).
  - The event loop is handled by the engine that runs JS (node , V8, etc …). These engines are multithreaded and will run those functions in parallel.
- Once the main thread finishes, then it goes back and checks the event queue for finished tasks and executes them.

![eventLoop](https://i.stack.imgur.com/BTm1H.png)

## **How does JavaScript perform asynchronously??**

Through asynchronous **callback functions**

```javascript
const fs = require("fs");

console.log('BEFORE writeFile call');

fs.writeFile("./test_async.txt", "h3ll0 file!\n", (error) => {
  if (error) {
    // Handle error
    console.log("Failed to write to file");
    return;
  }
  // Success!
  console.log("Successfully wrote to file");
});

console.log('AFTER writeFile call');

// BEFORE message
// AFTER message
// Success/Fail..
```

Downside to Asynchronous programming is you lose the ability to know order of tasks being completed. You don't know how long tasks could take to complete so the order could be different than intended.
- Nested callbacks is how you control the flow. Below waits till each task is completed before moving on!

```javascript
const fs = require("fs");

fs.readFile("file1.txt", () => {
  fs.readFile("file1.txt", () => {
    fs.readFile("file1.txt", () => {
        ....
    })
  })
})
```