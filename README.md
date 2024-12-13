# Silent Route Failure in Next.js

This repository demonstrates a common, yet subtle, error in Next.js applications involving the `router.push()` method.  When attempting to navigate to a route that does not exist, the application silently fails, providing no feedback to the user.  This can lead to confusion and unexpected behavior.

## Bug Description

The provided code uses `router.push()` to navigate to a route ('/nonexistent-route') that is not defined in the application's `pages` directory. Instead of showing an error or redirecting to a 404 page, Next.js simply does nothing resulting in a broken user experience.

## Solution

The solution involves utilizing the `router.push`'s callback to handle potential errors or utilizing an error boundary component to handle the failure scenario gracefully.
