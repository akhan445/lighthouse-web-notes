# Algorithms

**Algorithm**- set of instructions or steps to complete a task
- We tell the computer what to do by writing out the steps for it to complete a task

**Algorithmic Complexity** deals with how fast/slow a particular problem is.
- *Time is not a reliable* way to measure how long it takes for an algorithm to run. There are many factors that could influence how long it takes including things like teh computer's architecture, what language is being used, operating system etc

## **How to measure?** 

- Count the number of **elementary operations**. For example:
    - let number = 0;
    - number += 2;
    - console.log(number);

So if you perform `n` operations, then the running time is `n`.

***Each elementary operation takes a fixed amount of time to perform no matter what the data is.***

    number1 + number2; // running time = 1

For a simple for loop problem:

```javascript

let result = 0;

for (let i = 0; i < array.length; i++) {
  let number = array[i];
  result += number;
}

console.log(result);

/*************************** Analyze below ***************************/

let result = 0; // 1

for (
  let i = 0; // 1
  i < array.length; // n + 1
  i++ // n
) {

  let number = array[i]; // n
  result += number; // n
}

console.log(result); // 1
```

Some operations are fixed while other are depeendant on the size of the array. If array is size `n`, then array will call for loop `n` times.


|        1             |        n             |       	n + 1         |
|:--------------------:|:--------------------:|:---------------------:|
| let result = 0;      | i++	                | i < array.length;     |
| let i = 0;	let      | number = array[i];   |	_                     |
| console.log(result); | result += number;	  | _                     |

Total = `3 + (n * 3) + n - 1` = `4 + (n * 4)`

## **Constant operations**

When looking at algorithmic run time, we are concerned with the **worst case scenario**

Certain algorithms are always the same no matter how many inputs you have. runtime = **O (1)**

Some examples:
  - check if last element is ... --> just jump to end of array
  - how many people in array     --> just return length

## **Linear and Binary Search**

**Linear algorithms**- the run time is proportional to the input size. When you add one extra element to input, the number of operations will increase by constant amount. runtime = **O (n)**

Some examples:
  - linear search
  - count even numbers in array

**Logarithmic algorithms**- The number of operations is directly proportional to the logarithm of the size of the input. These algorithms cut the problem in half at each "iteration" so the relationship is logarithmic. runtime = **O (log n)**

Some exmples:
  - binary search

Both linear and binary search only work for **sorted/ordered data**.

![linear-vs-binary](https://i.imgur.com/qU0Euzx.png)

## **Quadractic Time**

Quadratic are usually seen in nested loops. As n grows, the run time grows exponentially. runtime = **O (n^2)**

For a triple nested loops the runtime grows even faster, making it cubic. runtime = **O (n^3)**

Some examples:
  - find all duplicates in array
  - find the first unique number in array
  - 

Keep in mind however, looping over the same array is necessary to get this.

```javascript
// Same Array
for (let i = 0; i < array.length; i++) {
  console.log(array[i]); // n
  for (let ii = 0; ii < array.length; ii++) {
    console.log(array[ii]); // n^2
  }
}

// different arrays
for (let i = 0; i < arrayA.length; i++) {
  console.log(arrayA[i]); // a
  for (let ii = 0; ii < arrayB.length; ii++) {
    console.log(arrayB[ii]); // a*b
  }
}
```

![linear-vs=quadractic-vs-cubic](https://i.imgur.com/AAmzk1h.png)

## **Big O Notation**

Denoted using the **O ( )** to represent the algorithmic runtime.

3 main things to consider:
1. Only care about arbitrary **large inputs**
    - Smaller inputs make it difficult to determine which algorithms are faster. Sometimes slower algorithms have a faster runtime for smaller `n` inputs. Also, smaller number of operations are not a big deal for a computer so we care about performance when the `n` is large enough to make a difference.
2. Drop the **non-dominant terms**
    - For a runtime of `n^2 + 1000n` we can see below that for a large input the `1000n` doesn't make a difference because the more dominant term is growing a lot faster. When it comes to Big O, only worry about the highest order term.
    - `n^2 + 1000n` = O (n^2)
    - ![non-dominant-terms-example](https://i.imgur.com/gEqddpZ.png)
3. Drop **constants**
    - Just like non-dominants, constants also don't make a difference. They only affect the runtime by a constant amount when we actually care about how **complexity grows relative to input**.

![time-complexity](https://i.imgur.com/WmFTz0a.png)
