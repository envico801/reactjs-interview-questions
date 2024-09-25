========== Question ==========  

### What are HOC factory implementations?  

========== Answer ==========  

There are two main ways of implementing HOCs in React.

1.  Props Proxy (PP) and

2.  Inheritance Inversion (II).

But they follow different approaches for manipulating the _WrappedComponent_.

**Props Proxy**

In this approach, the render method of the HOC returns a React Element of the
type of the WrappedComponent. We also pass through the props that the HOC
receives, hence the name **Props Proxy**.

```jsx
function ppHOC(WrappedComponent) {
    return class PP extends React.Component {
        render() {
            return <WrappedComponent {...this.props} />;
        }
    };
}
```

**Inheritance Inversion**

In this approach, the returned HOC class (Enhancer) extends the
WrappedComponent. It is called Inheritance Inversion because instead of the
WrappedComponent extending some Enhancer class, it is passively extended by the
Enhancer. In this way the relationship between them seems **inverse**.

```jsx
function iiHOC(WrappedComponent) {
    return class Enhancer extends WrappedComponent {
        render() {
            return super.render();
        }
    };
}
```

========== Id ==========  
326

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#326-What-are-hoc-factory-implementations

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
