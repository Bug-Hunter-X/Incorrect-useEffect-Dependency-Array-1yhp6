# Incorrect useEffect Dependency Array in React 18+

This repository demonstrates a common error in React's `useEffect` hook and how to fix it.  The error arises from omitting state variables from the dependency array, leading to unexpected behavior and potentially infinite loops.

## The Problem

The provided `MyComponent` utilizes `useState` to manage a count. The `useEffect` hook is intended to log the count to the console whenever it changes.  However, omitting `count` from the dependency array prevents the effect from running when `count` updates, resulting in inconsistent behavior.

## The Solution

The solution is simply to include `count` in the dependency array.  This ensures that the `useEffect` runs whenever the `count` value changes.

## How to reproduce

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install the necessary packages.
4. Run `npm start` to start the development server.
5. Observe the console logs and how they change with the correct solution. 
