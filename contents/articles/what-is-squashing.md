---
title: What is squashing?
template: article.jade
---

Squashing is the act of turning multiple git commits into fewer. There are many reasons you might want to do this but the most straightforward is to simply keep the commit history cleaner and filled with high value changes.

Consider the following set of commits

```
f53d15b fixed edge case with IE5
930c0e5 increased code coverage
fa7c471 fixed lint errors
fb57c85 added feature Foo
```

In a local repository that level of detail may be useful; at some point a regression may have been introduced
 while fixing lint errors and you would be able to revert to a previous commit to do some testing.

In the grand scheme of living software, this level of granularity becomes noisier than it is worth. When preparing code
to enter a main line branch it can become more valuable to squash commits into logical chunks so that the history becomes
more valuable as a record of important changes. The following commits could then be squashed into a single commit, eg

```
a3545a5 added feature Foo
```

See also [how do I squash commits?](/articles/how-do-I-squash-commits.html)
