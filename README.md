# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input parameters.

## Bug Description
The provided `bug.js` code snippet shows a route handler that fetches a user by ID.  However, it doesn't handle cases where the provided `userId` is not a valid number. This can lead to unexpected behavior or crashes due to `parseInt` failing silently or attempting to access the `users` array with a non-numeric index.

## Solution
The `bugSolution.js` file demonstrates the correct way to handle the error.  By explicitly checking if the parsed ID is a number before using it, we ensure the code gracefully handles invalid input and prevents potential crashes.  A 400 Bad Request status code is returned for invalid input, improving error reporting and user experience.