# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of error handling for invalid input.  The `bug.js` file shows a route that attempts to parse a user ID as an integer without checking for non-numeric input.  This can lead to unexpected behavior or crashes.  `bugSolution.js` provides a corrected version with robust error handling.

## Problem

The provided code attempts to parse a user ID from the request parameters.  If the user ID is not a number, `parseInt(userId)` will return `NaN`, which can cause unexpected behavior or crashes when used in subsequent operations.

## Solution

The solution incorporates checks to ensure the user ID is a valid number before attempting any operations.