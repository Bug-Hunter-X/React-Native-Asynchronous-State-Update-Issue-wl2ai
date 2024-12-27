# React Native Asynchronous State Update Issue

This repository demonstrates a common issue in React Native applications involving asynchronous operations and state updates.  The problem arises when asynchronous functions access state variables that might become stale due to component re-renders before the asynchronous operation completes. 

## Problem Description

The `bug.js` file contains a React component that fetches data from an API asynchronously.  If the API call takes a significant amount of time, and the component re-renders during this process, the asynchronous function might access outdated state values. 

## Solution

The `bugSolution.js` file demonstrates a solution using functional updates in the `useState` hook. This approach ensures that the state is always updated with the most recent values.  Also added error handling for network issues.