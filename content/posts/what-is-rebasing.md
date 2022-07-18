---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: What is rebasing?
title: What is rebasing?
---

Rebasing is establishing a new base for a series of commits.

In the example below, the branch `feature` deviated at commit `B`, while the `master` branch moved along in parallel.

```sh
A-B-C-D-E    master
   \
    X-Y-Z    feature
```

You can rebase with the `rebase` command. For example, to rebase the `feature` branch on `master`:

```sh
$ git checkout feature
$ git rebase master
```

Rebasing essentially rewinds the commits on a branch, brings the branch up to date with the rebase target, and then
replays the rewound commits over it, leaving the timeline looking like this.

```sh
A-B-C-D-E        master
         \
          X'-Y'-Z'  feature
```

Warning this changes history, see also [What does changing history mean?](/articles/what-does-changing-history-mean.html)
