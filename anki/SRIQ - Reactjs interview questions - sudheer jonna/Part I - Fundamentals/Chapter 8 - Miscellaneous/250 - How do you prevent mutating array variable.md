========== Question ==========  

### How do you prevent mutating array variables?  

========== Answer ==========  

The preexisting variables outside of the function scope including state, props
and context leads to a mutation and they result in unpredictable bugs during the
rendering stage. The below points should be taken care while working with arrays
variables.

1. You need to take copy of the original array and perform array operations on
   it for the rendering purpose. This is called local mutation.

2. Avoid triggering mutation methods such as push, pop, sort and reverse methods
   on original array. It is safe to use filter, map and slice method because
   they create a new array.

========== Id ==========  
250

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#250-How-do-you-prevent-mutating-array-variable

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
