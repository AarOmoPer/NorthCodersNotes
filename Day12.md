# Prototypes and Constructors

```js
function Person (name) {
  this.name = name;
}

const sam = new Person ('Sam');

console.log(sam intanceof Person;) // logs true

console.log(sam.constructor) // logs Function Person
```

A prototype exists to store all methods associated with a particular datatype.