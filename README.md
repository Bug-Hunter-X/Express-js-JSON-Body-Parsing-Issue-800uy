# Express.js JSON Body Parsing Issue

This repository demonstrates a common issue in Express.js applications where the JSON payload from a POST request is not correctly parsed, resulting in an empty `req.body` object.

## Bug Description

The provided Express.js server fails to parse incoming JSON data from POST requests.  The `req.body` object remains empty despite a JSON payload being sent.

## Bug Solution

The issue is solved by ensuring the correct middleware is used to parse the JSON body.  This involves using `express.json()` middleware before defining the route handler.

## Setup and Reproduction

1. Clone the repository
2. Install dependencies: `npm install`
3. Run the server: `node bug.js`
4. Send a POST request to `http://localhost:3000/data` with a JSON payload (e.g., using curl or Postman)
5. Observe that the console logs an empty `req.body` in `bug.js`.
6. Run the solution: `node bugSolution.js`
7. Repeat step 4, and observe that the console now logs the JSON payload correctly.
