---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: How do I change the contents of a commit I have not pushed?
title: How do I change the contents of a commit I have not pushed?
---

```sh
git commit --amend <files>
```

or

```sh
git commit --amend --all
```

If the commit message does not need to be changed, add `--no-edit` eg

```sh
git commit --amend --all --no-edit
```
