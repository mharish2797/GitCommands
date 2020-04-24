# Core Concepts
`
3 areas of Git -> Working tree, Staging area and commit graph.`

**git init** - Initializes a git repository in the current directory

**git config --[global/local] user.[name/email] ''name/email''** - configures git either for the entire system or for the particular directory.

**git status** - shows the status of files in the working tree.  

**git add [filename/.]** - moves the file / all contents from working tree to staging area.

**git commit -m "commit message"** - snapshots the contents in the staging area as a commit, which can be retrieved later using the hash it specifies.

**git diff [--staged]** - shows differences in the contents of the files in the staging area and those in the working area (or) staging area and most recent commit.

**git log [-p]** - Shows us the commit graph with/without the differences.

**git rm "file"** - removes file from both working tree and staging area.

**git checkout -- "file"** - restores file from staging area back into the working tree discarding the current changes made forever.

**git checkout "hash" --"file"** - recover file from the commit specified by the hash back into staging area and working tree.

**git reset HEAD "file"** - undo changes made to file in staging area (git add file). use git checkout to move that file from staging area to working tree.

**.gitignore** - add files/directories to this file that need not be tracked by Git. This file should be added.
