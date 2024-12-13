# Closure Problem in JavaScript Loops

This repository demonstrates a common error in JavaScript involving closures within loops and `setTimeout`.  The issue arises because the callback function within `setTimeout` doesn't capture the value of `i` at the time it's created, but rather captures a reference to `i`. By the time the `setTimeout` functions execute, the loop has already completed, and `i` will be its final value.

The `bug.js` file shows the problematic code, while `bugSolution.js` provides a solution using an immediately invoked function expression (IIFE) to create a new scope for each iteration.