========== Question ==========  

### How you implement Server Side Rendering or SSR?  

========== Answer ==========  

React is already equipped to handle rendering on Node servers. A special version
of the DOM renderer is available, which follows the same pattern as on the
client side.

```jsx
import ReactDOMServer from 'react-dom/server';
import App from './App';
ReactDOMServer.renderToString(<App />);
```

This method will output the regular HTML as a string, which can be then placed
inside a page body as part of the server response. On the client side, React
detects the pre-rendered content and seamlessly picks up where it left off.

========== Id ==========  
49

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#49-How-you-implement-server-side-rendering-or

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
