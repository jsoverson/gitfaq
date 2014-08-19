---
title: How do I ignore a file pattern?
template: article.jade
---

```
git ignore '*.swp'
```
If you haven't ignored anything yet, this creates a `.gitignore` file which you probably want to add and track.
```
git add .gitignore
git commit -m 'added .gitignore'
```
