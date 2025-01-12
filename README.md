# Firebase Snapshot Data Race Condition
This repository demonstrates a common error when working with Firebase document snapshots: attempting to access data before the snapshot has fully loaded.

The `bug.js` file shows the problematic code. The `bugSolution.js` file provides the corrected approach using `.then()` or async/await to handle the asynchronous nature of data loading from Firebase.

## How to Reproduce the Bug
1. Clone this repository.
2. Ensure you have the Firebase SDK installed and configured correctly.
3. Run `bug.js`. Observe the error thrown.
4. Run `bugSolution.js`. Verify the correct behavior.

## Solution
Always wait for the snapshot to load completely before accessing its properties using promises or async/await.