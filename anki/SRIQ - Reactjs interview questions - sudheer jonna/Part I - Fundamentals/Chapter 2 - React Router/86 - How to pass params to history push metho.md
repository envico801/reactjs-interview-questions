========== Question ==========  

### How to pass params to `history.push` method in React Router v4?  

========== Answer ==========  

While navigating you can pass props to the `history` object:

```javascript
this.props.history.push({
    pathname: '/template',
    search: '?name=sudheer',
    state: { detail: response.data },
});
```

The `search` property is used to pass query params in `push()` method.

========== Id ==========  
86

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 2 - React Router

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-2-React-Router::#86-How-to-pass-params-to-history-push-metho

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
