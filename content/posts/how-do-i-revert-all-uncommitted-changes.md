---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: How do I revert all uncommitted changes?
title: How do I revert all uncommitted changes?
---

```sh
git checkout .        # reset all tracked files
git checkout file.txt # reset file.txt
git checkout somedir/ # reset all files in somedir/
```

```sh
git reset --hard HEAD
```
