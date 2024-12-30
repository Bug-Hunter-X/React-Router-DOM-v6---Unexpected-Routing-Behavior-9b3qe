This repository demonstrates a common issue encountered when working with React Router DOM v6: unexpected routing behavior. Links initially navigate correctly, but subsequent clicks fail to update the URL or render the appropriate component.  The problem is not due to obvious errors, such as typos or incorrect path definitions. This repository aims to reproduce this subtle bug and demonstrate the solution.

## How to reproduce

1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Click the link to navigate to '/about'.
5. Click the link again - navigation should fail.

## Solution

The solution involves ensuring proper usage of `useLocation` to detect changes in URL, correctly managing component state to avoid infinite rerenders, or using a `Navigate` component (see bugSolution.js).