========== Question ==========  

### Does the lazy function support named exports?  

========== Answer ==========  

No, currently `React.lazy` function supports default exports only. If you would like to import modules which are named exports, you can create an intermediate module that reexports it as the default. It also ensures that tree shaking keeps working and don’t pull unused components.

Let's take a component file which exports multiple named components,

```javascript
// MoreComponents.js
export const SomeComponent = /* ... */;
export const UnusedComponent = /* ... */;
```

and reexport `MoreComponents.js` components in an intermediate file `IntermediateComponent.js`

```javascript
// IntermediateComponent.js
export { SomeComponent as default } from './MoreComponents.js';
```

Now you can import the module using lazy function as below,

```javascript
import React, { lazy } from 'react';
const SomeComponent = lazy(() => import('./IntermediateComponent.js'));
```

========== Id ==========  
29

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#29-Does-the-lazy-function-support-named-expor

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
