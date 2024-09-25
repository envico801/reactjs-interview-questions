========== Question ==========  

### What is diffing algorithm?  

========== Answer ==========  

React needs to use algorithms to find out how to efficiently update the UI to
match the most recent tree. The diffing algorithms is generating the minimum
number of operations to transform one tree into another. However, the algorithms
have a complexity in the order of O(n³) where n is the number of elements in the
tree.

In this case, displaying 1000 elements would require in the order of one billion
comparisons. This is far too expensive. Instead, React implements a heuristic
O(n) algorithm based on two assumptions:

1.  Two elements of different types will produce different trees.

2.  The developer can hint at which child elements may be stable across
    different renders with a key prop.

========== Id ==========  
202

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#202-What-is-diffing-algorithm

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
