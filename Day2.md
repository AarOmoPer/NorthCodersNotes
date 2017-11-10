# Array Methods

* ```.forEach(function(){});```
    * This iterates over the array and executes the function for all populated indices of the array.
* ```.map(function(){});``` 
    * This creates a new array containing a function manipulated value of the same index
* ```.filter(function(){});``` 
    * This creates a new array containing a function manipulated value of the same index
* ```.some(function(){});``` 
    * This returns true if **SOME** of the values in the array meet the function's requirements
* ```.every(function(){});``` 
    * This returns true if **ALL** of the values in the array meet the function's requirements

## Useful Methods 

* ```.includes('<string>')```
* ```.split('<split character>')[<array index>]```

# Debugging

### Bugs 
Bugs occur when a piece of code doesn't act as expected usually due to logical error.
### Errors
These occur when there is a problem stopping the code from being executed at all. JavaScript terminal error output is a good resource for determining where an error has occured.
* Reference Error : 
    * These are errors that arise from referencing values that are not defined.
    * These are *run-time* errors, therefore only surface when the line of code is run.
* Syntax Error :
    * These errors are found before the code is run during compilation and can be easily fixed beforehand.
* Type Error :
    * This is also a *run-time* error, therefore happens during code execution.
    * This error occurs when a value is being refered to or used as a _type_ that it is not.



