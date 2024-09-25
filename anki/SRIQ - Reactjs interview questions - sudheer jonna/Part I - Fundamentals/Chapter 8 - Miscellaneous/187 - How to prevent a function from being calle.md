========== Question ==========  

### How to prevent a function from being called multiple times?  

========== Answer ==========  

If you use an event handler such as **onClick or onScroll** and want to prevent
the callback from being fired too quickly, then you can limit the rate at which
callback is executed. This can be achieved in the below possible ways,

1.  **Throttling:** Changes based on a time based frequency. For example, it can
    be used using \_.throttle lodash function

2.  **Debouncing:** Publish changes after a period of inactivity. For example,
    it can be used using \_.debounce lodash function

3.  **RequestAnimationFrame throttling:** Changes based on
    requestAnimationFrame. For example, it can be used using raf-schd lodash
    function

========== Id ==========  
187

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#187-How-to-prevent-a-function-from-being-calle

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
