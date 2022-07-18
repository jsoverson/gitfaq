---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: How do I undo a commit?
title: How do I undo a commit?
---

Do you want to undo the commit and never see the changes ever again?

```
git reset --hard HEAD~1
```

Do you want to keep your changes and just undo the actual act of committing?

```
git reset HEAD~1
```
