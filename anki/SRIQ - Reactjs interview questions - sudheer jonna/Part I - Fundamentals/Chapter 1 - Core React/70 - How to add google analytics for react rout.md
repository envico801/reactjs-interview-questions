========== Question ==========  

### How to add Google Analytics for React Router?  

========== Answer ==========  

Add a listener on the `history` object to record each page view:

```javascript
history.listen(function (location) {
    window.ga('set', 'page', location.pathname + location.search);
    window.ga('send', 'pageview', location.pathname + location.search);
});
```

========== Id ==========  
70

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#70-How-to-add-google-analytics-for-react-rout

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
