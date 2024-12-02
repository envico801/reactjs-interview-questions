========== Question ==========  

### How do you programmatically navigate using React Router v4?  

========== Answer ==========  

There are three different ways to achieve programmatic routing/navigation within components.

1.  **Using the `withRouter()` higher-order function:**

    The `withRouter()` higher-order function will inject the history object as a prop of the component. This object provides `push()` and `replace()` methods to avoid the usage of context.

    ```jsx
    import { withRouter } from "react-router-dom"; // this also works with 'react-router-native'
    const Button = withRouter(({ history }) => (
      <button
        type="button"
        onClick={() => {
          history.push("/new-location");
        }}
      >
        {"Click Me!"}
      </button>
    ));
    ```

2.  **Using `<Route>` component and render props pattern:**

    The `<Route>` component passes the same props as `withRouter()`, so you will be able to access the history methods through the history prop.

    ```jsx
    import { Route } from "react-router-dom";
    const Button = () => (
      <Route
        render={({ history }) => (
          <button
            type="button"
            onClick={() => {
              history.push("/new-location");
            }}
          >
            {"Click Me!"}
          </button>
        )}
      />
    );
    ```

3.  **Using context:**

    This option is not recommended and treated as unstable API.

    ```jsx
    const Button = (props, context) => (
      <button
        type="button"
        onClick={() => {
          context.history.push("/new-location");
        }}
      >
        {"Click Me!"}
      </button>
    );
    Button.contextTypes = {
      history: React.PropTypes.shape({
        push: React.PropTypes.func.isRequired,
      }),
    };
    ```

========== Id ==========  
83

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 2 - React Router

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-2-React-Router::#83-How-do-you-programmatically-navigate-using

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
