========== Question ==========  

### How to implement _default_ or _NotFound_ page?  

========== Answer ==========  

A `<Switch>` renders the first child `<Route>` that matches. A `<Route>` with no path always matches. So you just need to simply drop path attribute as below

```jsx
<Switch>
    <Route exact path='/' component={Home} />
    <Route path='/user' component={User} />
    <Route component={NotFound} />
</Switch>
```

========== Id ==========  
87

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 2 - React Router

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-2-React-Router::#87-How-to-implement-default-or-notfound-p

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
