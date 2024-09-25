========== Question ==========  

### What is the purpose of getDerivedStateFromError?  

========== Answer ==========  

This lifecycle method is invoked after an error has been thrown by a descendant
component. It receives the error that was thrown as a parameter and should
return a value to update state.

The signature of the lifecycle method is as follows,

```javascript
static getDerivedStateFromError(error)
```

Let us take error boundary use case with the above lifecycle method for
demonstration purpose,

```javascript
class ErrorBoundary extends React.Component {
    constructor(props) {
        super(props);
        this.state = { hasError: false };
    }
    static getDerivedStateFromError(error) {
        // Update state so the next render will show the fallback UI.
        return { hasError: true };
    }
    render() {
        if (this.state.hasError) {
            // You can render any custom fallback UI
            return <h1>Something went wrong.</h1>;
        }
        return this.props.children;
    }
}
```

========== Id ==========  
335

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#335-What-is-the-purpose-of-getderivedstatefrom

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
