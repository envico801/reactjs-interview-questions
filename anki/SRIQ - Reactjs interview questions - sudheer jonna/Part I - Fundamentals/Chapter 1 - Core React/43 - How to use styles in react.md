========== Question ==========  

### How to use styles in React?  

========== Answer ==========  

The `style` attribute accepts a JavaScript object with camelCased properties
rather than a CSS string. This is consistent with the DOM style JavaScript
property, is more efficient, and prevents XSS security holes.

```jsx
const divStyle = {
    color: 'blue',
    backgroundImage: 'url(' + imgUrl + ')',
};
function HelloWorldComponent() {
    return <div style={divStyle}>Hello World!</div>;
}
```

Style keys are camelCased in order to be consistent with accessing the
properties on DOM nodes in JavaScript (e.g. `node.style.backgroundImage`).

========== Id ==========  
43

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#43-How-to-use-styles-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
