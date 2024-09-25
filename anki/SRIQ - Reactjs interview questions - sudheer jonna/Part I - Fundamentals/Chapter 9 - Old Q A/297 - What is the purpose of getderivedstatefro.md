========== Question ==========  

### What is the purpose of `getDerivedStateFromProps()` lifecycle method?  

========== Answer ==========  

The new static `getDerivedStateFromProps()` lifecycle method is invoked after a
component is instantiated as well as before it is re-rendered. It can return an
object to update state, or `null` to indicate that the new props do not require
any state updates.

```javascript
class MyComponent extends React.Component {
    static getDerivedStateFromProps(props, state) {
        // ...
    }
}
```

This lifecycle method along with `componentDidUpdate()` covers all the use cases
of `componentWillReceiveProps()`.

========== Id ==========  
297

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#297-What-is-the-purpose-of-getderivedstatefro

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
