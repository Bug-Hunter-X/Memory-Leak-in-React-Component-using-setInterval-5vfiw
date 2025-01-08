# React setInterval Memory Leak Bug
This repository demonstrates a common bug in React applications involving the use of `setInterval` within the `useEffect` hook.  The bug stems from the missing cleanup function to clear the interval, resulting in a memory leak.  The solution provides the correct implementation to avoid this issue.

## Bug Description:
The provided `MyComponent` uses `setInterval` to update a counter every second. However, it lacks a cleanup function within the `useEffect` hook to clear the interval when the component unmounts. This leads to the interval continuing to run indefinitely, causing a memory leak.

## Solution:
The solution demonstrates the correct usage of `setInterval` within `useEffect`. A cleanup function is added to `clearInterval` when the component unmounts. This prevents memory leaks and ensures proper resource management.