---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: How do I undo git add?
title: How do I undo git add?
---

```sh
git reset
```

_or_

```sh
git reset file.txt
```

`git add` simply stages changes to be committed. To undo that action,
all that's needed is to `git reset` the file or list of files.

To undo a commit, see [How do I undo a commit?](http://gitfaq.org/#How do I undo a commit?)
