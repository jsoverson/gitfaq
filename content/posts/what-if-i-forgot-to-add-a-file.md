---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: What if I forgot to add a file in my last commit?
title: What if I forgot to add a file in my last commit?
---

```sh
git add file.js     # the file that needed to be included
git commit --amend  # amend the commit done before step 1 with the added file
```

This will add the file to the previous commit and replace it with a new commit.

This can be simplified into one command:

```sh
git commit --amend file.js
```

If the commit message doesn't need to be updated:

```sh
git commit --amend --no-edit file.js
```

If all the edited files need to be added to the last commit:

```sh
git commit --amend --no-edit --all
```
