========== Question ==========  

### Give an example of Styled Components?  

========== Answer ==========  

Lets create `<Title>` and `<Wrapper>` components with specific styles for each.

```javascript
import React from 'react';
import styled from 'styled-components';
// Create a <Title> component that renders an <h1> which is centered, red and sized at 1.5em
const Title = styled.h1`
    font-size: 1.5em;
    text-align: center;
    color: palevioletred;
`;
// Create a <Wrapper> component that renders a <section> with some padding and a papayawhip background
const Wrapper = styled.section`
    padding: 4em;
    background: papayawhip;
`;
```

These two variables, `Title` and `Wrapper`, are now components that you can
render just like any other react component.

```jsx
<Wrapper>
    <Title>{'Lets start first styled component!'}</Title>
</Wrapper>
```

========== Id ==========  
151

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 7 - React supported libraries Integration

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-7-React-supported-libraries-Integration::#151-Give-an-example-of-styled-components

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
