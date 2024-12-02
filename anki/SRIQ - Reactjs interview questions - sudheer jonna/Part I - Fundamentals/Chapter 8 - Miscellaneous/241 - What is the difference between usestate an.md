========== Question ==========  

### What is the difference between useState and useRef hook?  

========== Answer ==========  

1. useState causes components to re-render after state updates whereas useRef doesn’t cause a component to re-render when the value or state changes.

    Essentially, useRef is like a “box” that can hold a mutable value in its (.current) property.

2. useState allows us to update the state inside components. While useRef allows referencing DOM elements.

========== Id ==========  
241

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#241-What-is-the-difference-between-usestate-an

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
