---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: How do I delete a branch?
title: How do I delete a branch?
---

Delete a local branch `feature`:

```sh
git branch -d feature
```

This will fail if the branch is not merged. To delete the branch regardless:

```sh
git branch -D feature
```

To delete a remote branch `feature` on remote `origin` (warning: There is no confirmation!):

```sh
git push origin :feature
```

Note: `git-branch` documentation lists documentation for the option `-r` which works on remote _tracking_ branches, not
branches on the remote; `git branch -D -r origin/feature` will delete the remote tracking branch `origin/feature`,
not the branch `feature` on remote `origin`. Pulling/fetching from the remote again will recreate that tracking branch.

To delete remote tracking branches that no longer exist on the remote:

```sh
git fetch --prune
```
