# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency.

## Problem
The `useEffect` hook, when used without specifying a dependency array, runs after every render.  If the effect modifies state, it creates an infinite loop: the state change triggers a re-render, which triggers the effect again, and so on.

## Solution
Ensure all values read inside the `useEffect` are listed in the dependency array. This array tells React when to run the effect.

## How to reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop in the console and the crashing app.
5. Check the `bugSolution.js` file for the correct implementation.