========== Question ==========  

### How to access Redux store outside a component?  

========== Answer ==========  

You just need to export the store from the module where it created with `createStore()`. Also, it shouldn't pollute the global window object.

```javascript
store = createStore(myReducer);

export default store;
```

========== Id ==========  
108

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#108-How-to-access-redux-store-outside-a-compon

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
