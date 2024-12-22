# React Router v6 Catch-all Route Bug

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router v6.  The catch-all route is incorrectly intercepting other defined routes, preventing them from rendering.

## Problem Description
The `App.js` file contains a React Router configuration where a catch-all route is defined before a specific route (`/about`). This causes the catch-all route to always be matched, regardless of the URL.

## Solution
The `AppSolution.js` file provides the corrected code. The key is to ensure that the catch-all route is placed last in the route definition order. This guarantees that it only matches when no other specific routes are matched.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Navigate to `/about`. You'll notice that the "Not Found" component is rendered instead of the "About" component.
5. Switch to `AppSolution.js` and restart to see the correct behavior.