========== Question ==========  

### Can I use javascript urls in react16.9?  

========== Answer ==========  

Yes, you can use javascript: URLs but it will log a warning in the console.
Because URLs starting with javascript: are dangerous by including unsanitized
output in a tag like `<a href>` and create a security hole.

```javascript
const companyProfile = {
    website: "javascript: alert('Your website is hacked')",
};
// It will log a warning
<a href={companyProfile.website}>More details</a>;
```

Remember that the future versions will throw an error for javascript URLs.

========== Id ==========  
232

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#232-Can-i-use-javascript-urls-in-react16-9

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
