========== Question ==========  

### How do you create HOC using render props?  

========== Answer ==========  

You can implement most higher-order components (HOC) using a regular component with a render prop. For example, if you would prefer to have a withMouse HOC instead of a <Mouse> component, you could easily create one using a regular <Mouse> with a render prop.

```javascript
function withMouse(Component) {
    return class extends React.Component {
        render() {
            return (
                <Mouse
                    render={(mouse) => (
                        <Component {...this.props} mouse={mouse} />
                    )}
                />
            );
        }
    };
}
```

This way render props gives the flexibility of using either pattern.

========== Id ==========  
354

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#354-How-do-you-create-hoc-using-render-props

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
