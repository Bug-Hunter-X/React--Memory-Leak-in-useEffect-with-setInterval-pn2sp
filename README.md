# React: Memory Leak in useEffect with setInterval
This repository demonstrates a common error in React applications: memory leaks caused by improper use of the `setInterval` function within the `useEffect` hook.

## Problem
The provided `MyComponent` uses `setInterval` to update a counter every second. However, it lacks a cleanup function to stop the interval when the component unmounts. This leads to a memory leak, as the interval continues running even after the component is removed from the DOM.

## Solution
The solution involves using a cleanup function in the `useEffect` hook to `clearInterval` before the component unmounts. This ensures that the interval is stopped properly, preventing memory leaks.