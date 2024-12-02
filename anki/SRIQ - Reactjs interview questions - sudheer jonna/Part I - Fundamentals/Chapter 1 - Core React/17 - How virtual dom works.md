========== Question ==========  

### How Virtual DOM works?  

========== Answer ==========  

The _Virtual DOM_ works in three simple steps.

1. Whenever any underlying data changes, the entire UI is re-rendered in Virtual DOM representation.

    ![vdom1](../../../../images/vdom1.png)

2. Then the difference between the previous DOM representation and the new one is calculated.

    ![vdom2](../../../../images/vdom2.png)

3. Once the calculations are done, the real DOM will be updated with only the things that have actually changed.

    ![vdom3](../../../../images/vdom3.png)

========== Id ==========  
17

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#17-How-virtual-dom-works

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
