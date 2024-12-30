# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications: an infinite loop caused by incorrect usage of the `useEffect` hook. The bug occurs when a dependency is missing from the `useEffect` hook's dependency array, causing the effect to run repeatedly and potentially lead to performance issues or unexpected behavior. The solution shows how to correctly specify the dependencies to resolve the issue.

## Bug Description

The `useEffect` hook in the `MyComponent` component lacks a dependency array. This causes the `console.log` statement to execute after every render, leading to an infinite loop and filling the console with logs.  This makes the component unresponsive and might even cause the browser to crash.

## Solution

The solution involves adding `count` to the dependency array. This ensures that the effect only runs when the `count` value changes.