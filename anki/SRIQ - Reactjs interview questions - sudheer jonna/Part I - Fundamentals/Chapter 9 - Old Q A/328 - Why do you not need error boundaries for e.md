========== Question ==========  

### Why do you not need error boundaries for event handlers?  

========== Answer ==========  

Error boundaries do not catch errors inside event handlers.

React doesn’t need error boundaries to recover from errors in event handlers. Unlike the render method and lifecycle methods, the event handlers don’t happen during rendering. So if they throw, React still knows what to display on the screen.

If you need to catch an error inside an event handler, use the regular JavaScript try / catch statement:

```javascript
class MyComponent extends React.Component {
    constructor(props) {
        super(props);
        this.state = { error: null };
        this.handleClick = this.handleClick.bind(this);
    }

    handleClick() {
        try {
            // Do something that could throw
        } catch (error) {
            this.setState({ error });
        }
    }

    render() {
        if (this.state.error) {
            return <h1>Caught an error.</h1>;
        }
        return <button onClick={this.handleClick}>Click Me</button>;
    }
}
```

Note that the above example is demonstrating regular JavaScript behavior and doesn’t use error boundaries.

========== Id ==========  
328

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#328-Why-do-you-not-need-error-boundaries-for-e

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
