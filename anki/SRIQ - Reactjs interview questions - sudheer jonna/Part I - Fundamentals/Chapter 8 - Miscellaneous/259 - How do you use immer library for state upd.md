========== Question ==========  

### How do you use immer library for state updates?  

========== Answer ==========  

Immer library enforces the immutability of state based on **copy-on-write**
mechanism. It uses JavaScript proxy to keep track of updates to immutable
states. Immer has 3 main states as below,

1. **Current state:** It refers to actual state

2. **Draft state:** All new changes will be applied to this state. In this
   state, draft is just a proxy of the current state.

3. **Next state:** It is formed after all mutations applied to the draft state

Immer can be used by following below instructions,

1. Install the dependency using `npm install use-immer` command

2. Replace `useState` hook with `useImmer` hook by importing at the top

3. The setter function of `useImmer` hook can be used to update the state.

For example, the mutation syntax of immer library simplifies the nested address
object of user state as follows,

```jsx
import { useImmer } from 'use-immer';
const [user, setUser] = useImmer({
    name: 'John',
    age: 32,
    address: {
        country: 'Singapore',
        postalCode: 440004,
    },
});
//Update user details upon any event
setUser((draft) => {
    draft.address.country = 'Germany';
});
```

The preceding code enables you to update nested objects with a conceise mutation
syntax.

========== Id ==========  
259

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#259-How-do-you-use-immer-library-for-state-upd

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
