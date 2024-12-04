# React useEffect setInterval Memory Leak

This repository demonstrates a common error in React components: memory leaks caused by improper use of `setInterval` within the `useEffect` hook.

## Bug Description

The `MyComponent` component uses `setInterval` to update a counter every second. However, it fails to properly clean up the interval when the component unmounts, resulting in a memory leak.  This is especially problematic in applications with many such components or components that frequently mount and unmount. 

## Solution

The solution involves using the return function of `useEffect` to clear the interval before the component unmounts.