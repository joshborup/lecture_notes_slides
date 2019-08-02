# Array Methods

- Student can use the array map method.
- Student can use the array filter method.
- Student can use the array reduce method.
- Student can use the array forEach method.

# Objects

- Student can use delete to delete an object property.
- Student can use a for in loop to access property names and property values on an object.
- Student can use Object.assign() to create a new object.
- Student can use object destructuring to create new variables from an object.

# Spread Operator

- Student can use spread in function calls
- Student can use spread in array literals
- Student can use spread to concatenate arrays
- Student can use spread to make a copy of an array
- Student can use spread in object literals
- Student can use spread to make a copy of an object

# Nesting

- Student can build objects with objects and objects with arrays.
- Student can build an array of arrays and an array of objects.
- Student can nest for loops.

### **Review Callbacks**

A callback is simply a function that has been passed to another function as an argument to be invoked at a later time.

**Example:**

```js
// function to add numbers when called
function add(num1, num2) {
  return num1 + num2;
}

// function to subtract numbers when called
function subtract(num1, num2) {
  return num1 - num2;
}

// function to handle to callback invocation and passing in the numbers correct arguments
function evaluator(cb, num1, num2) {
  return cb(num1, num2);
}
```

**function to be used as a callback**

```js
function add5(element, index, array) {
  return element + 5;
}
```

**higher order function**

```js
// higher order function, takes a callback and enhances it
function myMapperFunction(cb, arr) {
  // new Mapped Array
  let mappedArray = [];
  // for loop to run on every element of the array
  for (let i = 0; i <= arr.length - 1; i++) {
    // declare the result and set it equal to the result of the callback function and the current element in the arrays forloop iteration passed in
    let result = cb(arr[i], i, arr);
    // push result to newMapped array
    mappedArray.push(result);
  }
  // return the result
  return mappedArray;
}
```

**function invocation with callback and array passed in**

```js
myMapperFunction(add5, myWordArray); // [1,2,3,4,5,6,7] => [6,7,8,9,10,11,12]
```

|    Type    |        for..in        | for..of             |
| :--------: | :-------------------: | ------------------- |
| Applies to | Enumerable Properties | Iterable Collection |
|   Object   |          yes          | no                  |
|   Arrays   |   yes, not advised    | yes                 |
|  Strings   |   yes, not advised    | yes                 |

**`Iterating`:** means repeating some steps

**`enumerating`:** going through all values in a collection of values
