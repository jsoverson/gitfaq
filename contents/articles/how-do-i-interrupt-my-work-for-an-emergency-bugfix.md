---
title: How do I interrupt my work for an emergency bugfix?
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