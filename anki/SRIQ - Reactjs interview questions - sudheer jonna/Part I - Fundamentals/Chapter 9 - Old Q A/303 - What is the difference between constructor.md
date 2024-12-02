========== Question ==========  

### What is the difference between constructor and getInitialState?  

========== Answer ==========  

You should initialize state in the constructor when using ES6 classes, and `getInitialState()` method when using `React.createClass()`.

**Using ES6 classes:**

```javascript
class MyComponent extends React.Component {
    constructor(props) {
        super(props);
        this.state = {
            /* initial state */
        };
    }
}
```

**Using `React.createClass()`:**

```javascript
const MyComponent = React.createClass({
    getInitialState() {
        return {
            /* initial state */
        };
    },
});
```

**Note:** `React.createClass()` is deprecated and removed in React v16. Use plain JavaScript classes instead.

========== Id ==========  
303

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#303-What-is-the-difference-between-constructor

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
