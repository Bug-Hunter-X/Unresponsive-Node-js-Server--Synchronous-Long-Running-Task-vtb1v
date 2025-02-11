# Unresponsive Node.js Server

This repository demonstrates a common Node.js issue: an unresponsive server caused by a long-running synchronous operation blocking the event loop.  The `server.js` file contains the buggy code, while `server-solution.js` provides a corrected version using asynchronous operations.

## Problem

The original server code performs a 5-second CPU-intensive operation synchronously within the request handler. This blocks the event loop, preventing the server from accepting new requests or responding to existing ones.

## Solution

The solution utilizes asynchronous operations (using `setTimeout`) to prevent blocking the event loop.  This allows the server to remain responsive while handling long-running tasks.