========== Question ==========  

### What are the advantages of formik over redux form library?  

========== Answer ==========  

Below are the main reasons to recommend formik over redux form library,

1.  The form state is inherently short-term and local, so tracking it in Redux
    (or any kind of Flux library) is unnecessary.

2.  Redux-Form calls your entire top-level Redux reducer multiple times ON EVERY
    SINGLE KEYSTROKE. This way it increases input latency for large apps.

3.  Redux-Form is 22.5 kB minified gzipped whereas Formik is 12.7 kB

========== Id ==========  
194

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#194-What-are-the-advantages-of-formik-over-red

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
