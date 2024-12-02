========== Question ==========  

### What is the main purpose of constructor?  

========== Answer ==========  

The constructor is mainly used for two purposes,

1.  To initialize local state by assigning object to this.state

2.  For binding event handler methods to the instance

    For example, the below code covers both the above cases,

```javascript
constructor(props) {
  super(props);
  // Don't call this.setState() here!
  this.state = { counter: 0 };
  this.handleClick = this.handleClick.bind(this);
}
```

========== Id ==========  
332

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#332-What-is-the-main-purpose-of-constructor

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
