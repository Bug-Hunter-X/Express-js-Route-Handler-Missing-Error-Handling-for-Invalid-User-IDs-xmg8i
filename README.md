# Express.js Route Handler Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user inputs.  Specifically, the provided code lacks handling for non-numeric user IDs, leading to potential crashes or unexpected behavior.

The `bug.js` file showcases the problematic code, while `bugSolution.js` presents a corrected version that includes robust error handling.

## Bug

The `bug.js` file contains an Express.js route that retrieves a user based on their ID.  However, it fails to handle cases where the `userId` parameter is not a valid number. This can lead to errors if a user enters non-numeric data in the URL.

## Solution

The `bugSolution.js` file corrects this by adding error handling. It checks if `userId` can be parsed as an integer using `isNaN()`. If not, it sends a proper error response instead of crashing.  Additionally, it handles the case where a user is not found.