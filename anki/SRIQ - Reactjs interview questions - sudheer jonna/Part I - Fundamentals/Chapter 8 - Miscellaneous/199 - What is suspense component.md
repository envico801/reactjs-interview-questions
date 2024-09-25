========== Question ==========  

### What is suspense component?  

========== Answer ==========  

If the module containing the dynamic import is not yet loaded by the time parent
component renders, you must show some fallback content while you’re waiting for
it to load using a loading indicator. This can be done using **Suspense**
component.

For example, the below code uses suspense component,

```javascript
const OtherComponent = React.lazy(() => import('./OtherComponent'));
function MyComponent() {
    return (
        <div>
            <Suspense fallback={<div>Loading...</div>}>
                <OtherComponent />
            </Suspense>
        </div>
    );
}
```

As mentioned in the above code, Suspense is wrapped above the lazy component.

========== Id ==========  
199

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#199-What-is-suspense-component

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
