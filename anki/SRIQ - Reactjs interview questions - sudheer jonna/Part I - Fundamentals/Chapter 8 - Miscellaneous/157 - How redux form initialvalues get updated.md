========== Question ==========  

### How Redux Form `initialValues` get updated from state?  

========== Answer ==========  

You need to add `enableReinitialize : true` setting.

```javascript
const InitializeFromStateForm = reduxForm({
    form: 'initializeFromState',
    enableReinitialize: true,
})(UserEdit);
```

If your `initialValues` prop gets updated, your form will update too.

========== Id ==========  
157

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#157-How-redux-form-initialvalues-get-updated

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
