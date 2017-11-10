# Function

## Types of functions

* Function Declaration

```JavaScript
function sum (num1, num2) {
  return num1 + num2;
}
```

* Function Expression

```JavaScript
// Named
var sum = function add (num1, num2) {
  return num1 + num2;
};

// Anonymous
var sum = function (num1, num2) {
  return num1 + num2;
};
```

## Impure function

An impure function is any function that relies on variables outside its scope. Due to uncertainty about the behaviour and value of variables outside a function's scope, it is inadvisible to rely on them within the function.

## Argument Object

Functions can be declared with no parameters if there is an uncertainty about how many arguments will be passed into the function.

```JavaScript
function addNums () {
    console.log(arguments)
}

addNums(1,1,1,1,1)
addNums(2)
```

    logs: { '0': 1, '1': 1, '2': 1, '3': 1, '4': 1 }

          { '0': 2, }

This returns an object with a argument position as a key and its value.

To change this format immediately to an array, we can use:

```JavaScript
const argsArray = [...arguments];
```

## Arrow Functions

Arrow functions look like this:

```JavaScript
const timesTwo = (n) => {
    return n * 2
}
```