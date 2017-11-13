# Recursion - 101

The first thing to deal with when writing a recursive function is the `base case`. This is where the function will end and without it the function will continue forever or till the stack overflows.

```JavaScript
function exponential (n, pow) {
    // base case
    if (pow === 0) return 1;
}
```

The `recursive case` is what a function recursive, this is where the function calls itself with modified arguments.

```JavaScript
function exponential (n, pow) {
    // base case
    if (pow === 0) return 1;
    // recursive case
    return n * exponential(n, pow - 1);
}
```

A recursive function will continue inwards until it hits its `base case` then it unfolds outwards from the base case.

    The example above works as:
    exponential(2, 4)

    2 * exponential(2, 3)
        2 * exponential(2, 2)
            2 * exponential(2, 1)
                2 * exponential(2, 0) => base case
                2 * 1 = 2
            2 * 2 = 4
        2 * 4 = 8
    2 * 8 = 16

    returns 16.
