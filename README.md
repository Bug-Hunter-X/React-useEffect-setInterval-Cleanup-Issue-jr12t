# React useEffect setInterval Cleanup Issue

This repository demonstrates a common error in React applications involving the use of `setInterval` within the `useEffect` hook without proper cleanup. This can lead to memory leaks and unexpected behavior.

## Bug Description
The `MyComponent` component uses `setInterval` to update the `count` state every second. However, it fails to provide a cleanup function within the `useEffect` hook to stop the interval when the component unmounts. This results in the interval continuing to run even after the component is no longer rendered, causing memory leaks and potential performance issues.

## Solution
The solution involves adding a cleanup function to the `useEffect` hook. This function will clear the interval when the component unmounts, preventing memory leaks and ensuring proper behavior.
