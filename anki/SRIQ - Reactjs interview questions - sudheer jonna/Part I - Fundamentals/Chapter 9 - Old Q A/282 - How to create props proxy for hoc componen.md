========== Question ==========  

### How to create props proxy for HOC component?  

========== Answer ==========  

You can add/edit props passed to the component using _props proxy_ pattern like this:

```jsx
function HOC(WrappedComponent) {
    return class Test extends Component {
        render() {
            const newProps = {
                title: 'New Header',
                footer: false,
                showFeatureX: false,
                showFeatureY: true,
            };
            return <WrappedComponent {...this.props} {...newProps} />;
        }
    };
}
```

========== Id ==========  
282

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#282-How-to-create-props-proxy-for-hoc-componen

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
