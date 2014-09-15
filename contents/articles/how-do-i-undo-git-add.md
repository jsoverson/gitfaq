---
title: How do I undo git add?
template: article.jade
---

```
git reset
```

*or* 

```
git reset file.txt
```

`git add` simply stages changes to be committed. To undo that action, 
all that's needed is to `git reset` the file or list of files.

To undo a commit, see [How do I undo a commit?](http://gitfaq.org/#How do I undo a commit?)

