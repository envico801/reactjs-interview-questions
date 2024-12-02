========== Question ==========  

### How can we find the version of React at runtime in the browser?  

========== Answer ==========  

You can use `React.version` to get the version.

```jsx
const REACT_VERSION = React.version;

ReactDOM.render(
    <div>{`React version: ${REACT_VERSION}`}</div>,
    document.getElementById('app'),
);
```

========== Id ==========  
69

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#69-How-can-we-find-the-version-of-react-at-ru

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
