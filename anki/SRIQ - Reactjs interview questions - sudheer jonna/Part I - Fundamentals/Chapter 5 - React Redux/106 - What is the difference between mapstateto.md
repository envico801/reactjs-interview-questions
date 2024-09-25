========== Question ==========  

### What is the difference between `mapStateToProps()` and `mapDispatchToProps()`?  

========== Answer ==========  

`mapStateToProps()` is a utility which helps your component get updated state
(which is updated by some other components):

```javascript
const mapStateToProps = (state) => {
    return {
        todos: getVisibleTodos(state.todos, state.visibilityFilter),
    };
};
```

`mapDispatchToProps()` is a utility which will help your component to fire an
action event (dispatching action which may cause change of application state):

```javascript
const mapDispatchToProps = (dispatch) => {
    return {
        onTodoClick: (id) => {
            dispatch(toggleTodo(id));
        },
    };
};
```

It is recommended to always use the “object shorthand” form for the
`mapDispatchToProps`.

Redux wraps it in another function that looks like (…args) =>
dispatch(onTodoClick(…args)), and pass that wrapper function as a prop to your
component.

```javascript
const mapDispatchToProps = {
    onTodoClick,
};
```

========== Id ==========  
106

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#106-What-is-the-difference-between-mapstateto

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
