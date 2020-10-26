---
title: "Fix Branch Rename"
date: 2020-10-24
categories:
  - git
tags:
  - errors
  - terminal
---

## Branch rename failed on Git [Fixed]
* Create a repo on Github
* Create a local repo for the remote repo in step 1.
* Initialize .git remote repo on local repo in step 2 with `git init`. Default branch will be `master`
* Rename default branch `master` in step 3 into `main`

  ```
  git branch -M main
  ```
### Error occurs:
```
error: refname refs/heads/master not found
fatal: Branch rename failed
```
### Cause: currently in "detached head state"
### Fix: checkout on the <new_branch> which commit will be pushed on
```
git checkout -b main
```
