# React UseEffect setInterval Memory Leak
This repository demonstrates a common mistake in React: using setInterval within a useEffect hook without properly cleaning up the interval. This can lead to memory leaks and unexpected behavior.

## The Problem
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second.  However, it fails to clear the interval when the component unmounts or when the effect is rerun, resulting in multiple intervals running concurrently.

## The Solution
The `bugSolution.js` file provides the corrected code that addresses the memory leak using `clearInterval` within the cleanup function of `useEffect`.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies (if any).
3. Run the application and observe the behavior of both versions of the component to see the memory leak problem and its solution.