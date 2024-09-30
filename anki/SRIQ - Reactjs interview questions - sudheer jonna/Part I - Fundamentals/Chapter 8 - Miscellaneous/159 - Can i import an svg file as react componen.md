========== Question ==========  

### Can I import an SVG file as react component?  

========== Answer ==========  

You can import SVG directly as component instead of loading it as a file. This feature is available with `react-scripts@2.0.0` and higher.

```jsx
import { ReactComponent as Logo } from './logo.svg';
const App = () => (
    <div>
        {/* Logo is an actual react component */}
        <Logo />
    </div>
);
```

**Note**: Don't forget about the curly braces in the import.

========== Id ==========  
159

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#159-Can-i-import-an-svg-file-as-react-componen

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
