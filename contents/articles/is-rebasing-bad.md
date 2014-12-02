---
title: Is rebasing bad?
template: article.jade
---

Rebasing isn't good or bad, it's just different. It's common to hear people advise against rebasing because it's easier
to assume people don't know what they are doing than it is to teach people to do something correctly.

Problems can arise because rebasing rewrites the history. In the example given for ["what is rebasing"](/articles/what-is-rebasing.html), the history of the `feature` branch is
changed after the rebase and, if this was a shared branch, other developers wouldn't be able to cleanly get up to date.

Rebasing is valuable because it leaves the history cleaner with fewer merge commits and more accurately describes
common development intentions.

Think about the flow behind keeping a `feature` branch like below up to date with `master`.

```
A-B-C-D-E    master
   \
    X-Y-Z    feature
```

The goal isn't, necessarily, to regularly "merge" `master` into `feature` en masse, the goal is to ensure that the work
done in `feature` simply stays up to date with the latest code in `master`. This is a great reason to use rebase; `X-Y-Z` get
rewound, `feature` is then pulled up to date with `master`, and the commits are replayed essentially making it feel
like your work has always been done on top of the latest code in `master`.

