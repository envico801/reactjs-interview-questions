========== Question ==========  

### How to make AJAX call and in which component lifecycle methods should I make an AJAX call?  

========== Answer ==========  

You can use AJAX libraries such as Axios, jQuery AJAX, and the browser built-in `fetch`. You should fetch data in the `componentDidMount()` lifecycle method. This is so you can use `setState()` to update your component when the data is retrieved.

For example, the employees list fetched from API and set local state:

```jsx
class MyComponent extends React.Component {
    constructor(props) {
        super(props);
        this.state = {
            employees: [],
            error: null,
        };
    }

    componentDidMount() {
        fetch('https://api.example.com/items')
            .then((res) => res.json())
            .then(
                (result) => {
                    this.setState({
                        employees: result.employees,
                    });
                },
                (error) => {
                    this.setState({ error });
                },
            );
    }

    render() {
        const { error, employees } = this.state;
        if (error) {
            return <div>Error: {error.message}</div>;
        } else {
            return (
                <ul>
                    {employees.map((employee) => (
                        <li key={employee.name}>
                            {employee.name}-{employee.experience}
                        </li>
                    ))}
                </ul>
            );
        }
    }
}
```

========== Id ==========  
318

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#318-How-to-make-ajax-call-and-in-which-compone

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
