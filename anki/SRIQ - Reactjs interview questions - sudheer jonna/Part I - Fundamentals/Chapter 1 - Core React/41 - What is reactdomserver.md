========== Question ==========  

### What is ReactDOMServer?  

========== Answer ==========  

The `ReactDOMServer` object enables you to render components to static markup (typically used on node server). This object is mainly used for _server-side rendering_ (SSR). The following methods can be used in both the server and browser environments:

1. `renderToString()`

2. `renderToStaticMarkup()`

For example, you generally run a Node-based web server like Express, Hapi, or Koa, and you call `renderToString` to render your root component to a string, which you then send as response.

```javascript
// using Express
import { renderToString } from 'react-dom/server';
import MyPage from './MyPage';

app.get('/', (req, res) => {
    res.write('<!DOCTYPE html><html><head><title>My Page</title></head><body>');
    res.write('<div id="content">');
    res.write(renderToString(<MyPage />));
    res.write('</div></body></html>');
    res.end();
});
```

========== Id ==========  
41

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#41-What-is-reactdomserver

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
