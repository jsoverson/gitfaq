---
title: How do I undo a commit?
template: article.jade
---

Do you want to undo the commit and never see the changes ever again?

```
git reset --hard HEAD~1
```

Do you want to keep your changes and just undo the actual act of committing?

```
git reset HEAD~1
```

**WARNING**: By undoing a commit this way, you are rewriting history. If you would like to *revert* the last commit, which does not rewrite history (it preserves the original commit, and just adds a commit that undoes that commit), use this:

```
git revert HEAD
```

