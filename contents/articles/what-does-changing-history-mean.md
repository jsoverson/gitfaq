---
title: What does "Changing History" mean?
template: article.jade
---

In git, each commit is tagged with a unique SHA-1 hash. These are critical when resolving differences between sources that
have diverged. This sequence of SHAs is referred to as the "history" and "changing history" is regenerating
those hashes via any number of legitimate means.

A modified history makes it very difficult to resolve differences between two repositories because, from git's perspective,
the SHAs have changed and commits that *should* refer to the same changes now look to be two different changes at different times.

Rewriting history has a number of legitimate uses but requires communication proportional to the number of people who
have already based development off the history that is to be changed. It is important that changes are resolved before
history is rewritten and that usually means waiting for all important work to be pushed.

Rewriting *local history* up to the point of shared changes is rarely a problem. The number of people you need to communicate with
 is usually limited to just you.

On shared feature branches, the burden of communication increases to the people who are developing with you on that branch. This
 is also usually not a problem if you expect branches to be short lived and highly collaborative (assuming high communication).

On mainline branches that anyone could base off of for any arbitrary work (eg "master" or "develop"),
changing history is very problematic and should only be done in extreme cases where the cost is understood.
Problems occur because you can rarely be sure you've communicated with *everybody* you need to in order to
make sure important changes are pushed before a history modification.

See also [What is local history/shared history?](/articles/what-is-local-shared-history.html)