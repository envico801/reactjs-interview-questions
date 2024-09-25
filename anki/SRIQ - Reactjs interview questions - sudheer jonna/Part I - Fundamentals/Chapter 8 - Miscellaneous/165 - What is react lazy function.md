========== Question ==========  

### What is React lazy function?  

========== Answer ==========  

The `React.lazy` function lets you render a dynamic import as a regular
component. It will automatically load the bundle containing the `OtherComponent`
when the component gets rendered. This must return a Promise which resolves to a
module with a default export containing a React component.

```jsx
const OtherComponent = React.lazy(() => import('./OtherComponent'));
function MyComponent() {
    return (
        <div>
            <OtherComponent />
        </div>
    );
}
```

**Note:**

`React.lazy` and `Suspense` is not yet available for server-side rendering. If
you want to do code-splitting in a server rendered app, we still recommend React
Loadable.

========== Id ==========  
165

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#165-What-is-react-lazy-function

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
