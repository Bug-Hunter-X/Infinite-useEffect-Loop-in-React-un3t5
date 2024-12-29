# Infinite useEffect Loop in React

This repository demonstrates a common React bug: an infinite loop caused by a `useEffect` hook lacking a cleanup function.  The `useEffect` hook, without a proper return function, continues to run indefinitely. This leads to performance degradation and potentially application crashes.  The solution shows how to implement a cleanup function to resolve this issue.

## Bug
The `bug.js` file contains a `useEffect` hook that runs without a cleanup function which continuously logs a message to the console.  This behaviour will not stop unless the application is refreshed.

## Solution
The `bugSolution.js` file demonstrates the correct usage of `useEffect` with a cleanup function to prevent the infinite loop. The return function within the `useEffect` acts as a cleanup function. This resolves the infinite loop and prevents the performance issues. 

## How to Run
Clone the repository and run `npm install` to install dependencies. Then, run `npm start` to run either bug.js or bugSolution.js. You will see console logs and can observe the difference in behavior between the buggy and the corrected versions.