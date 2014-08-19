---
title: How do I revert all uncommitted changes?
template: article.jade
---

```
git checkout .        # reset all tracked files
git checkout file.txt # reset file.txt
git checkout somedir/ # reset all files in somedir/
```

```
git reset --hard HEAD
```
