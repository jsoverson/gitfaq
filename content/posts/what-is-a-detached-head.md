---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: What is a "detached head"?
title: What is a "detached head"?
---

```sh
You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.
```

This is not an error message and is nothing to be worried about. This is simply a notice
that you are not attached to an actual branch. For example, take the following commits on `master`:

```sh
master    A-B-C-D-E-F-G
```

Using the example above where the `master` branch has commits `A-G`, if you check out master you will be placed at the 'tip'
of master, commit `G`. If you remain at the tip of a branch, you are considered "attached."

If you check out an arbitrary commit, you are no longer necessarily associated with a branch and are considered "detached."

This is useful to explore the state of code at a commit, and you can also create and move to a branch from a "detached head" state.

If this state was unintentional, you can get back to where you likely want to be by checking out the branch you expected to be on, eg

```sh
$ git checkout master
Previous HEAD position was 183409d... added file.txt
Switched to branch 'master'
```

Try navigating through detached head by yourself. The following block sets up a fresh git repository with two commits.

```sh
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

```sh
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

```sh
$ git checkout master
Previous HEAD position was 183409d... added file.txt
Switched to branch 'master'
```

Notice, though, if you try to check out what commit the tip of master was initially pointing to you still will be
detached!

```sh
$ git co ec3...7da
Previous HEAD position was 183409d... added file.txt
HEAD is now at ec36c1b... added file2.txt
$ git status
HEAD detached at ec36c1b
nothing to commit, working directory clean
```
