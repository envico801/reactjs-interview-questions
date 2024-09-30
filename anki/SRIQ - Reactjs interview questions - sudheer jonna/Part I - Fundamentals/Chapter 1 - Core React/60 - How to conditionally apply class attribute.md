========== Question ==========  

### How to conditionally apply class attributes?  

========== Answer ==========  

You shouldn't use curly braces inside quotes because it is going to be evaluated as a string.

```jsx
<div className="btn-panel {this.props.visible ? 'show' : 'hidden'}">
```

Instead you need to move curly braces outside (don't forget to include spaces between class names):

```jsx
<div className={'btn-panel ' + (this.props.visible ? 'show' : 'hidden')}>
```

_Template strings_ will also work:

```jsx
<div className={`btn-panel ${this.props.visible ? 'show' : 'hidden'}`}>
```

========== Id ==========  
60

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#60-How-to-conditionally-apply-class-attribute

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
