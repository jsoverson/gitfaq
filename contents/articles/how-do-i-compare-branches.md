---
title: How do I compare branches?
template: article.jade
---

Find commits on remote `master` branch which are not on our local `master` branch:

    git cherry -v origin/master master

Find commits on local `master` branch which are not on our local `feature-1` branch:

    git cherry -v master feature-1

Find commits added since the `1.0.0` tag which:

    git cherry -v v1.0.0 master
