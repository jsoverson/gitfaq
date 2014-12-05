---
title: What is rebasing?
template: article.jade
---

Rebasing is establishing a new base for a series of commits.

In the example below, the branch `feature` deviated at commit `B`, while the `master` branch moved along in parallel.

```
A-B-C-D-E    master
   \
    X-Y-Z    feature
```

Rebasing essentially rewinds the commits on a branch, brings the branch up to date with the rebase target, and then
replays the rewound commits over it, leaving the timeline looking like this.

```
A-B-C-D-E        master
         \
          X-Y-Z  feature
```

Warning this changes history, see also []

See also [is rebasing bad?](/articles/is-rebasing-bad.html)
