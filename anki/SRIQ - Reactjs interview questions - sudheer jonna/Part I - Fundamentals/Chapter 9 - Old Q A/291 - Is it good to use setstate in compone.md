========== Question ==========  

### Is it good to use `setState()` in `componentWillMount()` method?  

========== Answer ==========  

Yes, it is safe to use `setState()` inside `componentWillMount()` method. But at
the same it is recommended to avoid async initialization in
`componentWillMount()` lifecycle method. `componentWillMount()` is invoked
immediately before mounting occurs. It is called before `render()`, therefore
setting state in this method will not trigger a re-render. Avoid introducing any
side-effects or subscriptions in this method. We need to make sure async calls
for component initialization happened in `componentDidMount()` instead of
`componentWillMount()`.

```jsx
componentDidMount() {
  axios.get(`api/todos`)
    .then((result) => {
      this.setState({
        messages: [...result.data]
      })
    })
}
```

========== Id ==========  
291

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#291-Is-it-good-to-use-setstate-in-compone

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
