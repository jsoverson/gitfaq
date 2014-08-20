---
title: What is the difference between fetch and pull?
template: article.jade
---

`git pull [remote] [branch]` is the same as

```
git fetch [remote] [branch]
git merge [remote][/branch]
```

`git pull --rebase [remote] [branch]` is the same as 

```
git fetch [remote] [branch]
git rebase [remote][/branch]
```