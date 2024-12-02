========== Question ==========  

### What are the different ways to write `mapDispatchToProps()`?  

========== Answer ==========  

There are a few ways of binding _action creators_ to `dispatch()` in `mapDispatchToProps()`.

Below are the possible options:

```javascript
const mapDispatchToProps = (dispatch) => ({
    action: () => dispatch(action()),
});
```

```javascript
const mapDispatchToProps = (dispatch) => ({
    action: bindActionCreators(action, dispatch),
});
```

```javascript
const mapDispatchToProps = { action };
```

The third option is just a shorthand for the first one.

========== Id ==========  
119

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#119-What-are-the-different-ways-to-write-mapd

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
