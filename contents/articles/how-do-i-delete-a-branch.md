---
title: How do I delete a branch?
template: article.jade
---

Delete a local branch `feature`:

    git branch -d feature
    
This will fail if the branch is not merged. To delete the branch regardless:

    git branch -D feature
    
To delete a remote branch `feature` on remote `origin` (warning: There is no confirmation!):
 
    git push origin :feature

Note: `git-branch` documentation lists documentation for the option `-r` which works on remote *tracking* branches, not
branches on the remote; `git branch -D -r origin/feature` will delete the remote tracking branch `origin/feature`, 
not the branch `feature` on remote `origin`. Pulling/fetching from the remote again will recreate that tracking branch.

To delete remote tracking branches that no longer exist on the remote:

    git fetch --prune
