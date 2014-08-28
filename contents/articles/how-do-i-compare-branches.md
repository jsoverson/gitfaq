---
title: How do I compare branches?
template: article.jade
---

Find commits on remote `master` branch which are not on our local `master` branch:

    git cherry -v origin/master master

Find commits on local `master` branch which are not on our local `feature` branch:

    git cherry -v master feature

Find commits added since the `1.0.0` tag:

    git cherry -v v1.0.0 master
