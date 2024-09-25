========== Question ==========  

### How to use `connect()` from React Redux?  

========== Answer ==========  

You need to follow two steps to use your store in your container:

1.  **Use `mapStateToProps()`:** It maps the state variables from your store to
    the props that you specify.

2.  **Connect the above props to your container:** The object returned by the
    `mapStateToProps` function is connected to the container. You can import
    `connect()` from `react-redux`.

    ```jsx
    import React from 'react';
    import { connect } from 'react-redux';
    class App extends React.Component {
        render() {
            return <div>{this.props.containerData}</div>;
        }
    }
    function mapStateToProps(state) {
        return { containerData: state.data };
    }
    export default connect(mapStateToProps)(App);
    ```

========== Id ==========  
321

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#321-How-to-use-connect-from-react-redux

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
