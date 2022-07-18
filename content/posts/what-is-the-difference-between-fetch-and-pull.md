---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: What is the difference between fetch and pull?
title: What is the difference between fetch and pull?
---

`git pull [remote] [branch]` is the same as

```sh
git fetch [remote] [branch]
git merge [remote][/branch]
```

`git pull --rebase [remote] [branch]` is the same as

```sh
git fetch [remote] [branch]
git rebase [remote][/branch]
```
