# Git commands
## Frequently used commands
```git
git init
git add .
git status
git commit -m "msg"
```
Stage and commit a tracked file
```git
git commit -a -m "msg"
git diff
git diff --staged
touch <filename>
.gitignore
```
## History
Commit history <br>
`git log`<br>
Commit history with respect to a file<br>
`git log -- <filename>`<br>
Commit history graph <br>
```git
git log --all --decorate --oneline --graph
alias graph="git log --all --decorate --oneline --graph"
```
## Reverting back
Remove file in both working tree and staging area<br>
`git rm <filename>`<br>
Revert a change to the working tree<br>
`git checkout -- <filename>`<br>
Revert a change to the staging area<br>
`git reset HEAD <filename>`<br>
Restore a file to working tree and staging area from a previous git version<br>
`git checkout <first 5 characters of commit ID> -- <filename>`

## Branching
Create branch<br>
`git branch <branchname>`<br>
List branch<br>
`git branch`<br>
Work on a branch: HEAD->branchname<br>
`git checkout <branchname>`<br>
create and checkout branch<br>
`git checkout -b <branchname>`<br>

## Merging
##### Types of Merging
1. Fast forward merge
2. 3-way merging with conflicts
3. 3-way merging without conflicts

`git merge <branchname>`<br>
`git merge --abort`<br>
Indicating what happens during merging<br>
`git diff master..<branchname>`<br>
List merged branches<br>
`git branch --merged`<br>
List local and remote repo<br>
`git branch -a`<br>
List remote repo<br>
`git branch -r`<br>

## Deleting branches
`git branch -d <branchname>`

## Detached HEAD state
`git checkout <first 5 characters of commit ID>`

## Stashing
```git
git stash
git stash save "message"
git stash list -p
git stash apply
git stash apply <stash labelname>
git stash pop
```
## Remote
Default alias for the Github repo is 'origin'
```git
git clone <URI>
git remote add <remote name> <URI>
git remote remove <remote name>
git remote
git remote -v
```
##### Fetch or track latest changes at remote
`git fetch <remote name>`
##### Merging origin/master to local
`git merge origin/master`
##### Combining fetch and merge
`git pull`
##### Pushing local to remote branch
`git push origin <remotebranchname>`

Fork<br>
Sync with remote repo<br>
Issue Pull Request<br>
