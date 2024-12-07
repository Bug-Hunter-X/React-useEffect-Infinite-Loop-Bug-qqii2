# React useEffect Infinite Loop Bug
This repository demonstrates a common error in React's `useEffect` hook: creating an infinite loop by omitting a necessary dependency.

## Bug Description
The `useEffect` hook is designed to perform side effects after a component renders. However, if the dependency array is incorrectly specified, it can lead to unintended re-renders and an infinite loop. In this example, the missing dependency causes the `useEffect` to run after every render, resulting in an infinite update cycle and console spam.

## How to Reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output – it continuously updates with the counter value.

## Solution
The solution involves correctly specifying the dependency array for the `useEffect` hook. By including `count` in the dependency array, the effect only runs when the `count` state variable changes.