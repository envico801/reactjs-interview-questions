========== Question ==========  

### What are forward refs?  

========== Answer ==========  

_Ref forwarding_ is a feature that lets some components take a _ref_ they
receive, and pass it further down to a child.

```jsx
const ButtonElement = React.forwardRef((props, ref) => (
    <button ref={ref} className='CustomButton'>
        {props.children}
    </button>
));
// Create ref to the DOM button:
const ref = React.createRef();
<ButtonElement ref={ref}>{'Forward Ref'}</ButtonElement>;
```

========== Id ==========  
277

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#277-What-are-forward-refs

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
