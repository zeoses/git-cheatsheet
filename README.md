# git-cheatsheet
Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.
## git useage
 * Code management
 * Fix code clutter
 * Distributed Development

## repository

a place ,or receptacle where things are or may be stored. in git contain a collection of files of various different versions of a Project.  
a best git repo includes files:
* LICENSE
* README.md

## README.md
This file has two mandatory sections and a optinal sections.
 * what is
 * how to work
 *  how to contribute to this project (optinal)

 ## git clone 
Clone a repository into a new directory
```
git clone  <remote address>
``` 
## how to update a local branch 
```
git pull
```
or
```
git fetch 
git rebase orgin <branch>
```
## DIFF checkout, revert, reset
### checkout
Switch branches or restore working tree files whitout changes.
```
git checkout <branch> or <commit>
```
### reset
Reset current HEAD to the specified state and remove commit after that and untracking file but if use ` --hard` remove all changes.
```
git reset <commit>
```
### revert
git to a commit whitout remove other commit
```
git revert <commit>
```
![image](statics/crr.png 'DIFF checkout, revert, reset ')

## merge vs rebase
Git rebase and merge both integrate changes from one branch into another. Where they differ is how it's done. Git rebase moves a feature branch into a master. Git merge adds a new commit, preserving the history.
### Benefits
Here are the top three benefits for Git rebase and for Git merge.

#### Git Rebase
* Streamlines a potentially complex history.
* Avoids merge commit “noise” in busy repos with busy branches.
* Cleans intermediate commits by making them a single commit, which can be helpful for DevOps teams.  
#### Git Merge
* Simple and familiar.
* Preserves complete history and chronological order.
* Maintains the context of the branch.


## history
```
git log # all history
git show HEAD~<commit number> # show log changes

```
## changes a file
```
git show <file name>
git deff <branch a> <branch b>
```

## tag
A Git tag is a reference to a specific commit within the history of a Git repository. In Git, tags are often used to mark releases.
```
git tag -a <tag> -m <commit>
git show <tag>
```
## contribute
### admin side:
the first step create an organization and after that and create a repo in this organization
### developer side:
fork the repo in git remote, clone your local repo, and add your code 
for merge in base repo must be created a merge request. 
## branch
A branch is simply a pointer to one of the commits in the repository. In the simplest case, there is the default branch called "master", and master points to the most recent commit. we used to branch for add and testing new features. 
```
# create
git branch <branchName>
# switching branches
git checkout <branchName>
# create and switch that
git checkout -b <branchName>
# merge : the first step switch to base branch
git merge <branch name> 
# or
git rebase <branch name> 

```

