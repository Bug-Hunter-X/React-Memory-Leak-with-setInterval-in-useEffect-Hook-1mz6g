# React Memory Leak Bug
This repository demonstrates a common React bug involving memory leaks caused by the improper use of setInterval within the useEffect hook.  The bug involves the continuous incrementing of a counter even after the component is unmounted.  The solution involves correctly clearing the interval using the cleanup function provided by useEffect.

## How to Reproduce
1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the app: `npm start`
4. Observe the counter incrementing.  Even after navigating away from the component, the counter continues to increment in the background causing a memory leak.

## Solution
The provided solution correctly implements the cleanup function within useEffect to prevent memory leaks.  This ensures that the setInterval is cleared when the component unmounts.