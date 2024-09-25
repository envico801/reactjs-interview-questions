========== Question ==========  

### What are error boundaries in React v16?  

========== Answer ==========  

_Error boundaries_ are components that catch JavaScript errors anywhere in their
child component tree, log those errors, and display a fallback UI instead of the
component tree that crashed.

A class component becomes an error boundary if it defines a new lifecycle method
called `componentDidCatch(error, info)` or `static getDerivedStateFromError() `:

```jsx
class ErrorBoundary extends React.Component {
    constructor(props) {
        super(props);
        this.state = { hasError: false };
    }
    componentDidCatch(error, info) {
        // You can also log the error to an error reporting service
        logErrorToMyService(error, info);
    }
    static getDerivedStateFromError(error) {
        // Update state so the next render will show the fallback UI.
        return { hasError: true };
    }
    render() {
        if (this.state.hasError) {
            // You can render any custom fallback UI
            return <h1>{'Something went wrong.'}</h1>;
        }
        return this.props.children;
    }
}
```

After that use it as a regular component:

```jsx
<ErrorBoundary>
    <MyWidget />
</ErrorBoundary>
```

========== Id ==========  
287

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#287-What-are-error-boundaries-in-react-v16

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
