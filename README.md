# React useEffect setInterval Memory Leak

This repository demonstrates a common error in React applications involving the use of `setInterval` within the `useEffect` hook.  The issue arises from the lack of a cleanup function to stop the interval when the component unmounts, leading to a memory leak.

## Bug Description
The `MyComponent` component uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component is unmounted, resulting in continued updates even after the component is no longer rendered.

## Solution
The solution involves returning a cleanup function from the `useEffect` hook. This function clears the interval using `clearInterval` when the component unmounts, preventing the memory leak.

## How to run the code
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.