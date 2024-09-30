========== Question ==========  

### What are fragments?  

========== Answer ==========  

It's a common pattern or practice in React for a component to return multiple elements. _Fragments_ let you group a list of children without adding extra nodes to the DOM.

You need to use either `<Fragment>` or a shorter syntax having empty tag (`<></>`).

Below is the example of how to use fragment inside _Story_ component.

```jsx
function Story({ title, description, date }) {
    return (
        <Fragment>
            <h2>{title}</h2>
            <p>{description}</p>
            <p>{date}</p>
        </Fragment>
    );
}
```

It is also possible to render list of fragments inside a loop with the mandatory **key** attribute supplied.

```jsx
function StoryBook() {
    return stories.map((story) => (
        <Fragment key={story.id}>
            <h2>{story.title}</h2>
            <p>{story.description}</p>
            <p>{story.date}</p>
        </Fragment>
    ));
}
```

Usually, you don't need to use `<Fragment>` until there is a need of _key_ attribute. The usage of shorter syntax looks like below.

```jsx
function Story({ title, description, date }) {
    return (
        <>
            <h2>{title}</h2>
            <p>{description}</p>
            <p>{date}</p>
        </>
    );
}
```

========== Id ==========  
31

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#31-What-are-fragments

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
