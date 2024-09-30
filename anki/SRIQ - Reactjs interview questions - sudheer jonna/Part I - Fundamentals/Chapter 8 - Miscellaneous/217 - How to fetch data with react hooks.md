========== Question ==========  

### How to fetch data with React Hooks?  

========== Answer ==========  

The effect hook called `useEffect` can be used to fetch data from an API and to set the data in the local state of the component with the useState hook’s update function.

Here is an example of fetching a list of react articles from an API using fetch.

```javascript
import React from 'react';
function App() {
    const [data, setData] = React.useState({ hits: [] });
    React.useEffect(() => {
        fetch('http://hn.algolia.com/api/v1/search?query=react')
            .then((response) => response.json())
            .then((data) => setData(data));
    }, []);
    return (
        <ul>
            {data.hits.map((item) => (
                <li key={item.objectID}>
                    <a href={item.url}>{item.title}</a>
                </li>
            ))}
        </ul>
    );
}
export default App;
```

A popular way to simplify this is by using the library axios.

We provided an empty array as second argument to the useEffect hook to avoid activating it on component updates. This way, it only fetches on component mount.

========== Id ==========  
217

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#217-How-to-fetch-data-with-react-hooks

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
