# Node.js Server Crashing Under Load

This repository demonstrates a common issue in Node.js applications where the server crashes under heavy load due to unhandled exceptions. The provided code creates a simple HTTP server that is vulnerable to crashing when faced with a large number of concurrent requests.

## Problem

The `server.js` file contains a basic HTTP server.  However, it lacks the necessary mechanisms to handle a high volume of requests concurrently.  This results in the server becoming unresponsive and eventually crashing.

## Solution

The `serverSolution.js` file provides a solution that addresses the concurrency issue using the `cluster` module for increased stability and scalability.  It utilizes multiple processes to handle incoming requests more efficiently, preventing crashes under heavy load.

## How to Run

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `node server.js` to start the original vulnerable server.
4. Run `node serverSolution.js` to start the improved, more robust server.  
5. Use a load testing tool (like k6 or Apache Bench) to simulate multiple requests to observe the difference in behavior.
