# JavaScript Array Methods

## 1. Mutator Methods (modify the array)

- **push()**: Adds one or more elements to the end of an array and returns the new length of the array.
```
let arr = [1, 2, 3];
  arr.push(4); // arr is now [1, 2, 3, 4]
  
```
- **pop()**: Removes the last element from an array and returns that element.
```
let arr = [1, 2, 3];
let lastElement = arr.pop();
 // lastElement is 3, arr is now [1, 2]

```
- **shift()**: Removes the first element from an array and returns that element.
```
let arr = [1, 2, 3];
let firstElement = arr.shift(); 
// firstElement is 1, arr is now [2, 3]

```
- **unshift()**: Adds one or more elements to the beginning of an array and returns the new length of the array.
```
let arr = [1, 2, 3];
arr.unshift(0); 
// arr is now [0, 1, 2, 3]
```
- **splice()**: Changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.
```
let arr = [1, 2, 3, 4];
arr.splice(1, 2, 'a', 'b');
 // arr is now [1, 'a', 'b', 4]
```
- **sort()**: Sorts the elements of an array in place and returns the sorted array.
```
let arr = [3, 1, 4, 2];
arr.sort();
 // arr is now [1, 2, 3, 4]
```
- **reverse()**: Reverses the elements of an array in place.
```
let arr = [1, 2, 3];
arr.reverse(); // arr is now [3, 2, 1]
```
- **fill()**: Fills all the elements of an array from a start index to an end index with a static value.
```
let arr = [1, 2, 3];
arr.fill(0); // arr is now [0, 0, 0]
```
- **copyWithin()**: Shallow copies part of an array to another location in the same array and returns it, without modifying its size.
```
let arr = [1, 2, 3, 4];
arr.copyWithin(0, 2); // arr is now [3, 4, 3, 4]
```
## 2. Accessor Methods (do not modify the array)

- **concat()**: Merges two or more arrays and returns a new array.
```
let arr1 = [1, 2];
let arr2 = [3, 4];
let newArr = arr1.concat(arr2); // newArr is [1, 2, 3, 4]
```
- **includes()**: Determines whether an array includes a certain value among its entries.
```
let arr = [1, 2, 3];
let hasTwo = arr.includes(2); // hasTwo is true
```
- **indexOf()**: Returns the first index at which a given element can be found in the array, or -1 if it is not present.
```
let arr = [1, 2, 3];
let index = arr.indexOf(2); // index is 1
```
- **lastIndexOf()**: Returns the last index at which a given element can be found in the array, or -1 if it is not present.
```
let arr = [1, 2, 3, 2];
let lastIndex = arr.lastIndexOf(2); // lastIndex is 3
```
- **slice()**: Returns a shallow copy of a portion of an array into a new array object.
```
let arr = [1, 2, 3, 4];
let newArr = arr.slice(1, 3); // newArr is [2, 3]
```
- **join()**: Joins all elements of an array into a string.
```
let arr = [1, 2, 3];
let str = arr.join('-'); // str is '1-2-3'
```
- **map()**: Creates a new array with the results of calling a provided function on every element in the calling array.
```
let arr = [1, 2, 3];
let newArr = arr.map(x => x * 2); // newArr is [2, 4, 6]
```
- **filter()**: Creates a new array with all elements that pass the test implemented by the provided function.
```
let arr = [1, 2, 3, 4];
let newArr = arr.filter(x => x > 2); // newArr is [3, 4]
```
- **forEach()**: Executes a provided function once for each array element.
```
let arr = [1, 2, 3];
arr.forEach(x => console.log(x)); // logs 1, 2, 3
```
- **reduce()**: Executes a reducer function on each element of the array, resulting in a single output value.
```
let arr = [1, 2, 3];
let sum = arr.reduce((acc, x) => acc + x, 0); // sum is 6
```
- **reduceRight()**: Applies a function against an accumulator and each element in the array (from right to left) to reduce it to a single value.
```
let arr = [1, 2, 3];
let sum = arr.reduceRight((acc, x) => acc + x, 0); // sum is 6
```
- **some()**: Tests whether at least one element in the array passes the test implemented by the provided function.
```
let arr = [1, 2, 3];
let hasEven = arr.some(x => x % 2 === 0); // hasEven is true
```
- **every()**: Tests whether all elements in the array pass the test implemented by the provided function.
```
let arr = [1, 2, 3];
let allEven = arr.every(x => x % 2 === 0); // allEven is false
```
- **find()**: Returns the value of the first element in the provided array that satisfies the provided testing function.
```
let arr = [1, 2, 3];
let found = arr.find(x => x > 1); // found is 2
```
- **findIndex()**: Returns the index of the first element in the array that satisfies the provided testing function.
```
let arr = [1, 2, 3];
let index = arr.findIndex(x => x > 1); // index is 1
```
- **flat()**: Creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.
```
let arr = [1, [2, 3], [4]];
let newArr = arr.flat(); // newArr is [1, 2, 3, 4]
```
- **flatMap()**: First maps each element using a mapping function, then flattens the result into a new array.
```
let arr = [1, 2, 3];
let newArr = arr.flatMap(x => [x, x * 2]); // newArr is [1, 2, 2, 4, 3, 6]
```

## 3. Array Properties
\
- **length**: Returns the number of elements in the array.
```
let arr = [1, 2, 3];
let len = arr.length; // len is 3
```
- **prototype**: Allows you to add new properties or methods to the Array object.
```
Array.prototype.sayHello = function() {
    console.log("Hello!");
};

let arr = [1, 2, 3];
arr.sayHello(); // logs 'Hello!'

```
