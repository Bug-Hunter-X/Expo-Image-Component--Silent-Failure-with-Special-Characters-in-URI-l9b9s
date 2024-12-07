# Expo Image Component: Silent Failure with Special Characters in URI

This repository demonstrates a bug in the Expo `Image` component where images with special characters in their URIs fail to load silently.  The issue is particularly challenging because no error messages are logged to the console, making debugging difficult.

The `bug.js` file shows the problematic code.  The `bugSolution.js` file provides a solution to handle special characters and prevent this issue.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `expo start`.
4. Observe that the image in `bug.js` fails to load, while the image in `bugSolution.js` loads correctly.

## Solution

The solution involves properly URL-encoding the URI before passing it to the `Image` component.  See `bugSolution.js` for implementation details.