========== Question ==========  

### What are the core principles of Redux?  

========== Answer ==========  

Redux follows three fundamental principles:

1.  **Single source of truth:** The state of your whole application is stored in
    an object tree within a single store. The single state tree makes it easier
    to keep track of changes over time and debug or inspect the application.

2.  **State is read-only:** The only way to change the state is to emit an
    action, an object describing what happened. This ensures that neither the
    views nor the network callbacks will ever write directly to the state.

3.  **Changes are made with pure functions:** To specify how the state tree is
    transformed by actions, you write reducers. Reducers are just pure functions
    that take the previous state and an action as parameters, and return the
    next state.

========== Id ==========  
104

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#104-What-are-the-core-principles-of-redux

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
