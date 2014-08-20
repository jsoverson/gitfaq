---
title: How do I update my repository?
template: article.jade
---

```
git pull [remote] [branch]
```

To update using rebase : 

```
git pull --rebase [remote] [branch]
```

This performs the same as above, but using `rebase` instead of `merge`.

(See also "What is the difference between fetch and pull" for more details)

