# Unexpected NaN Behavior in JavaScript Addition Function

This repository demonstrates a common, yet subtle, JavaScript bug related to handling `NaN` (Not a Number) values in addition operations.

The `foo` function attempts to gracefully handle `null` values by returning 0 if either input is `null`. However, it does not explicitly address `NaN`, resulting in unexpected behavior when `NaN` is involved in the addition.

## Bug

The `bug.js` file contains the function with the bug. Observe the unexpected `NaN` results when calling the function with `NaN` arguments. This can be problematic if your application needs to handle `NaN` values differently or needs to provide more robust error handling.

## Solution

The `bugSolution.js` file demonstrates a solution.  It explicitly checks for `NaN` using `isNaN()` and handles it appropriately. For this example, we choose to return 0 if either of the input values is `NaN`.

This showcases the importance of explicitly handling `NaN` to avoid unexpected behavior and improve the robustness of your JavaScript code.