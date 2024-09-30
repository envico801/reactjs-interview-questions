========== Question ==========  

### Whats the purpose of `at` symbol in the Redux connect decorator?  

========== Answer ==========  

The **@** symbol is in fact a JavaScript expression used to signify decorators. _Decorators_ make it possible to annotate and modify classes and properties at design time.

Let's take an example setting up Redux without and with a decorator.

-   **Without decorator:**

    ```javascript
    import React from 'react';
    import * as actionCreators from './actionCreators';
    import { bindActionCreators } from 'redux';
    import { connect } from 'react-redux';
    function mapStateToProps(state) {
        return { todos: state.todos };
    }
    function mapDispatchToProps(dispatch) {
        return { actions: bindActionCreators(actionCreators, dispatch) };
    }
    class MyApp extends React.Component {
        // ...define your main app here
    }
    export default connect(mapStateToProps, mapDispatchToProps)(MyApp);
    ```

-   **With decorator:**

    ```javascript
    import React from 'react';
    import * as actionCreators from './actionCreators';
    import { bindActionCreators } from 'redux';
    import { connect } from 'react-redux';
    function mapStateToProps(state) {
        return { todos: state.todos };
    }
    function mapDispatchToProps(dispatch) {
        return { actions: bindActionCreators(actionCreators, dispatch) };
    }
    @connect(mapStateToProps, mapDispatchToProps)
    export default class MyApp extends React.Component {
        // ...define your main app here
    }
    ```

The above examples are almost similar except the usage of decorator. The decorator syntax isn't built into any JavaScript runtimes yet, and is still experimental and subject to change. You can use babel for the decorators support.

========== Id ==========  
322

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#322-Whats-the-purpose-of-at-symbol-in-the-re

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
