========== Question ==========  

### Why should not call setState in componentWillUnmount?  

========== Answer ==========  

You should not call `setState()` in `componentWillUnmount()` because once a component instance is unmounted, it will never be mounted again.

========== Id ==========  
334

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#334-Why-should-not-call-setstate-in-componentw

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
