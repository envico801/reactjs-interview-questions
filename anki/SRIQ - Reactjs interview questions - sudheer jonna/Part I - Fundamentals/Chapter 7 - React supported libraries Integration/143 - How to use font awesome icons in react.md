========== Question ==========  

### How to use Font Awesome icons in React?  

========== Answer ==========  

The below steps followed to include Font Awesome in React:

1.  Install `font-awesome`:

    ```console
    $ npm install --save font-awesome
    ```

2.  Import `font-awesome` in your `index.js` file:

    ```javascript
    import 'font-awesome/css/font-awesome.min.css';
    ```

3.  Add Font Awesome classes in `className`:

    ```javascript
    function MyComponent {
      return <div><i className={'fa fa-spinner'} /></div>
    }
    ```

========== Id ==========  
143

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 7 - React supported libraries Integration

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-7-React-supported-libraries-Integration::#143-How-to-use-font-awesome-icons-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
