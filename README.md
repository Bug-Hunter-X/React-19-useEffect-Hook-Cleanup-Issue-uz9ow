# React 19 useEffect Hook Cleanup Issue

This repository demonstrates a common error related to the `useEffect` hook in React 19: forgetting to include a cleanup function.

## Problem

The `bug.js` file contains a component that uses `useEffect` to log a message when the component mounts. However, it's missing the return statement for the cleanup function. This can lead to memory leaks and unexpected behavior, particularly if the effect performs actions that need to be reversed when the component unmounts.

## Solution

The `bugSolution.js` file shows the corrected version.  A return statement is added which returns a cleanup function. The cleanup function runs immediately before the component unmounts and is vital for preventing memory leaks or other unintended behavior.

## How to reproduce

1. Clone this repository.
2. Navigate to the root directory.
3. Run `npm install` to install the dependencies.
4. Run `npm start` to start the development server.
5. Observe the console logs and component behavior in both the buggy and corrected versions.