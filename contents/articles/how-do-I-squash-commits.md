---
title: How do I squash commits?
template: article.jade
---

There are multiple ways of squashing commits but the most recommended and straight forward is to use an interactive rebase, eg

```
git rebase -i HEAD~4 # interactively rebase from 3 commits ago
```

This command will bring up your editor with some helpful documentation and list of those commits and messages. The commits are listed in order with the oldest commit at the top and the latest commit at the bottom.

```
pick f53d15b fixed edge case with IE5
pick 930c0e5 added code coverage
pick fa7c471 fixed lint errors
pick fb57c85 added feature Foo

# Rebase 0a4b808..db5d725 onto 0a4b808
#
# Commands:
#  p, pick = use commit
#  r, reword = use commit, but edit the commit message
#  e, edit = use commit, but stop for amending
#  s, squash = use commit, but meld into previous commit
#  f, fixup = like "squash", but discard this commit's log message
#  x, exec = run command (the rest of the line) using shell
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.
#
# Note that empty commits are commented out
```

To squash the last 4 commits into the most recent, you would change `pick` to `squash` for commits 2, 3, and 4.

```
pick f53d15b fixed edge case with IE5
squash 930c0e5 added code coverage
squash fa7c471 fixed lint errors
squash fb57c85 added feature Foo
```

When the file is saved and the editor is quit, git will automatically squash those 4 commits into one. Your editor
will then pop up again allowing you to change the commit message for the resulting commit(s).
