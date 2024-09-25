========== Question ==========  

### What is the methods order when component re-rendered?  

========== Answer ==========  

An update can be caused by changes to props or state. The below methods are
called in the following order when a component is being re-rendered.

1.  static getDerivedStateFromProps()

2.  shouldComponentUpdate()

3.  render()

4.  getSnapshotBeforeUpdate()

5.  componentDidUpdate()

========== Id ==========  
336

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#336-What-is-the-methods-order-when-component-r

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
