========== Question ==========  

### Why are Redux state functions called reducers?  

========== Answer ==========  

Reducers always return the accumulation of the state (based on all previous and
current actions). Therefore, they act as a reducer of state. Each time a Redux
reducer is called, the state and action are passed as parameters. This state is
then reduced (or accumulated) based on the action, and then the next state is
returned. You could _reduce_ a collection of actions and an initial state (of
the store) on which to perform these actions to get the resulting final state.

========== Id ==========  
113

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#113-Why-are-redux-state-functions-called-reduc

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
