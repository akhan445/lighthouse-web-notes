# Data Structures

`undefined`, `Boolean`, `Number`, `String`, `BigInt`, `Symbol` are **data types**.

`Object`, `Array`, `Date`, `Map` are **structural types**.
- Array, Date and Map are constructed from `Object` type so are **substructes** of `Object` type.

## **Arrays vs Objects**

When to use which

***Arrays*** should be used when:
- Order is important
- Collection items are *independant*
- When you need to access elements by index (first, last, middle etc)
- **CONS**
    - reading/modifying elements that are not first or last (You have to perform search then manipulate the data)

***Objects*** should be used when:
- information stored is *related*
- order is not important
- need to access elements frequently

## **Complex Data Structures**

**Objects containing arrays, storing strings**
```js
{
  carbonSteel:    ["1084","1075","80CrV2"],
  stainlessSteel: ["S30V", "420HC"]  
}
```

**Array of objects**
```js
[
   {
    name:  "Dainton Markham",
    email: "d.markham@mail.com"
  },
  {
    name:  "Heidi Dalton",
    email: "heidi.d@mail.com"
  }
]
```

**Object of objects with ids as keys for quick access**
```js
{
    "MURB090909": {
      name: "Buddy Murillo",
      studentId: "MURB090909",
      numberOfClasses: 2
    },
    "TAND060606": {
      name: "Dilan Tanner",
      studentId: "TAND060606",
      numberOfClasses: 5
    },
    "SKIS424242": {
      name: "Sophia Skinner",
      studentId: "SKIS424242",
      numberOfClasses: 1
    },
    "HALA101010": {
      name: "Antony Hale",
      studentId: "HALA101010",
      numberOfClasses: 0
    }
  }
```


