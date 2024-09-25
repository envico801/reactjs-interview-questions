========== Question ==========  

### What rules need to be followed for hooks?  

========== Answer ==========  

You need to follow two rules in order to use hooks,

1.  **Call Hooks only at the top level of your react functions:** You should always use hooks at the top level of react function before any early returns. i.e, You shouldn’t call Hooks inside loops, conditions, or nested functions. This will ensure that Hooks are called in the same order each time a component renders and it preserves the state of Hooks between multiple re-renders due to useState and useEffect calls.

2.  **Call Hooks from React Functions only:** You shouldn’t call Hooks from regular JavaScript functions or class components. Instead, you should call them from either function components or custom hooks.

========== Id ==========  
169

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#169-What-rules-need-to-be-followed-for-hooks

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
