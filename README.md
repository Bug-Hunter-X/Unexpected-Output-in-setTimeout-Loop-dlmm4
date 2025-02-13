# JavaScript Closure Issue in setTimeout Loops

This repository demonstrates a common JavaScript bug related to closures and the `setTimeout` function within loops.  The issue arises because of how variables are captured in closures. In the provided code, each `setTimeout` callback function should print the value of `i` at the time it was created. However, due to the asynchronous nature of `setTimeout`, by the time the callback functions are executed, the loop has already completed, and the variable 'i' will have reached its final value of 10 for all callbacks. This results in the unexpected output of '10' being logged ten times. The solution involves using a closure to capture the value of 'i' at each iteration using an immediately invoked function expression (IIFE).

## How to reproduce the bug

1. Clone this repository.
2. Open `bug.js` and run the code.
3. Observe the unexpected output.