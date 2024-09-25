========== Question ==========  

### How to structure Redux top level directories?  

========== Answer ==========  

Most of the applications has several top-level directories as below:

1.  **Components**: Used for _dumb_ components unaware of Redux.

2.  **Containers**: Used for _smart_ components connected to Redux.

3.  **Actions**: Used for all action creators, where file names correspond to part of the app.

4.  **Reducers**: Used for all reducers, where files name correspond to state key.

5.  **Store**: Used for store initialization.

This structure works well for small and medium size apps.

========== Id ==========  
121

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#121-How-to-structure-redux-top-level-directori

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
