# Unhandled Promise Rejection in Express.js Async Middleware

This repository demonstrates a common error in Express.js applications: unhandled promise rejections in asynchronous middleware.  The `bug.js` file shows an example of asynchronous middleware that lacks proper error handling.  This can lead to silent failures and unexpected application behavior.

The `bugSolution.js` file provides a corrected version with comprehensive error handling, demonstrating how to prevent these issues.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `node bug.js`.
4. Observe the server start, but errors might not be logged visibly.
5. Run `node bugSolution.js` to see the fixed version with proper error handling.

## Solution

Always handle potential errors in asynchronous operations using `.catch()` or `try...catch` blocks.  Proper logging of errors is crucial for debugging and monitoring.