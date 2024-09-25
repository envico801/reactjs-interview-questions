========== Question ==========  

### What will happen if you use props in initial state?  

========== Answer ==========  

If the props on the component are changed without the component being refreshed,
the new prop value will never be displayed because the constructor function will
never update the current state of the component. The initialization of state
from props only runs when the component is first created.

The below component won't display the updated input value:

```jsx
class MyComponent extends React.Component {
    constructor(props) {
        super(props);
        this.state = {
            records: [],
            inputValue: this.props.inputValue,
        };
    }
    render() {
        return <div>{this.state.inputValue}</div>;
    }
}
```

Using props inside render method will update the value:

```jsx
class MyComponent extends React.Component {
    constructor(props) {
        super(props);
        this.state = {
            record: [],
        };
    }
    render() {
        return <div>{this.props.inputValue}</div>;
    }
}
```

========== Id ==========  
292

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#292-What-will-happen-if-you-use-props-in-initi

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
