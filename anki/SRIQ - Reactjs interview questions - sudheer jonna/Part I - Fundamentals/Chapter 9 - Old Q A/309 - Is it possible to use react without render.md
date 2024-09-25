========== Question ==========  

### Is it possible to use React without rendering HTML?  

========== Answer ==========  

It is possible. Below are the possible options:

```jsx
render() {
  return false
}
```

```jsx
render() {
  return true
}
```

```jsx
render() {
  return null
}
```

React version >=16.0.0:

```jsx
render() {
  return []
}
```

```jsx
render() {
  return ""
}
```

React version >=16.2.0:

```jsx
render() {
  return <React.Fragment></React.Fragment>
}
```

```jsx
render() {
  return <></>
}
```

React version >=18.0.0:

```jsx
render() {
  return undefined
}
```

========== Id ==========  
309

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#309-Is-it-possible-to-use-react-without-render

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
