========== Question ==========  

### How to perform automatic redirect after login?  

========== Answer ==========  

The `react-router` package provides `<Redirect>` component in React Router. Rendering a `<Redirect>` will navigate to a new location. Like server-side redirects, the new location will override the current location in the history stack.

```javascript
import { Redirect } from "react-router";
export default function Login {
    if (this.state.isLoggedIn === true) {
      return <Redirect to="/your/redirect/page" />;
    } else {
      return <div>{"Login Please"}</div>;
    }
}
```

  <details><summary><b>See Class</b></summary>

  <p>

```jsx
import React, { Component } from 'react';
import { Redirect } from 'react-router';
export default class LoginComponent extends Component {
    render() {
        if (this.state.isLoggedIn === true) {
            return <Redirect to='/your/redirect/page' />;
        } else {
            return <div>{'Login Please'}</div>;
        }
    }
}
```

   </p>

   </details>

========== Id ==========  
89

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 2 - React Router

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-2-React-Router::#89-How-to-perform-automatic-redirect-after-lo

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
