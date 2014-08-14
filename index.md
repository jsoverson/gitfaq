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
git reset
```

*or* 

```
git reset file.txt
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

## What is difference between master & HEAD?
 
`master` is the common name for the default branch. It doesn't need to exist, but it often does.

`HEAD` is the leading commit of a branch. For example, if the following represents a `master` branch with commit hashes 
`A-G` in sequential order, the commit `G` represents the `HEAD` of `master`. 

```
master    A-B-C-D-E-F-G
```

 There is a `HEAD` for every branch.

------------------------------------------------

## What is 'detached head'?

```
master    A-B-C-D-E-F-G
```

Using the example above, if you check out anything but `G` your current "HEAD" is detached from a branch.
 
You can create and move to a branch from the commit and you will be at the `HEAD` of the new branch.

To get back to where you likely want to be, you want to check out a relevant branch, eg

```
git checkout master
```

 
------------------------------------------------

## What is origin?

Origin is the default name for the remote server. "Remotes" can be named anything, you can see the names of all
 your remotes with the command `remote`
 
```
$ git remote -v
origin	git@github.com:jsoverson/gitfaq.git (fetch)
origin	git@github.com:jsoverson/gitfaq.git (push)
```

------------------------------------------------
