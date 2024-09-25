========== Question ==========  

### Which is preferred option with in callback refs and findDOMNode()?  

========== Answer ==========  

It is preferred to use _callback refs_ over `findDOMNode()` API. Because
`findDOMNode()` prevents certain improvements in React in the future.

The **legacy** approach of using `findDOMNode`:

```javascript
class MyComponent extends Component {
    componentDidMount() {
        findDOMNode(this).scrollIntoView();
    }
    render() {
        return <div />;
    }
}
```

The recommended approach is:

```javascript
class MyComponent extends Component {
    constructor(props) {
        super(props);
        this.node = createRef();
    }
    componentDidMount() {
        this.node.current.scrollIntoView();
    }
    render() {
        return <div ref={this.node} />;
    }
}
```

========== Id ==========  
278

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#278-Which-is-preferred-option-with-in-callback

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
