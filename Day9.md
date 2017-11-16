# Closure

Closure means to remember where a piece of code was intanciated hence aligning with the rules of its parent scope.

```js
function createMultiplier (m) {
  return function (n) {
    return m * n;
  }
}
```

    const double = createMultiplier(2);
    const triple = createMultiplier(3);

    double(5) *returns* 10
    triple(5) *returns* 15

This happens because the function assigned to double and triple apply closure to their m value. When double was defined, ***m was 2***, when triple was defined, ***m was 3*** so when they are called later with an `n of 5`, they apply closure and use the value of m when they were defined.