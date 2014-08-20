---
title: How do I change the contents of a commit I have not pushed?
template: article.jade
---

```
git commit --amend <files>
```

or

```
git commit --amend --all
```

If the commit message does not need to be changed, add `--no-edit` eg

```
git commit --amend --all --no-edit
```
