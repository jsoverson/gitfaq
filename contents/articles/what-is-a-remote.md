---
title: What is a "remote"?
template: article.jade
---

The term "remote" is any remote destination that you may want to push or pull from. This is often a git
repository hosted on a git server, ie github.com

You can have multiple remotes that you push and pull from.

You can view the remotes you have set with `git remote` and `git remote -v` gives you more important information.

```
$ git remote -v
origin	git@github.com:jsoverson/gitfaq.git (fetch)
origin	git@github.com:jsoverson/gitfaq.git (push)
```

You can add new remotes via `git remote add <destination>` eg

```
$ git remote add mficarra git@github.com:mficarra/gitfaq.git
```

You can change the destination via `git remote set-url <remote> <destination>`

```
$ git remote set-url origin git@github.com:mficarra/gitfaq.git
```
