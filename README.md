# GitCommands
A File containing a list of git commands
 Youtube (David Mahler) - https://www.youtube.com/watch?v=uR6G2v_WsRA

# Core Concepts
`
3 areas of Git -> Working tree, Staging area and commit graph.
`

**git init** - Initializes a git repository in the current directory.   
<br/>
**git config --[global/local] user.[name/email] ''name/email''** - configures git either for the entire system or for the particular directory.    
<br/>
**git status** - shows the status of files in the working tree.       
<br/>
**git add [filename/.]** - moves the file / all contents from working tree to staging area.      
<br/>
**git commit -m "commit message"** - snapshots the contents in the staging area as a commit, which can be retrieved later using the hash it specifies.      
<br/>
**git commit -a -m "msg"** - Performs both staging (git add ) and commits.   
<br/>
**git diff [--staged]** - shows differences in the contents of the files in the staging area and those in the working area (or) staging area and most recent commit.   
<br/>
**git log [-p]** - Shows us the commit graph with/without the differences.   
<br/>
**git rm "file"** - removes file from both working tree and staging area.     
<br/>
**git checkout -- "file"** - restores file from staging area back into the working tree discarding the current changes made forever.   
<br/>
**git checkout "hash" --"file"** - recover file from the commit specified by the hash back into staging area and working tree.    
<br/>
**git reset HEAD "file"** - undo changes made to file in staging area (git add file). use git checkout to move that file from staging area to working tree.   
<br/>
**.gitignore** - add files/directories to this file that need not be tracked by Git. This file should be added.   
<br/>
# Merging and Branching

## Branching. 

**git branch "name"** - Creates a new git branch with name.  
<br/>
**git checkout "name"** - Moves head to that branch.   
<br/>
**git branch -d "name"** - Deletes  git branch with name after successful merge.[-D forces delete].   
<br/>
## Merging
```Move to the master branch to merge with master using git checkout master```

**git merge "name"** - Creates a new git branch with name.  
<br/>
**git merge --abort** - aborts merge process when a conflict is present.   
<br/>
```
Fast forward merge - If there is a direct path between parent and the child branch.
Three-way merge - If there is no direct path, a merge commit is performed.
```
### Merge Conflicts
If changes are made in the same line of the code in different branches, conflict arises as to which changes are to be kept.

### Detached HEAD
If HEAD points to a commit instead of a branch, then we have a **Detached Head** state.
We can create a branch and attach it to the head by performing :
```
git branch "name"
git checkout "name"
```
### Stashing

When we try to move to a different branch with a dirty working tree, git blocks it with an error message.<br/>
**git stash** - saves these changes so that they can be recovered later.
						[list] shows all stashes.<br/>
						**git stash apply** - reapplies the most recent stash
				
						
# Git Remotes

## Remote
```
Ex- Our laptop can be remote with respect to GitHub. 
It can be anything with respect to our git repository.
```

**git clone "github url"** - From the perspective of our system, GitHub is now our remote repository.  We can push and fetch from and to our repo. Default alias for our remote repo is **origin** .<br/>

**git remote** - displays remotes . [-v] displays full locations.<br/>
**git log** now shows us our local master branch and also our origin/master and origin/HEAD. <br/>
Checking out to origin/master will result in a **detached Head** state.<br/>
**git status** fails to fetch the changes made in Github website. <br/>
To update changes made in UI, 
**git fetch origin ** -  updates origin locally with changes made in Github.
<br/>
**git pull**
```
Pull is a combination of both 'git fetch origin' and 'git merge origin/branch_name', but keeping them separate avoids unexpected merge results.
```
<br/>
When we are ahead of our remote github commits, we need to **push** our local changes to our repository.<br/>
**git push 'remote_branch_name' 'our_local_branch_name'**
Ex- git push origin master
<br/>
**git remote add "alias" "url"** - Adds a new remote with the alias specified. We can use this when we fork a Github project, then clone it to our local machine and push changes to either our repository in Github(the forked one) or the actual one using the aliases.



