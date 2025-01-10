# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug is caused by an infinite loop due to a missing dependency array in a `useEffect` call.

## Bug Description
The provided code uses `useEffect` to log the current count value whenever the count changes.  However, because the second `useEffect` is missing a dependency array, it runs on every render, causing an infinite loop of updates and log messages to the console.  This significantly impacts the application's performance.

## Solution
The solution involves correctly specifying the dependency array for the `useEffect` hook. By adding `[count]` as the dependency array, the effect will only run when the `count` variable changes, preventing the infinite loop.