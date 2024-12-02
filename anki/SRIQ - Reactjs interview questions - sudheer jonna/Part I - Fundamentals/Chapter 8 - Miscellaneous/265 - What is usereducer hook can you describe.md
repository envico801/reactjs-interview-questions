========== Question ==========  

### What is useReducer hook? Can you describe its usage?  

========== Answer ==========  

The `useReducer` hook is a React hook that provides an alternative to `useState` for managing complex state logic in functional components. It's particularly useful when you have state transitions that depend on the previous state or when the next state is determined by multiple sub-values.

Here's a brief overview of `useReducer`:

1. Basic structure:

    ```javascript
    const [state, dispatch] = useReducer(reducer, initialState);
    ```

2. Components:

    - `state`: The current state value

    - `dispatch`: A function to send actions to update the state

    - `reducer`: A pure function that takes the current state and an action, and returns the new state

    - `initialState`: The initial state value

3. Usage:

```javascript
import React, { useReducer } from 'react';

// Reducer function
const counterReducer = (state, action) => {
    switch (action.type) {
        case 'INCREMENT':
            return { count: state.count + 1 };
        case 'DECREMENT':
            return { count: state.count - 1 };
        default:
            return state;
    }
};

const Counter = () => {
    // Using useReducer
    const [state, dispatch] = useReducer(counterReducer, { count: 0 });

    return (
        <div>
            Count: {state.count}
            <button onClick={() => dispatch({ type: 'INCREMENT' })}>+</button>
            <button onClick={() => dispatch({ type: 'DECREMENT' })}>-</button>
        </div>
    );
};

export default Counter;
```

In this example:

1. We define a `counterReducer` function that specifies how the state should change in response to different actions.

2. The `useReducer` hook is called with the reducer function and an initial state.

3. We use the `dispatch` function to send actions to the reducer, which then updates the state.

4. The component re-renders with the new state when an action is dispatched.

Key benefits of `useReducer`:

1. Centralized state logic: All state update logic is contained in the reducer function.

2. Predictable state changes: The reducer must return a new state for any given current state and action.

3. Easier testing: Reducer functions are pure and can be easily unit tested.

4. Complex state transitions: Useful for managing state that involves multiple sub-values or when the next state depends on the previous one.

5. Performance optimization: Can be more efficient than `useState` for complex state logic.

========== Id ==========  
265

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#265-What-is-usereducer-hook-can-you-describe

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
