---
layout: page
title: GIT FAQ
tagline: 
---
{% include JB/setup %}

## How do I start a new git repository?

```
git init
git add .
git commit -m ‘initial commit’
git remote set-url origin <destination>
git push
```

------------------------------------------------


## How do I commit a file?

```
git add file.js   # stage the file
git commit    # commit the file
```

------------------------------------------------

## How do I push my changes up?

```
git push
git push origin branch-name
```

------------------------------------------------

## How do I get updates from the origin?
 
```
git pull --rebase
what about git pull?
```

------------------------------------------------

## How do I create a branch?

```
git branch just creates a branch off the current sha
git checkout <branch> moves to branch
```

------------------------------------------------

## How do I check out a branch from the server?

```
git checkout -b <branch>
```

------------------------------------------------

## How do I undo git add?

```
$ git reset
```

*or* 

```
$ git reset file.txt
```

------------------------------------------------

## How do I change my last commit message?

```
git commit --amend
```

------------------------------------------------

## Oops I forgot a file in my last commit!

```
# after a commit
git add file.js
git commit --amend
```

This will add the file to the previous commit and replace it with a new commit.

------------------------------------------------

## How do I undo a commit?

### &bull; Do you want to undo the commit and never see the changes ever again?

```
git reset --hard HEAD~1
```

### &bull; Do you want to keep your changes and just undo the actual commit?

```
git reset HEAD~1
```

------------------------------------------------

## How do I revert all uncommitted changes?

```
git checkout .
git checkout file.txt
git checkout somedir/
git reset --hard HEAD
```

------------------------------------------------

## How do I remove all untracked files?

```
git clean -fd
```

------------------------------------------------

## How do I completely reset my local repository?

```
git reset
git checkout .
git clean -fdx
```

