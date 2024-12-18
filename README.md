# React useEffect Hook Missing Dependency

This repository demonstrates a common error in React applications: an infinite loop caused by a missing dependency in the `useEffect` hook.

## Bug Description
The `useEffect` hook is designed to perform side effects after every render. However, if the dependency array is missing or incorrect, it can lead to unwanted behavior, such as an infinite loop or unexpected re-renders.

## Bug Reproduction
1. Clone this repository.
2. Navigate to the `bug` folder.
3. Run `npm start` to start the development server.
4. Observe the console log and the continuous re-rendering of the component.

## Solution
The solution is to add all variables used inside the `useEffect` hook to the dependency array. In this example, `count` is used, so it needs to be included in the array.  Adding the dependency ensures the effect only runs when `count` changes.

## Additional Information
Always carefully consider what variables your `useEffect` hook depends on and make sure they are included in the dependency array. Missing dependencies can cause subtle bugs that are difficult to track down. Please refer to the official React documentation for more details about using the `useEffect` hook.