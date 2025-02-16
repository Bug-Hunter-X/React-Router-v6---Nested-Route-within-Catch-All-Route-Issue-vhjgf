# React Router v6 Nested Route Issue

This repository demonstrates an issue with nested routes in React Router v6.  Specifically, when a route with a wildcard path (`/*`) is nested within another route, it interferes with the expected behavior of the wildcard route. 

The problem arises when you attempt to nest a more specific route (e.g., `/about/*`) within a catch-all route (`/*`).  The nested route effectively overrides the catch-all route, preventing the latter from handling routes that don't match any other routes. 

The `bug.js` file contains the buggy code, and `bugSolution.js` provides the correct implementation.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to `/about` and `/random-path`. Observe the unexpected behavior of the `/*` route.