# Object Oriented Programming

```js
function createUser(name){
  const user = {
    name: name;
    sayName: function () {
      console.log('Hello, my name is '+ user.name);
    }
  }
  return user;
}

const mauro = createUser('Mauro')
const sam = createUser('Sam')

mauro.sayName(); // logs: Hello, my name is Mauro;
sam.sayName(); // logs: Hello, my name is Sam;
console.log(sam.sayName() === mauro.sayName()); // logs: false;
```

> The this keyword in JavaScript represents the context the function is caused.

## Functional Sharing

```js
function createUser(name){
  const user = {
    name: name;
    sayName: sayName;
  }
  return user;
}

function sayName () {
    console.log('Hello, my name is '+ this.name);
}

const mauro = createUser('Mauro')
const sam = createUser('Sam')

mauro.sayName(); // logs: Hello, my name is Mauro;
sam.sayName(); // logs: Hello, my name is Sam;
console.log(sam.sayName() === mauro.sayName()); // logs: true;
```

By sharing the sayName function, we do not create this function needlessly when a new user is intanciated.

## Explicit Binding

```js
function createUser(name){
  const user = {
    name: name;
    sayName: sayName;
  }
  return user;
}

function sayName () {
    console.log('Hello, my name is '+ this.name);
}

const jonny = {name: 'Jonny'}

sayName.call(jonny); // logs: Hello, my name is Jonny;
```