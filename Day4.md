# Reduce as a method

## Const

A constant defined to a data type stored by val are immutable.

```JavaScript
const testData = 'test';
testData = 'Data';
```

> This throws a type error because we are trying to change the value of testData and since const are immutable, it creates a conflict.

However, when a const points to a data type by reference, the data type can still be modified. Objects are stored by refrence and arrays are a subset of objects.

```JavaScript
const testData = ['test'],
testData[0] = 'Data';
```

> This works perfectly fine, since the refence of the data isn't being changed the program has no problems with us mutating the array.
___

## Reduce

### Using reduce to filter and map at once

This is a function filters the array for the condition `num % 2` i.e. `not divisible by 2` then maps a function of `num * 3` on the values that satisfy the condition.

```JavaScript
const arr = [1,2,3,4,5,6,7,8,9,10];

let count = 0;

const c = arr.reduce(function (acc, num) {
    console.log(++count);
    if(num % 2) acc.push(num * 3);
    return acc;
}, []/*This is the initial value of the acc*/)
```

    returns: [3,9,15,21,27]

### Using reduce for a tally function

This is a function that tallys the occurance of an array entry.

```JavaScript
const desserts = ['cake', 'ice cream', 'cookies', 'cake', 'ice cream', 'cake'];

const votes = desserts.reduce(function (acc, dessert) {
    if(acc.hasOwnProperty(dessert)) acc[dessert]++;
    else acc[dessert] = 1;
    return acc;
}, {})
```

    returns: { cake: 3, ice cream: 2, cookies: 1 }

### Using reduce to flatten an array

This is a function that tallys the occurance of an array entry.

```JavaScript
const data = [[1,2,3],[4,5,6],[7,8,9]];

const flat = data.reduce(function (acc, array) {
    return acc.concat(array);
}, [])
```

    returns: [1,2,3,4,5,6,7,8,9]

