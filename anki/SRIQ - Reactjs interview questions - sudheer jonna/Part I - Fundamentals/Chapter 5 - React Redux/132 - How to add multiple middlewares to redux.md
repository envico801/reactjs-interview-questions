========== Question ==========  

### How to add multiple middlewares to Redux?  

========== Answer ==========  

You can use `applyMiddleware()`.

For example, you can add `redux-thunk` and `logger` passing them as arguments to `applyMiddleware()`:

```javascript
import { createStore, applyMiddleware } from 'redux';
const createStoreWithMiddleware = applyMiddleware(
    ReduxThunk,
    logger,
)(createStore);
```

========== Id ==========  
132

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#132-How-to-add-multiple-middlewares-to-redux

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
