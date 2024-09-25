========== Question ==========  

### What are the lifecycle methods going to be deprecated in React v16?  

========== Answer ==========  

The following lifecycle methods going to be unsafe coding practices and will be
more problematic with async rendering.

1. `componentWillMount()`

2. `componentWillReceiveProps()`

3. `componentWillUpdate()`

Starting with React v16.3 these methods are aliased with `UNSAFE_` prefix, and
the unprefixed version will be removed in React v17.

========== Id ==========  
296

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#296-What-are-the-lifecycle-methods-going-to-be

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
