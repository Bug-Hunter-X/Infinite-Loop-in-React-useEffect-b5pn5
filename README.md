# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite loop due to the effect running after every render.

## Bug Description

The `useEffect` hook without a dependency array runs after every render. In this example, it logs the current count to the console.  Since updating the count triggers a re-render, the effect runs again, creating an infinite loop and flooding the console.

## Solution

The solution involves adding a dependency array to the `useEffect` hook.  This array specifies which values the effect depends on. The effect will only run when one of these values changes.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite console logs and slow performance.