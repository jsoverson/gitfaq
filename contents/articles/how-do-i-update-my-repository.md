---
title: How do I update my repository?
template: article.jade
---

```
git pull [remote] [branch]
```

This fetches the changes from the remote branch (ie `origin master`) and merges them into your current branch.

This is essentially doing:

```
git fetch [remote] [branch]
git merge FETCH_HEAD
```

`FETCH_HEAD` is a temporary reference pointing to the tip of what was just fetched, `[remote]/[branch]` could also be
used.

To update using rebase:

```
git pull --rebase [remote] [branch]
```

This performs the same as above, but using `rebase` instead of `merge`.
