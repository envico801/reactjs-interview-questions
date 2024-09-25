========== Question ==========  

### In which scenarios do error boundaries not catch errors?  

========== Answer ==========  

Below are the cases in which error boundaries don't work,

1.  Inside Event handlers

2.  Asynchronous code using **setTimeout or requestAnimationFrame** callbacks

3.  During Server side rendering

4.  When errors thrown in the error boundary code itself

========== Id ==========  
174

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#174-In-which-scenarios-do-error-boundaries-not

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
