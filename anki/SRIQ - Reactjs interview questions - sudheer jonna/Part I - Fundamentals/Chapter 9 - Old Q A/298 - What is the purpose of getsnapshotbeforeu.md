========== Question ==========  

### What is the purpose of `getSnapshotBeforeUpdate()` lifecycle method?  

========== Answer ==========  

The new `getSnapshotBeforeUpdate()` lifecycle method is called right before DOM
updates. The return value from this method will be passed as the third parameter
to `componentDidUpdate()`.

```javascript
class MyComponent extends React.Component {
    getSnapshotBeforeUpdate(prevProps, prevState) {
        // ...
    }
}
```

This lifecycle method along with `componentDidUpdate()` covers all the use cases
of `componentWillUpdate()`.

========== Id ==========  
298

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#298-What-is-the-purpose-of-getsnapshotbeforeu

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
