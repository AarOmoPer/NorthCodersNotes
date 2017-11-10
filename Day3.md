# Reference and Value

    The six primitive data types are :
    * String
    * Boolean
    * Number
    * Undefined
    * Null
    * Symbol

> Primitive data types are stored by value and are immutable, however, objects are stored by reference and are mutable.

## Reference

```JavaScript
const nums = [1,2,3];
const threeNums = [1,2,3];
console.log(nums === threeNums)
```

prints `false` to console,

However,

```JavaScript
const nums = [1,2,3];
const threeNums = nums;
console.log(nums === threeNums)
```

 prints `true` to console,

> This is because two objects will only ever deeply equal each other when they reference the same data.


# Making a copy

### To copy an `array`, you use the

```JavaScript
let newArr = originalArr.slice()
```

### To copy an `object`, you use the

```JavaScript
let newObj = Object.assign({}, originalObj)
```

### To copy an `array of object`, you can use

```JavaScript
let sampleArray = [{...},{...}];

let newArray = sampleArray.map(function (object) {
    const newObject = Object.assign({}, object);
    return newObject
})
```

# Testing

## Unit testing

    Testing a single unit of code in isolation. This could be a single function.

An `assertion` checks a condition and only throws an error to the console when the condition is not met.

```JavaScript
console.assert(`condition`, <error message>)
```

### How to set up for testing

```Node
npm init

npm install --save mocha chai
```

`Exporting from source`

```JavaScript
module.export = {
    <function name>
}
```

`Writing test`

```JavaScript
const {/*testFunction*/} = require(/*Path*/);
const {expect} = require('chai');

describe('testFunction name', function() {
    it(/*'description of test'*/, function () {
     // AAA
     // arrange
     const testInput = '#', expected = '£';
     // act
     const actual = testFunction(testInput);
     //assert
     expect(actual).to.equal(expected);
     //.equal checks value .eql checks reference
    })
})
```
