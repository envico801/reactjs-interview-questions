========== Question ==========  

### Can I use web components in react application?  

========== Answer ==========  

Yes, you can use web components in a react application. Even though many
developers won't use this combination, it may require especially if you are
using third-party UI components that are written using Web Components.

For example, let us use `Vaadin` date picker web component as below,

```javascript
import './App.css';
import '@vaadin/vaadin-date-picker';
export default function App() {
    return (
        <div className='App'>
            <vaadin-date-picker label='When were you born?'></vaadin-date-picker>
        </div>
    );
}
```

========== Id ==========  
196

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#196-Can-i-use-web-components-in-react-applicat

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
