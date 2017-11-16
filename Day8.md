# Scope

Scope refers to the area where a piece of code is accessible. The global scope is the largest scope and every nested piece of code in the global scope has access to any defined variable or function in it.

## Scope Hoisting

In JavaScript, `var` are hoisted to the top and are defined at the start of the execution but are not assigned a value untiil the line where the programmer defined it. `let` and `const` are not hoisted at all. Functions are completely hoisted and can be called from anywhere in the scope.