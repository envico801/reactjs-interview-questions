========== Question ==========  

### How to make AJAX request in Redux?  

========== Answer ==========  

You can use `redux-thunk` middleware which allows you to define async actions.

Let's take an example of fetching specific account as an AJAX call using _fetch
API_:

```javascript
export function fetchAccount(id) {
    return (dispatch) => {
        dispatch(setLoadingAccountState()); // Show a loading spinner
        fetch(`/account/${id}`, (response) => {
            dispatch(doneFetchingAccount()); // Hide loading spinner
            if (response.status === 200) {
                dispatch(setAccount(response.json)); // Use a normal function to set the received state
            } else {
                dispatch(someError);
            }
        });
    };
}
function setAccount(data) {
    return { type: 'SET_Account', data: data };
}
```

========== Id ==========  
114

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#114-How-to-make-ajax-request-in-redux

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
