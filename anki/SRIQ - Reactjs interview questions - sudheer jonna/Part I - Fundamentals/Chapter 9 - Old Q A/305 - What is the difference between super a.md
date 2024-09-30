========== Question ==========  

### What is the difference between `super()` and `super(props)` in React using ES6 classes?  

========== Answer ==========  

When you want to access `this.props` in `constructor()` then you should pass props to `super()` method.

**Using `super(props)`:**

```javascript
class MyComponent extends React.Component {
    constructor(props) {
        super(props);
        console.log(this.props); // { name: 'John', ... }
    }
}
```

**Using `super()`:**

```javascript
class MyComponent extends React.Component {
    constructor(props) {
        super();
        console.log(this.props); // undefined
    }
}
```

Outside `constructor()` both will display same value for `this.props`.

========== Id ==========  
305

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#305-What-is-the-difference-between-super-a

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
