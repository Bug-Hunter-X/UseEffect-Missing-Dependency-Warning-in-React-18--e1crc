# React 18 useEffect Missing Dependency Bug

This repository demonstrates a common error in React 18 and later versions related to missing dependencies in the `useEffect` hook.  Failing to include all variables that change within the `useEffect` callback in the dependency array can result in unexpected behavior, such as stale closures, unnecessary re-renders, and potential memory leaks.  The solution showcases the proper way to handle dependencies to avoid these issues.

## Bug
The `bug.js` file contains the problematic code.  The `setInterval` function creates a memory leak because the component re-renders even when there's no state update.