## Check type of input

### Primitive data types (except Null)

```JavaScript
typeOf('testInput') === 'data type';
```

### Function

```JavaScript
typeOf('testInput') === 'function';
```

### Objects

```JavaScript
typeOf('testInput') === 'object';
```

> Note that `Array` and `Null` return true as they are subsets of objects.

### Arrays

```JavaScript
Array.isArray('testInput');
```