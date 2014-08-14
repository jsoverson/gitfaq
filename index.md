---
layout: page
title: GIT FAQ
tagline: Help without manpages.
---
{% include JB/setup %}

Want to answer or ask a question? Check out the [unanswered page](./unanswered.html).

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
git add file.js # stage the file
git commit      # commit the file
```

------------------------------------------------

## How do I push my changes up?

```
git push
git push origin branch-name
```

------------------------------------------------

## How do I get updates from the server?
 
```
git pull
```

------------------------------------------------

## How do I create a branch?

```
git branch <branch>   # just creates a branch off the current sha
git checkout <branch> # actually moves to branch

git checkout -b <branch>    # branches and moves to the branch in one command
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

{{ site.warning.history }}

------------------------------------------------

## What if I forgot a file in my last commit!

```
git commit       # the original commit
git add file.js  # the file that needed to be included
git commit --amend  # amend the commit in step 1 with the added file
```

This will add the file to the previous commit and replace it with a new commit.

{{ site.warning.history }}

------------------------------------------------

## How do I undo a commit?

Do you want to undo the commit and never see the changes ever again?

```
git reset --hard HEAD~1
```

Do you want to keep your changes and just undo the actual act of committing?

```
git reset HEAD~1
```

------------------------------------------------

## How do I revert all uncommitted changes?

```
git checkout .        # reset all tracked files
git checkout file.txt # reset file.txt
git checkout somedir/ # reset all files in somedir/
```

```
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
------------------------------------------------

## What is the difference between fetch and pull?

Pull = Fetch + Merge

------------------------------------------------

## How do I get a list of files that have changed since a commit?

After getting the appropriate hash from a command like `git log`

```
git diff --name-only cda409f...
```

------------------------------------------------
