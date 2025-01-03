# React useEffect: Missing Dependency Causes Stale Closures

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include state variables in the dependency array.  This can lead to unexpected behavior and stale closures.

## The Problem

The `useEffect` hook in the `bug.js` file is missing `count` from its dependency array. This means that the effect only runs once after the initial render, even though the `count` value changes.  This leads to the console log always showing the initial value of `count`, not the updated value.

## The Solution

The `bugSolution.js` file demonstrates the correct usage of `useEffect`. By including `count` in the dependency array, the effect now runs every time the `count` value changes, providing the correct current value in the console log.

## How to Run

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install the necessary dependencies.
4. Run `npm start` to start the development server.

You can then open your browser and see the behavior in each of the files.