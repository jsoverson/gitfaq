---
title: What if I forgot to add a file in my last commit?
template: article.jade
---

```
git commit       # the original commit
git add file.js  # the file that needed to be included
git commit --amend  # amend the commit in step 1 with the added file
```

This will add the file to the previous commit and replace it with a new commit.

