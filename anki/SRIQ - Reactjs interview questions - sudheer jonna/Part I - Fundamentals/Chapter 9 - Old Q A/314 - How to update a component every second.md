========== Question ==========  

### How to update a component every second?  

========== Answer ==========  

You need to use `setInterval()` to trigger the change, but you also need to
clear the timer when the component unmounts to prevent errors and memory leaks.

```javascript
componentDidMount() {
  this.interval = setInterval(() => this.setState({ time: Date.now() }), 1000)
}
componentWillUnmount() {
  clearInterval(this.interval)
}
```

========== Id ==========  
314

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#314-How-to-update-a-component-every-second

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
