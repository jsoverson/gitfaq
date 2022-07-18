---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: What is local history/shared history?
title: What is local history/shared history?
---

"Remote history" or "Shared History" is used to refer to history that is shared with others. "Local history" is used to
refer to changes that have never been shared.

For the following commit history, "Shared History"and "Local History" boundaries are shown,

```sh
A-B-C-D-E                origin/master

A-B-C-D-E-F-G-H-I        origin/feature1

A-B-C-D-E-F-G-H-I-J-K-J  feature1 (local)
|       | |     | |   |
|       | |     | +-+-+
|       | |     |   |
|       | +--+--+   Local History
|       |    |
+---+---+  Shared History (branch)
    |
Shared History (master)
```
