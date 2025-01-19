# JavaScript Loose Comparison Bug

This repository demonstrates a common JavaScript bug related to loose comparison (==) and the handling of `undefined` values.

## Bug Description
The `foo` function uses loose comparison (`==`) to check for `null`. While it correctly returns 0 for `null`, it produces `NaN` when given `undefined` because the loose comparison doesn't distinguish between `null` and `undefined`. 

## Solution
The solution involves using strict equality (`===`) instead. This ensures type checking as well as value checking, which prevents unexpected behavior.

## How to reproduce the bug
1. Clone this repository.
2. Run `bug.js` using Node.js or a browser console. Observe the unexpected NaN.