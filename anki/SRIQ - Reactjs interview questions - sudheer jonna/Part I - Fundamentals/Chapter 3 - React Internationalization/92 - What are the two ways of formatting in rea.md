========== Question ==========  

### What are the two ways of formatting in React Intl?  

========== Answer ==========  

The library provides two ways to format strings, numbers, and dates:

1.  **Using react components:**

    ```jsx
    <FormattedMessage
        id={'account'}
        defaultMessage={'The amount is less than minimum balance.'}
    />
    ```

2.  **Using an API:**

    ```javascript
    const messages = defineMessages({
        accountMessage: {
            id: 'account',
            defaultMessage: 'The amount is less than minimum balance.',
        },
    });
    formatMessage(messages.accountMessage);
    ```

========== Id ==========  
92

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 3 - React Internationalization

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-3-React-Internationalization::#92-What-are-the-two-ways-of-formatting-in-rea

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
