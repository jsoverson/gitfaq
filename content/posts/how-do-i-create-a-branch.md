---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: How do I create a branch?
title: How do I create a branch?
---

```sh
git branch <branch>      # just creates a branch off the current sha
git checkout <branch>    # actually moves to the branch
```

This can be simplified to:

```sh
git checkout -b <branch> # branches and moves to the branch in one command
```
