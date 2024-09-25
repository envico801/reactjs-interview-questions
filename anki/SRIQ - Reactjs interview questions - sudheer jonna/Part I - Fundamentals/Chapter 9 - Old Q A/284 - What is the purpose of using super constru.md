========== Question ==========  

### What is the purpose of using super constructor with props argument?  

========== Answer ==========  

A child class constructor cannot make use of `this` reference until the
`super()` method has been called. The same applies to ES6 sub-classes as well.
The main reason for passing props parameter to `super()` call is to access
`this.props` in your child constructors.

**Passing props:**

```javascript
class MyComponent extends React.Component {
    constructor(props) {
        super(props);
        console.log(this.props); // prints { name: 'John', age: 42 }
    }
}
```

**Not passing props:**

```javascript
class MyComponent extends React.Component {
    constructor(props) {
        super();
        console.log(this.props); // prints undefined
        // but props parameter is still available
        console.log(props); // prints { name: 'John', age: 42 }
    }
    render() {
        // no difference outside constructor
        console.log(this.props); // prints { name: 'John', age: 42 }
    }
}
```

The above code snippets reveals that `this.props` is different only within the
constructor. It would be the same outside the constructor.

========== Id ==========  
284

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#284-What-is-the-purpose-of-using-super-constru

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
