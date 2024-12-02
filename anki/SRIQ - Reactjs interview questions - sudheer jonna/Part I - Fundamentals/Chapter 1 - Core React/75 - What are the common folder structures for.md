========== Question ==========  

### What are the common folder structures for React?  

========== Answer ==========  

There are two common practices for React project file structure.

1.  **Grouping by features or routes:**

    One common way to structure projects is locate CSS, JS, and tests together, grouped by feature or route.

    ```
    common/
    ├─ Avatar.js
    ├─ Avatar.css
    ├─ APIUtils.js
    └─ APIUtils.test.js
    feed/
    ├─ index.js
    ├─ Feed.js
    ├─ Feed.css
    ├─ FeedStory.js
    ├─ FeedStory.test.js
    └─ FeedAPI.js
    profile/
    ├─ index.js
    ├─ Profile.js
    ├─ ProfileHeader.js
    ├─ ProfileHeader.css
    └─ ProfileAPI.js
    ```

2.  **Grouping by file type:**

    Another popular way to structure projects is to group similar files together.

    ```
    api/
    ├─ APIUtils.js
    ├─ APIUtils.test.js
    ├─ ProfileAPI.js
    └─ UserAPI.js
    components/
    ├─ Avatar.js
    ├─ Avatar.css
    ├─ Feed.js
    ├─ Feed.css
    ├─ FeedStory.js
    ├─ FeedStory.test.js
    ├─ Profile.js
    ├─ ProfileHeader.js
    └─ ProfileHeader.css
    ```

========== Id ==========  
75

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#75-What-are-the-common-folder-structures-for

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
