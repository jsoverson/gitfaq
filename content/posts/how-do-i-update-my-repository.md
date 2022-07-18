---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: How do I update my repository?
title: How do I update my repository?
---

```sh
git pull [remote] [branch]
```

To update using rebase :

```sh
git pull --rebase [remote] [branch]
```

This performs the same as above, but using `rebase` instead of `merge`.

(See also [What is the difference between fetch and pull](http://gitfaq.org/articles/what-is-the-difference-between-fetch-and-pull.html) for more details)
