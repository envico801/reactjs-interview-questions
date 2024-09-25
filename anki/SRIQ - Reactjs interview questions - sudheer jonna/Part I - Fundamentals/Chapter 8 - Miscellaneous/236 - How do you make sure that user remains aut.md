========== Question ==========  

### How do you make sure that user remains authenticated on page refresh while using Context API State Management?  

========== Answer ==========  

When a user logs in and reload, to persist the state generally we add the load
user action in the useEffect hooks in the main App.js. While using Redux,
loadUser action can be easily accessed.

**App.js**

```js
import { loadUser } from '../actions/auth';
store.dispatch(loadUser());
```

-   But while using **Context API**, to access context in App.js, wrap the
    AuthState in index.js so that App.js can access the auth context. Now
    whenever the page reloads, no matter what route you are on, the user will be
    authenticated as **loadUser** action will be triggered on each re-render.

**index.js**

```js
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';
import AuthState from './context/auth/AuthState';
ReactDOM.render(
    <React.StrictMode>
        <AuthState>
            <App />
        </AuthState>
    </React.StrictMode>,
    document.getElementById('root'),
);
```

**App.js**

```js
const authContext = useContext(AuthContext);
const { loadUser } = authContext;
useEffect(() => {
    loadUser();
}, []);
```

**loadUser**

```js
const loadUser = async () => {
    const token = sessionStorage.getItem('token');
    if (!token) {
        dispatch({
            type: ERROR,
        });
    }
    setAuthToken(token);
    try {
        const res = await axios('/api/auth');
        dispatch({
            type: USER_LOADED,
            payload: res.data.data,
        });
    } catch (err) {
        console.error(err);
    }
};
```

========== Id ==========  
236

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#236-How-do-you-make-sure-that-user-remains-aut

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
