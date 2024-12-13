# Unhandled Asynchronous Errors in Express.js

This repository demonstrates a common error in Express.js applications: improperly handling asynchronous operations that might throw errors.  The server silently fails without providing any feedback to the client when an error occurs.

## The Bug

The `bug.js` file shows an Express.js server with an asynchronous operation (`someAsyncOperation`). If this operation fails (simulated with a random chance), the error is logged to the console, but no error response is sent to the client.  This results in a poor user experience, as the client might not understand why the request failed.

## The Solution

The `bugSolution.js` file demonstrates the correct way to handle asynchronous errors. It uses a `try...catch` block within the asynchronous operation's handler to capture any errors. The server will now send an appropriate error response (with a status code like 500) to the client, improving error handling and user experience.

## How to Run

1. Clone this repository.
2. Navigate to the repository's directory in your terminal.
3. Install the dependencies: `npm install express`
4. Run the bug example: `node bug.js`
5. Run the solution: `node bugSolution.js`
