# React useEffect Hook Missing Dependency

This repository demonstrates a common error in React applications: forgetting to include state variables in the dependency array of the `useEffect` hook. This can lead to unexpected behavior and potentially infinite loops.

## Bug Description
The provided `MyComponent` uses the `useEffect` hook to log the current count to the console. However, the `count` variable is missing from the dependency array. As a result, the effect runs after every render, regardless of whether `count` has actually changed.  This leads to unnecessary re-renders and potential performance issues. 

## Solution
The solution involves adding `count` to the dependency array. This ensures that the effect only runs when the value of `count` changes, resolving the issue.
