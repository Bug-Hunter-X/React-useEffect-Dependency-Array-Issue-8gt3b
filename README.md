# React useEffect Dependency Array Issue

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include state variables in the dependency array.  This can cause unexpected re-renders and potentially infinite loops.

## The Bug

The `bug.js` file contains a component with a `useEffect` hook. The hook logs the current count, but the `count` variable is missing from the dependency array. This means the effect runs after every render, even if the `count` hasn't changed, leading to unnecessary console logs and potential performance issues.  In more complex scenarios, this can lead to unexpected behavior or infinite rendering loops.

## The Solution

The `bugSolution.js` file demonstrates the correct way to use `useEffect`.  The `count` variable is added to the dependency array. Now, the effect only runs when the value of `count` changes.

## How to Run

1. Clone this repository.
2. Navigate to the repository's directory in your terminal.
3. Run `npm install` to install the necessary dependencies.
4. Run `npm start` to start the development server. 
5. Observe the behavior of both components in your browser's console.