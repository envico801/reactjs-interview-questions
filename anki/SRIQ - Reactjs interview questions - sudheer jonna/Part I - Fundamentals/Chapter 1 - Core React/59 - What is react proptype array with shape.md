========== Question ==========  

### What is React proptype array with shape?  

========== Answer ==========  

If you want to pass an array of objects to a component with a particular shape
then use `React.PropTypes.shape()` as an argument to
`React.PropTypes.arrayOf()`.

```javascript
ReactComponent.propTypes = {
    arrayWithShape: React.PropTypes.arrayOf(
        React.PropTypes.shape({
            color: React.PropTypes.string.isRequired,
            fontSize: React.PropTypes.number.isRequired,
        }),
    ).isRequired,
};
```

========== Id ==========  
59

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#59-What-is-react-proptype-array-with-shape

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
