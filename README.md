# React Router Dom v6 Catch All Route '*' Issue

This repository demonstrates a common issue encountered when using the catch-all route ('*') in React Router Dom v6.  The issue is that the catch-all route, intended to handle any unmatched routes, may not work as expected, sometimes failing to display the 404 page and instead redirecting to the home page. This is often due to order of routes and how React Router matches routes. 

## Problem
The problem lies in the order of routes defined within the `<Routes>` component. If a route with a more general path (like '/') comes before the catch-all route ('*'), React Router will match the home page route, rather than the 404 route, even if the URL does not match any specific route. 

## Solution
The solution involves placing the catch-all route ('*') at the end of the route definitions in the `<Routes>` component. This ensures that it only matches routes after all other routes have been checked.
