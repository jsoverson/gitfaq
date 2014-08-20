---
title: What if I forgot to add a file in my last commit?
template: article.jade
---

```
git add file.js     # the file that needed to be included
git commit --amend  # amend the commit done before step 1 with the added file
```
This will add the file to the previous commit and replace it with a new commit.

This can be simplified into one command:

```
git commit --amend file.js
```

If the commit message doesn't need to be updated:

```
git commit --amend --no-edit file.js
```

If all the edited files need to be added to the last commit:

```
git commit --amend --no-edit --all
```
