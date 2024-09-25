========== Question ==========  

### Why do you need additional care for component libraries while using forward refs?  

========== Answer ==========  

When you start using forwardRef in a component library, you should treat it as a
breaking change and release a new major version of your library. This is because
your library likely has a different behavior such as what refs get assigned to,
and what types are exported. These changes can break apps and other libraries
that depend on the old behavior.

========== Id ==========  
351

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#351-Why-do-you-need-additional-care-for-compon

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
