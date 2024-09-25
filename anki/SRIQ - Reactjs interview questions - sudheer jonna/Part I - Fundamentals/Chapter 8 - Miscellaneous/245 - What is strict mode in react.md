========== Question ==========  

### What is strict mode in React?  

========== Answer ==========  

`React.StrictMode` is a useful component for highlighting potential problems in
an application. Just like `<Fragment>`, `<StrictMode>` does not render any extra
DOM elements. It activates additional checks and warnings for its descendants.
These checks apply for _development mode_ only.

```jsx
import { StrictMode } from 'react';
function App() {
    return (
        <div>
            <Header />
            <StrictMode>
                <div>
                    <ComponentOne />
                    <ComponentTwo />
                </div>
            </StrictMode>
            <Header />
        </div>
    );
}
```

In the example above, the _strict mode_ checks apply to `<ComponentOne>` and
`<ComponentTwo>` components only. i.e., Part of the application only.

**Note:** Frameworks such as NextJS has this flag enabled by default.

========== Id ==========  
245

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#245-What-is-strict-mode-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
