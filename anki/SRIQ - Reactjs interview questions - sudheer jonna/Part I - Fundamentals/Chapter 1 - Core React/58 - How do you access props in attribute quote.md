========== Question ==========  

### How do you access props in attribute quotes?  

========== Answer ==========  

React (or JSX) doesn't support variable interpolation inside an attribute value. The below representation won't work:

```jsx
<img className='image' src='images/{this.props.image}' />
```

But you can put any JS expression inside curly braces as the entire attribute value. So the below expression works:

```jsx
<img className='image' src={'images/' + this.props.image} />
```

Using _template strings_ will also work:

```jsx
<img className='image' src={`images/${this.props.image}`} />
```

========== Id ==========  
58

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#58-How-do-you-access-props-in-attribute-quote

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
