========== Question ==========  

### What is the benefit of strict mode?  

========== Answer ==========  

The <StrictMode> will be helpful in the below cases,

1.  To find the bugs caused by impure rendering where the components will re-render twice.

2.  To find the bugs caused by missing cleanup of effects where the components will re-run effects one more extra time.

3.  Identifying components with **unsafe lifecycle methods**.

4.  Warning about **legacy string ref** API usage.

5.  Detecting unexpected **side effects**.

6.  Detecting **legacy context** API.

7.  Warning about deprecated **findDOMNode** usage

========== Id ==========  
246

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#246-What-is-the-benefit-of-strict-mode

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
