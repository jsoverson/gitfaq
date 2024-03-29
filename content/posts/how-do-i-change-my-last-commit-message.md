---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: How do I change my last commit message?
title: How do I change my last commit message?
---

```sh
$ git commit --amend --only
```

Or, without staged changes:

```sh
$ git commit --amend
```

`--amend` without other options combines the currently staged changes with the last commit and then opens an editor to
update the commit message. If you have staged changes, they will be added.

To update the last message even if there are staged changes (`git status` reports files under `Changes to be committed`)
then you can use the `-o` (or `--only`) option to indicate you want to amend the last commit but only use the files
that were previously committed.
