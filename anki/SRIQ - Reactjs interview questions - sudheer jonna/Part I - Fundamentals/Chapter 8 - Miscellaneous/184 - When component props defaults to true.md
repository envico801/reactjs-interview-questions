========== Question ==========  

### When component props defaults to true?  

========== Answer ==========  

If you pass no value for a prop, it defaults to true. This behavior is available
so that it matches the behavior of HTML.

For example, below expressions are equivalent,

```javascript
<MyInput autocomplete />
<MyInput autocomplete={true} />
```

**Note:** It is not recommended to use this approach because it can be confused
with the ES6 object shorthand (example, `{name}` which is short for
`{name: name}`)

========== Id ==========  
184

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#184-When-component-props-defaults-to-true

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
