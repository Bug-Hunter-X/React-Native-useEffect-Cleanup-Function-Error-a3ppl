# React Native useEffect Cleanup Function Error

This repository demonstrates a bug in React Native where an error thrown within the cleanup function of a `useEffect` hook is not properly handled, leading to unexpected crashes or behavior.

## Bug Description

The issue arises when the cleanup function of `useEffect` throws an error. This error isn't caught by the React Native runtime, causing the application to become unstable.  The example provided showcases this with a subscription that might throw on unsubscription.

## Solution

The solution involves using a `try...catch` block within the cleanup function to handle potential errors gracefully. This prevents the application from crashing and allows for more robust error handling.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npx react-native run-android` (or equivalent for iOS).
4. Observe the error in the console and the behavior of the application.
5. Uncomment the solution code to see how error handling improves stability.
