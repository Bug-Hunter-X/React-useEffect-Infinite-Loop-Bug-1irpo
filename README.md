# React useEffect Infinite Loop Bug
This repository demonstrates a common React bug involving the `useEffect` hook causing an infinite loop.  The bug arises from an incorrectly specified dependency array, leading to unnecessary re-renders and potential performance issues.

## Bug Description
The provided `MyComponent` uses `useEffect` to log the current `count` value. However, the dependency array is missing or contains incorrect dependencies. This causes the effect to run on every render, including each time the `count` state changes, creating an infinite loop.

## Solution
The solution involves correctly specifying the dependency array for `useEffect` to only run when the `count` state actually changes. This ensures that the effect doesn't cause unintended re-renders.