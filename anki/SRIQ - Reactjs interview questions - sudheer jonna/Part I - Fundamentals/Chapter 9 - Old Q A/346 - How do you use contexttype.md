========== Question ==========  

### How do you use contextType?  

========== Answer ==========  

ContextType is used to consume the context object. The contextType property can be used in two ways,

1.  **contextType as property of class:**

    The contextType property on a class can be assigned a Context object created by React.createContext(). After that, you can consume the nearest current value of that Context type using this.context in any of the lifecycle methods and render function.

    Lets assign contextType property on MyClass as below,

    ```javascript
    class MyClass extends React.Component {
        componentDidMount() {
            let value = this.context;
            /* perform a side-effect at mount using the value of MyContext */
        }
        componentDidUpdate() {
            let value = this.context;
            /* ... */
        }
        componentWillUnmount() {
            let value = this.context;
            /* ... */
        }
        render() {
            let value = this.context;
            /* render something based on the value of MyContext */
        }
    }
    MyClass.contextType = MyContext;
    ```

2.  **Static field**

    You can use a static class field to initialize your contextType using public class field syntax.

    ```javascript
    class MyClass extends React.Component {
        static contextType = MyContext;
        render() {
            let value = this.context;
            /* render something based on the value */
        }
    }
    ```

========== Id ==========  
346

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#346-How-do-you-use-contexttype

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
