# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js: server unresponsiveness caused by a long-running synchronous operation blocking the event loop.  The `server.js` file contains a server that simulates this problem by performing a 5-second CPU-bound task within the request handler.  This prevents the server from processing other requests during this time, leading to hangs and unresponsiveness.

The `serverSolution.js` file shows how to resolve this by using asynchronous operations and appropriate techniques to prevent blocking the event loop.

## How to Reproduce

1. Clone this repository.
2. Run `node server.js`.
3. Make multiple requests to `http://localhost:3000/`.  You'll observe that the server becomes unresponsive or slow after a few requests.

## Solution

Refer to `serverSolution.js` for a solution that uses asynchronous operations.