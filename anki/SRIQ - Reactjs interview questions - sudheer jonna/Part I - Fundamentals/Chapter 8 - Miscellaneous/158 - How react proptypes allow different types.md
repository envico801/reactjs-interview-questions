========== Question ==========  

### How React PropTypes allow different types for one prop?  

========== Answer ==========  

You can use `oneOfType()` method of `PropTypes`.

For example, the height property can be defined with either `string` or `number` type as below:

```javascript
Component.propTypes = {
    size: PropTypes.oneOfType([PropTypes.string, PropTypes.number]),
};
```

========== Id ==========  
158

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#158-How-react-proptypes-allow-different-types

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
