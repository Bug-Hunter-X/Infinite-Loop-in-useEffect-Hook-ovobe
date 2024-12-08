# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications: creating an infinite loop within the `useEffect` hook.  The bug arises from improperly updating state within the `useEffect`'s dependency array, leading to continuous re-renders and an infinite loop.

## Bug Description
The provided code attempts to increment a state variable `count` within the `useEffect` hook without specifying any dependencies. This causes the `useEffect` to run infinitely, as each state update triggers another render, leading to another `useEffect` execution.

## Solution
The solution involves correctly managing dependencies within the `useEffect` hook.  By specifying an empty array `[]` as dependencies, the effect runs only once after the initial render. Alternatively, specify the variables that will trigger re-runs.