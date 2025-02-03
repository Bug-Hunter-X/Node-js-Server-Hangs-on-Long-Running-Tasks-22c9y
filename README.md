# Node.js Server Hang Issue

This repository demonstrates a common issue in Node.js where a server can hang due to long-running operations that block the event loop.  The `server.js` file shows the problematic code, while `server-fixed.js` provides a solution using asynchronous operations.

## Problem

The original server uses a computationally expensive `while` loop to simulate a long task. This blocks the event loop, preventing the server from handling new requests or responding to existing ones.  This leads to the server appearing unresponsive or hanging.

## Solution

The fixed version demonstrates a more appropriate approach using asynchronous operations.  Even though it still uses a long-running task, it does not block the event loop. This allows Node.js to efficiently handle multiple requests concurrently.

## How to run

1. Clone the repository.
2. Navigate to the project directory.
3. Run the original server: `node server.js` (observe the hang)
4. Run the fixed server: `node server-fixed.js` (observe proper functionality)

This example highlights the importance of using asynchronous techniques in Node.js to avoid blocking the event loop and ensure responsiveness.