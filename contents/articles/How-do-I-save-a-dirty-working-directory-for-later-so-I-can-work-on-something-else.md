---
title: How do I save a dirty working directory for later so I can work on something else?
template: article.jade
---

If you have to interrupt your current work for some more important, you can make a temporary branch or you can use `git stash`.


```
git stash
# edit your bugfix
git commit -m 'my bugfix ...'
git stash pop
# continue
```
