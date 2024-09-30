========== Question ==========  

### How to debug forwardRefs in DevTools?  

========== Answer ==========  

**React.forwardRef** accepts a render function as parameter and DevTools uses this function to determine what to display for the ref forwarding component.

For example, If you don't name the render function or not using displayName property then it will appear as ”ForwardRef” in the DevTools,

```javascript
const WrappedComponent = React.forwardRef((props, ref) => {
    return <LogProps {...props} forwardedRef={ref} />;
});
```

But If you name the render function then it will appear as **”ForwardRef(myFunction)”**

```javascript
const WrappedComponent = React.forwardRef(function myFunction(props, ref) {
    return <LogProps {...props} forwardedRef={ref} />;
});
```

As an alternative, You can also set displayName property for forwardRef function,

```javascript
function logProps(Component) {
    class LogProps extends React.Component {
        // ...
    }
    function forwardRef(props, ref) {
        return <LogProps {...props} forwardedRef={ref} />;
    }
    // Give this component a more helpful display name in DevTools.
    // e.g. "ForwardRef(logProps(MyComponent))"
    const name = Component.displayName || Component.name;
    forwardRef.displayName = `logProps(${name})`;
    return React.forwardRef(forwardRef);
}
```

========== Id ==========  
340

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#340-How-to-debug-forwardrefs-in-devtools

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
