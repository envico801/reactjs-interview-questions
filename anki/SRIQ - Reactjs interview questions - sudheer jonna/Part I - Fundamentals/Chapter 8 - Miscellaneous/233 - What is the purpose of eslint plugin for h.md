========== Question ==========  

### What is the purpose of eslint plugin for hooks?  

========== Answer ==========  

The ESLint plugin enforces rules of Hooks to avoid bugs. It assumes that any
function starting with ”use” and a capital letter right after it is a Hook. In
particular, the rule enforces that,

1.  Calls to Hooks are either inside a PascalCase function (assumed to be a
    component) or another useSomething function (assumed to be a custom Hook).

2.  Hooks are called in the same order on every render.

========== Id ==========  
233

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#233-What-is-the-purpose-of-eslint-plugin-for-h

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
