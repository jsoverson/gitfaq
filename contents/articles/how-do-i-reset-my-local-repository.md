---
title: How do I completely reset my local repository?
template: article.jade
---

```
git reset
git checkout .
git clean -fdx
```

git clean options:
-f      force
-d      delete directories
-x      ignore .gitignore