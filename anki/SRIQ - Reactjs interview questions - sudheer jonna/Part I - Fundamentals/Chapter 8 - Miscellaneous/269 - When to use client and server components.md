========== Question ==========  

### When to use client and server components?  

========== Answer ==========  

You can efficiently build nextjs application if you are aware about which part
of the application needs to use client components and which other parts needs to
use server components. The common cases of both client and server components are
listed below:

**Client components:**

1. Whenever your need to add interactivity and event listeners such as
   onClick(), onChange(), etc to the pages

2. If you need to use State and Lifecycle Effects like useState(), useReducer(),
   useEffect() etc.

3. If there is a requirement to use browser-only APIs.

4. If you need to implement custom hooks that depend on state, effects, or
   browser-only APIs.

5. There are React Class components in the pages.

**Server components:**

1. If the component logic is about data fetching.

2. If you need to access backend resources directly.

3. When you need to keep sensitive information((access tokens, API keys, etc) )
   on the server.

4. If you want reduce client-side JavaScript and placing large dependencies on
   the server.

========== Id ==========  
269

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#269-When-to-use-client-and-server-components

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
