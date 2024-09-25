========== Question ==========  

### What are portals in React?  

========== Answer ==========  

_Portal_ is a recommended way to render children into a DOM node that exists
outside the DOM hierarchy of the parent component. When using

CSS transform in a component, its descendant elements should not use fixed
positioning, otherwise the layout will blow up.

```javascript
ReactDOM.createPortal(child, container);
```

The first argument is any render-able React child, such as an element, string,
or fragment. The second argument is a DOM element.

========== Id ==========  
33

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#33-What-are-portals-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
