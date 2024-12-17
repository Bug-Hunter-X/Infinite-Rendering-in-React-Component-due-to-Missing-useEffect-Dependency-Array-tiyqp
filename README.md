# Infinite Rendering Bug in React

This repository demonstrates a common React bug: infinite rendering caused by a missing dependency array in the `useEffect` hook.

## Bug Description
The `MyComponent` component uses `useState` to manage a count and `useEffect` to log the count to the console. However, the `useEffect` hook lacks a dependency array, causing it to run after every render, triggering another render, resulting in an infinite loop.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Open your browser and observe the console's continuous logging and the browser potentially crashing due to the infinite loop.

## Solution
The solution involves adding the `count` variable to the dependency array of the `useEffect` hook. This ensures that the effect only runs when the `count` value changes.

## Additional Notes
This example highlights the importance of correctly specifying the dependency array in `useEffect` to prevent performance issues and unexpected behavior.  Always include relevant state variables and props that the effect depends on in the array.