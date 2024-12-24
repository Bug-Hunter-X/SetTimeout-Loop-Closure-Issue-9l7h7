# setTimeout Loop Closure Issue in JavaScript

This repository demonstrates a common closure-related bug in JavaScript when using `setTimeout` within a loop. The issue arises because the value of the loop variable `i` is not captured correctly within each `setTimeout` callback.  Instead, the callbacks refer to the final value of `i` after the loop completes.

## Bug Description
The provided `bug.js` file contains a function `myFunction` that uses a `for` loop to schedule multiple `setTimeout` calls. The intention is to log the current value of `i` after a 1-second delay. However, due to the closure issue, all callbacks log the final value of `i` (which is 10). 

## Solution
The `bugSolution.js` file demonstrates a common solution using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, ensuring that the correct value of `i` is captured.