========== Question ==========  

### Why is `isMounted()` an anti-pattern and what is the proper solution?  

========== Answer ==========  

The primary use case for `isMounted()` is to avoid calling `setState()` after a
component has been unmounted, because it will emit a warning.

```javascript
if (this.isMounted()) {
  this.setState({...})
}
```

Checking `isMounted()` before calling `setState()` does eliminate the warning,
but it also defeats the purpose of the warning. Using `isMounted()` is a code
smell because the only reason you would check is because you think you might be
holding a reference after the component has unmounted.

An optimal solution would be to find places where `setState()` might be called
after a component has unmounted, and fix them. Such situations most commonly
occur due to callbacks, when a component is waiting for some data and gets
unmounted before the data arrives. Ideally, any callbacks should be canceled in
`componentWillUnmount()`, prior to unmounting.

========== Id ==========  
302

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#302-Why-is-ismounted-an-anti-pattern-and-w

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
