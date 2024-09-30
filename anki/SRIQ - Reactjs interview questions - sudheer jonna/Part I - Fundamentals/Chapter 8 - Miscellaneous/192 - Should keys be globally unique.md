========== Question ==========  

### Should keys be globally unique?  

========== Answer ==========  

The keys used within arrays should be unique among their siblings but they don’t need to be globally unique. i.e, You can use the same keys with two different arrays.

For example, the below `Book` component uses two arrays with different arrays,

```javascript
function Book(props) {
    const index = (
        <ul>
            {props.pages.map((page) => (
                <li key={page.id}>{page.title}</li>
            ))}
        </ul>
    );
    const content = props.pages.map((page) => (
        <div key={page.id}>
            <h3>{page.title}</h3>
            <p>{page.content}</p>
            <p>{page.pageNumber}</p>
        </div>
    ));
    return (
        <div>
            {index}
            <hr />
            {content}
        </div>
    );
}
```

========== Id ==========  
192

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#192-Should-keys-be-globally-unique

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
