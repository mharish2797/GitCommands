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

Commit history
`git log`
Commit history with respect to a file
`git log -- <filename>`
Commit history graph
`git log --all --decorate --oneline --graph`
`alias graph = "git log --all --decorate --oneline --graph"`

## Reverting back

Remove file in both working tree and staging area
`git rm <filename>`
Revert a change to the working tree
`git checkout -- <filename>`
Revert a change to the staging area
`git reset HEAD <filename>`
Restore a file to working tree and staging area from a previous git version
`git checkout <first 5 characters of commit ID> -- <filename>`

## Branching

Create branch
`git branch <branchname>`
List branch
`git branch`
Work on a branch: HEAD->branchname
`git checkout <branchname>`
create and checkout branch
`git checkout -b <branchname>`

## Merging

##### Types of Merging

1. Fast forward merge
2. 3-way merging with conflicts
3. 3-way merging without conflicts

`git merge <branchname>`
`git merge --abort`
Indicating what happens during merging
`git diff master..<branchname>`
List merged branches
`git branch --merged`
List local and remote repo
`git branch -a`
List remote repo
`git branch -r`

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

Fork
Sync with remote repo
Issue Pull Request
