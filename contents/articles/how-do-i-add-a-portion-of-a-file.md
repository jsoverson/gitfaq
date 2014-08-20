---
title: How do I add only a portion of a file?
template: article.jade
---

```
git add --patch <file>
```

This brings up an interactive interface that moves through each individual change to a file, allowing you to
only stage the changes that you want.

```
$ git add --patch package.json
diff --git a/package.json b/package.json
index 7a558a3..e03ce3f 100644
--- a/package.json
+++ b/package.json
@@ -2,7 +2,6 @@
   "name": "package",
   "version": "0.4.3",
   "description": "this is an example package",
-  "keywords": ["key", "middleware", "connect"],
   "repository": "git://github.com/foo/bar.git",
   "author": "Joe Smith <jsmith@google.com> (http://google.com)",
   "repository": "git://github.com/foo/bar",
Stage this hunk [y,n,q,a,d,/,j,J,g,e,?]? y
```
