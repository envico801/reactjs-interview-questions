========== Question ==========  

### When to use a Class Component over a Function Component?  

========== Answer ==========  

After the addition of Hooks(i.e. React 16.8 onwards) it is always recommended to
use Function components over Class components in React. Because you could use
state, lifecycle methods and other features that were only available in class
component present in function component too.

But even there are two reasons to use Class components over Function components.

1. If you need a React functionality whose Function component equivalent is not
   present yet, like Error Boundaries.

2. In older versions, If the component needs _state or lifecycle methods_ then
   you need to use class component.

So the summary to this question is as follows:

**Use Function Components:**

-   If you don't need state or lifecycle methods, and your component is purely
    presentational.

-   For simplicity, readability, and modern code practices, especially with the
    use of React Hooks for state and side effects.

**Use Class Components:**

-   If you need to manage state or use lifecycle methods.

-   In scenarios where backward compatibility or integration with older code is
    necessary.

**Note:** You can also use reusable
[react error boundary](https://github.com/bvaughn/react-error-boundary)
third-party component without writing any class. i.e, No need to use class
components for Error boundaries.

The usage of Error boundaries from the above library is quite straight forward.

> **_Note when using react-error-boundary:_** ErrorBoundary is a client
> component. You can only pass props to it that are serializable or use it in
> files that have a `"use client";` directive.

```jsx
'use client';
import { ErrorBoundary } from 'react-error-boundary';
<ErrorBoundary fallback={<div>Something went wrong</div>}>
    <ExampleApplication />
</ErrorBoundary>;
```

========== Id ==========  
7

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#7-When-to-use-a-class-component-over-a-funct

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
