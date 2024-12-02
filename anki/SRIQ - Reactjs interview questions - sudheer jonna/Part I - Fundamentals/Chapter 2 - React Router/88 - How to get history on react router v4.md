========== Question ==========  

### How to get history on React Router v4?  

========== Answer ==========  

Below are the list of steps to get history object on React Router v4,

1.  Create a module that exports a `history` object and import this module across the project.

    For example, create `history.js` file:

    ```javascript
    import { createBrowserHistory } from 'history';
    export default createBrowserHistory({
        /* pass a configuration object here if needed */
    });
    ```

2.  You should use the `<Router>` component instead of built-in routers. Import the above `history.js` inside `index.js` file:

    ```jsx
    import { Router } from 'react-router-dom';
    import history from './history';
    import App from './App';
    ReactDOM.render(
        <Router history={history}>
            <App />
        </Router>,
        holder,
    );
    ```

3.  You can also use push method of `history` object similar to built-in history object:

    ```javascript
    // some-other-file.js
    import history from './history';
    history.push('/go-here');
    ```

========== Id ==========  
88

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 2 - React Router

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-2-React-Router::#88-How-to-get-history-on-react-router-v4

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
