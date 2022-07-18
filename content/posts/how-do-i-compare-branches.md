---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: How do I compare branches?
title: How do I compare branches?
---

Find commits on remote `master` branch which are not on our local `master` branch:

```sh
git cherry -v origin/master master
```

Find commits on local `master` branch which are not on our local `feature` branch:

```sh
git cherry -v master feature
```

Find commits added since the `1.0.0` tag:

```sh
git cherry -v v1.0.0 master
```
