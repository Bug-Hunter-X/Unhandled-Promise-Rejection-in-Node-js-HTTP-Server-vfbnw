# Unhandled Promise Rejection in Node.js HTTP Server

This repository demonstrates a common error in Node.js server-side development: improper handling of promise rejections in asynchronous operations.  The example code simulates an asynchronous task (`someAsyncOperation`) that might fail.  Without proper error handling, the client will receive no response, and only partial logging will be visible in the server console.

## Bug
The `bug.js` file contains the problematic code.  The `someAsyncOperation` function can throw an error, but there's no proper mechanism to send an error response to the client or handle the error gracefully.

## Solution
The `bugSolution.js` file provides a corrected version, including comprehensive error handling. The solution sends appropriate error responses to the client, providing feedback even if the server encounters an issue during request processing.

## How to Run
1. Clone this repository.
2. Navigate to the directory in your terminal.
3. Run `node bug.js` (for the buggy version) or `node bugSolution.js` (for the solution).