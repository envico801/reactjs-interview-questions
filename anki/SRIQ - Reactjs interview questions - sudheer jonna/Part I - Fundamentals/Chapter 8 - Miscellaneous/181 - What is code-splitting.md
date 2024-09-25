========== Question ==========  

### What is code-splitting?  

========== Answer ==========  

Code-Splitting is a feature supported by bundlers like Webpack and Browserify
which can create multiple bundles that can be dynamically loaded at runtime. The
react project supports code splitting via dynamic import() feature.

For example, in the below code snippets, it will make moduleA.js and all its
unique dependencies as a separate chunk that only loads after the user clicks
the 'Load' button.

**moduleA.js**

```javascript
const moduleA = 'Hello';
export { moduleA };
```

**App.js**

```javascript
export default function App {
  function handleClick() {
    import("./moduleA")
      .then(({ moduleA }) => {
        // Use moduleA
      })
      .catch((err) => {
        // Handle failure
      });
  };
 return (
   <div>
     <button onClick={this.handleClick}>Load</button>
   </div>
 );
}
```

  <details><summary><b>See Class</b></summary>

<p>

```javascript
import React, { Component } from 'react';
class App extends Component {
    handleClick = () => {
        import('./moduleA')
            .then(({ moduleA }) => {
                // Use moduleA
            })
            .catch((err) => {
                // Handle failure
            });
    };
    render() {
        return (
            <div>
                <button onClick={this.handleClick}>Load</button>
            </div>
        );
    }
}
export default App;
```

  </p>

</details>

========== Id ==========  
181

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#181-What-is-code-splitting

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
