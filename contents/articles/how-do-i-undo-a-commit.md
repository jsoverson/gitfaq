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

Either way, if you already pushed the commit you'll need to force push:

```
git push -f
```

**WARNING**: Do not force push if you are not the only person working on that repository! It will mess up other peoples' local repositories.

