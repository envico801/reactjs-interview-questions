========== Question ==========  

### How to set state with a dynamic key name?  

========== Answer ==========  

If you are using ES6 or the Babel transpiler to transform your JSX code then you can accomplish this with _computed property names_.

```javascript
handleInputChange(event) {
  this.setState({ [event.target.id]: event.target.value })
}
```

========== Id ==========  
285

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#285-How-to-set-state-with-a-dynamic-key-name

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
