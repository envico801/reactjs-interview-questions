========== Question ==========  

### What is the purpose of the constants in Redux?  

========== Answer ==========  

Constants allows you to easily find all usages of that specific functionality
across the project when you use an IDE. It also prevents you from introducing
silly bugs caused by typos – in which case, you will get a `ReferenceError`
immediately.

Normally we will save them in a single file (`constants.js` or
`actionTypes.js`).

```javascript
export const ADD_TODO = 'ADD_TODO';
export const DELETE_TODO = 'DELETE_TODO';
export const EDIT_TODO = 'EDIT_TODO';
export const COMPLETE_TODO = 'COMPLETE_TODO';
export const COMPLETE_ALL = 'COMPLETE_ALL';
export const CLEAR_COMPLETED = 'CLEAR_COMPLETED';
```

In Redux, you use them in two places:

1.  **During action creation:**

    Let's take `actions.js`:

    ```javascript
    import { ADD_TODO } from './actionTypes';
    export function addTodo(text) {
        return { type: ADD_TODO, text };
    }
    ```

2.  **In reducers:**

    Let's create `reducer.js`:

    ```javascript
    import { ADD_TODO } from './actionTypes';
    export default (state = [], action) => {
        switch (action.type) {
            case ADD_TODO:
                return [
                    ...state,
                    {
                        text: action.text,
                        completed: false,
                    },
                ];
            default:
                return state;
        }
    };
    ```

========== Id ==========  
118

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#118-What-is-the-purpose-of-the-constants-in-re

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
