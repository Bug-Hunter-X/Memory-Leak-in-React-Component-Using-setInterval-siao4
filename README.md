# React Component Memory Leak

This repository demonstrates a common memory leak in React components that use `setInterval` within the `useEffect` hook without proper cleanup.  The `bug.js` file contains the problematic code.  The `bugSolution.js` provides the corrected version.

## Problem
The `setInterval` function continues to run even after the component unmounts. This leads to memory leaks and unexpected behavior.

## Solution
The solution involves using the return value of `useEffect` to clear the interval when the component is unmounted.