---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: How do I ignore a file pattern?
title: How do I ignore a file pattern?
---

```sh
git ignore '*.swp'
```

If you haven't ignored anything yet, this creates a `.gitignore` file which you probably want to add and track.

```sh
git add .gitignore
git commit -m 'added .gitignore'
```
