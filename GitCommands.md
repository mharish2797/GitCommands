#Git commands
##Frequently used commands
`git init`
`git add .`
`git status`
`git commit -m "msg"`
stage and commit a tracked file
`git commit -a -m "msg"`
`git diff`
`git diff --staged`
`touch <filename>`
`.gitignore`

##History
commit history
`git log`
commit hostory with respect to a file
`git log -- <filename>`
commit history graph 
`git log --all --decorate --oneline --graph`
(OR)
`alias graph = "git log --all --decorate --oneline --graph"`

##Reverting back
remove file in both working tree and staging area
`git rm <filename>`
revert a change to the working tree
`git checkout -- <filename>`
revert a change to the staging area
`git reset HEAD <filename>`
restore a file to working tree and staging area from a previous git version
`git checkout <first 5 characters of commit ID> -- <filename>`

##Branching
create branch
`git branch <branchname>`
list branch
`git branch`
work on a branch: HEAD->branchname
`git checkout <branchname>`
create and checkout branch
`git checkout -b <branchname>`

##Merging
Fast forward merge 
git merge <branchname>
3way merging with conflicts
git merge --abort

##Indicating what happens during merging
git diff master..<branchname>
##List merged branches
git branch --merged
##List local and remote repo
git branch -a
##List remote repo
git branch -r

##Deleting branches
git branch -d <branchname>

##Detached HEAD state
git checkout <first 5 characters of commit ID>

##Stashing
git stash
git stash save "message"
git stash list -p
git stash apply
git stash apply <stash labelname>
git stash pop

##Remote
for default remote name (origin)
git clone <URI>
git remote add <remote name> <URI>
git remote remove <remote name>

##default alias for the Github repo is 'origin'
git remote
git remote -v

##Fetch or track latest changes at remote
git fetch <remote name>

##merging origin/master to local
`git merge origin/master

##combining fetch and merge
`git pull

##pushing local to remote branch
`git push origin <remotebranchname>

Fork
Sync with remote repo
Issue Pull Request