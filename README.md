# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop caused by incorrect conditional rendering logic within a `useEffect` hook.

## Bug Description
The `MyComponent` uses `useState` and `useEffect`.  The `useEffect` has a condition that should prevent unnecessary side effects, but it causes an infinite loop because the conditional check within the effect itself triggers a state update, causing another re-render and another execution of the effect.

## How to Reproduce
1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the browser console; you'll see 'Count is greater than 0' printed repeatedly, indicating the infinite loop. 

## Solution
The solution moves the conditional logic outside the useEffect, ensuring the side effect only runs when the count changes. This prevents the infinite loop.

## License
MIT