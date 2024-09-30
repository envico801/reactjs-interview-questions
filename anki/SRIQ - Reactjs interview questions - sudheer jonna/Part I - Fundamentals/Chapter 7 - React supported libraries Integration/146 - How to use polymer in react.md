========== Question ==========  

### How to use Polymer in React?  

========== Answer ==========  

You need to follow below steps to use Polymer in React,

1.  Create a Polymer element:

    ```jsx
    <link rel='import' href='../../bower_components/polymer/polymer.html' />;
    Polymer({
        is: 'calendar-element',
        ready: function () {
            this.textContent = 'I am a calendar';
        },
    });
    ```

2.  Create the Polymer component HTML tag by importing it in a HTML document, e.g. import it in the `index.html` of your React application:

    ```html
    <link rel="import" href="./src/polymer-components/calendar-element.html" />
    ```

3.  Use that element in the JSX file:

    ```javascript
    export default function MyComponent {
      return <calendar-element />;
    }
    ```

========== Id ==========  
146

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 7 - React supported libraries Integration

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-7-React-supported-libraries-Integration::#146-How-to-use-polymer-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
