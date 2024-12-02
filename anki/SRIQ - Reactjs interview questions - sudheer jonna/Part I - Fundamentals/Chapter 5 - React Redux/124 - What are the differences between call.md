========== Question ==========  

### What are the differences between `call()` and `put()` in redux-saga?  

========== Answer ==========  

Both `call()` and `put()` are effect creator functions. `call()` function is used to create effect description, which instructs middleware to call the promise. `put()` function creates an effect, which instructs middleware to dispatch an action to the store.

Let's take example of how these effects work for fetching particular user data.

```javascript
function* fetchUserSaga(action) {
    // `call` function accepts rest arguments, which will be passed to `api.fetchUser` function.
    // Instructing middleware to call promise, it resolved value will be assigned to `userData` variable
    const userData = yield call(api.fetchUser, action.userId);

    // Instructing middleware to dispatch corresponding action.
    yield put({
        type: 'FETCH_USER_SUCCESS',
        userData,
    });
}
```

========== Id ==========  
124

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#124-What-are-the-differences-between-call

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
