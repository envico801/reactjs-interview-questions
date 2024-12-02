========== Question ==========  

### How to set initial state in Redux?  

========== Answer ==========  

You need to pass initial state as second argument to createStore:

```javascript
const rootReducer = combineReducers({
    todos: todos,
    visibilityFilter: visibilityFilter,
});

const initialState = {
    todos: [{ id: 123, name: 'example', completed: false }],
};

const store = createStore(rootReducer, initialState);
```

========== Id ==========  
133

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#133-How-to-set-initial-state-in-redux

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
