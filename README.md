# **devops**

## **Class 1 - 23-10-2024 - GIT**

- Version Control System
- Open source
- Important to know GIT to contribute in a open source project
- Must follow the best practices even if they are complex
- HEAD - current state
- Commit message always in present indefinite tense
- Commit hash - Unique identifier
- Always compares to the previous commit to track changes
- While deploying use the commit hash for versioning (build number)
- Can add empty commit without staging any change

## **Class 2 - 30-10-2024 - GIT**

- add git commit description  
```sh 
  git commit -m "commit message" -m "description"
```
- update last commit
```sh
  git commit --amend
```
- delete last commit but keep as unstaged
```sh 
  git reset HEAD~1
```
- delete upto N commits and keep changes unstaged, --mixed is default. can be skipped for default behavior
```sh 
  git reset --mixed HEAD~N
```
- deletes commit but changes are staged
```sh 
  git reset --soft HEAD~N
```
- deletes the local changes as well as the commit
```sh
  git reset --hard HEAD~N
```
- manipulate previous commits (sets the HEAD temporarily to the commit)
```sh 
  git rebase -i HEAD~N
```

- git rebasing follows commit order
- git squash (amend to a particular commit)

## **Class 3 - 03-11-2024 - GIT**

- Git rebase : merge commit by commit (unsquashed)
- Git squash before merge : conflicting commit unfoundable as all commits are squashed into single commit
- Rebase any branch with master : Git stashes & dumps commits one by one into master (a loop)
- Undo any git action
- git reflog (tracks all action)
- git co (short command for checkout) master
- git reset HEAD@{N}
- **git rebasing with reflog not clear**
- Forking (copy someone's code)
  - zip download
  - clone (includes the .git file)
  - fork (create a replica with my origin)
- git remote -v
- git remote add origin/jesse/rizwan
- git fetch jesse/master
- git checkout rizwan/master
- git rebase jesse/master
- git revert HEAD~N (delete the commit and add new commit)
- difference between reset & revert
