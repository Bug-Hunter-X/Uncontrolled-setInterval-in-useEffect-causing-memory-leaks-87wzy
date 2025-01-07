# Uncontrolled setInterval in useEffect causing memory leaks

This repository demonstrates a common React bug involving the use of `setInterval` within the `useEffect` hook without proper cleanup.  This can lead to memory leaks and unexpected behavior.

## Bug Description:
The `MyComponent` component uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts, resulting in the interval continuing to run even after the component is no longer needed.  This is a memory leak.

## Solution:
The solution involves using the return value of `useEffect` to clear the interval when the component unmounts.