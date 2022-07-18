---
author: "Jarrod Overson"
date: 2022-7-14
linktitle: What is difference between master & HEAD?
title: What is difference between master & HEAD?
---

`master` is the common name for the default branch. It doesn't need to exist, but it often does.

`HEAD` can be thought of as a variable pointing to a specific commit. It can change and isn't related to a branch.

Issuing new commits changes `HEAD`, checking anything out changes `HEAD`.
