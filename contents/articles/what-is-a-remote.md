---
title: What is a "remote"?
template: article.jade
---

The term "remote" is any remote destination that you may want to push or pull from. This is often a git
repository hosted on a git server like those run by Github.

You can have multiple remotes.

You can view the remotes you have set with `git remote` and `git remote -v` gives you more important information.

```
$ git remote -v
origin	git@github.com:jsoverson/gitfaq.git (fetch)
origin	git@github.com:jsoverson/gitfaq.git (push)
```

You can add new remotes via `git remote add <destination>` eg

```
$ git remote add michaelficarra git@github.com:michaelficarra/gitfaq.git
```

You can change the destination via `git remote set-url <remote> <destination>`

```
$ git remote set-url origin git@github.com:michaelficarra/gitfaq.git
```
