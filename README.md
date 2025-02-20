# React Native Uninitialized State Access Bug

This repository demonstrates a common error in React Native: attempting to access a state variable before it has been initialized.  This often occurs when using the `useState` hook or within class components' lifecycle methods.

## Problem

The `bug.js` file illustrates the issue.  Accessing the state variable `count` within the `useEffect` hook before it is initialized by `useState` results in `undefined` being logged to the console. This can lead to unpredictable behavior in the application.

## Solution

The `bugSolution.js` file shows a corrected approach.  By making sure to only access `count` after it has been assigned a value from `useState`, we avoid this issue.

## How to reproduce:

1. Clone this repository.
2. Navigate to the directory.
3. Run `npx react-native run-android` or `npx react-native run-ios` (depending on your target platform).
4. Observe the console log and the application's behavior for both `bug.js` and `bugSolution.js`. 
