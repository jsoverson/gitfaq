---
layout: page
title: GIT FAQ
tagline: Help without manpages.
---
{% include JB/setup %}

Want to answer or ask a question? Fork the [repository](https://github.com/jsoverson/gitfaq) and check out the [unanswered page](./unanswered.html).

## How do I start a new git repository?

```
git init
git add .
git commit -m ‘initial commit’
git remote set-url origin <destination>
git push
```

------------------------------------------------

## How do I ignore a file pattern?

```
git ignore '*.swp'
```

If you haven't ignored anything yet, this creates a `.gitignore` file which you probably want to add and track.

```
git add .gitignore
git commit -m 'added .gitignore'
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

`HEAD` can be thought of as a variable pointing to a specific commit. It can change and isn't related to a branch.

Issuing new commits changes `HEAD`, checking anything out changes `HEAD`.

------------------------------------------------

## What is a "detached head"?

```
master    A-B-C-D-E-F-G
```

Using the example above where the `master` branch has commits `A-G`, if you check out master you will be placed at the 'tip'
of master, commit `G`. If you remain at the tip of a branch, you are considered "attached."

If you check out an arbitrary commit, you are no longer necessarily associated with a branch and are considered "detached."
 
This is useful to explore the state of code at a commit, and you can also create and move to a branch from a "detached head" state.

If this state was unintentional, you can get back to where you likely want to be by checking out the branch you expected to be on, eg

```
$ git checkout master
Previous HEAD position was 183409d... added file.txt
Switched to branch 'master'
```

Try navigating through detached head by yourself. The following block sets up a fresh git repository with two commits.

```
git init
touch file.txt
git add file.txt
git commit -m 'added file.txt'
touch file2.txt
git add file2.txt
git commit -m 'added file2.txt'
```

`HEAD` is now at the tip of master. Check out the previous commit by issuing the command `git checkout HEAD~1` which references
the commit 1 before `HEAD`.

```
$ git checkout HEAD~1
git co HEAD~1
Note: checking out 'HEAD~1'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b new_branch_name

HEAD is now at 183409d... added file.txt
```

To get back to the tip of master, `checkout master`.

```
$ git checkout master
Previous HEAD position was 183409d... added file.txt
Switched to branch 'master'
```

Notice, though, if you try to check out what commit the tip of master was initially pointing to you still will be
detached!

```
$ git co ec3...7da
Previous HEAD position was 183409d... added file.txt
HEAD is now at ec36c1b... added file2.txt
$ git status
HEAD detached at ec36c1b
nothing to commit, working directory clean
```
 
------------------------------------------------

## What is "origin"?

Origin is the default name for the remote server. "Remotes" can be named anything, you can see the names of all
 your remotes with the command `remote`
 
```
$ git remote -v
origin	git@github.com:jsoverson/gitfaq.git (fetch)
origin	git@github.com:jsoverson/gitfaq.git (push)
```

------------------------------------------------
