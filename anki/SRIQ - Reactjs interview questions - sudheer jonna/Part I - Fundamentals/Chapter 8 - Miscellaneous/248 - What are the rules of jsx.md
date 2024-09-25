========== Question ==========  

### What are the rules of JSX?  

========== Answer ==========  

The below 3 rules needs to be followed while using JSX in a react application.

1.  **Return a single root element**:

    If you are returning multiple elements from a component, wrap them in a
    single parent element. Otherwise you will receive the below error in your
    browser console.

    `html Adjacent JSX elements must be wrapped in an enclosing tag.`

2.  **All the tags needs to be closed:**

    Unlike HTML, all tags needs to closed explicitly with in JSX. This rule
    applies for self-closing tags(like hr, br and img tags) as well.

3.  **Use camelCase naming:**

    It is suggested to use camelCase naming for attributes in JSX. For example,
    the common attributes of HTML elements such as `class`, `tabindex` will be
    used as `className` and `tabIndex`.

    **Note:** There is an exception for `aria-*` and `data-*` attributes which
    should be lower cased all the time.

========== Id ==========  
248

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#248-What-are-the-rules-of-jsx

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
