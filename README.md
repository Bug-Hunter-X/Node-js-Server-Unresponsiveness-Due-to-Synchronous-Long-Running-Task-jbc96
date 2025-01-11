# Node.js Server Unresponsiveness

This repository demonstrates a common Node.js issue: server unresponsiveness caused by a long-running synchronous operation blocking the event loop. The `server.js` file contains the buggy code, while `serverSolution.js` provides a corrected version using asynchronous operations.

## Problem

The original code includes a `while` loop that simulates a long-running task.  This blocks the event loop, preventing the server from responding to further requests until the loop completes. This results in a frozen or unresponsive server.

## Solution

The solution uses asynchronous programming techniques to avoid blocking the event loop.  This allows Node.js to efficiently handle multiple requests concurrently.