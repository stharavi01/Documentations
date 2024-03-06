## Basics

### Create a new repository on the command line

git init
git add README.md
git commit -m "first commit"
git branch -M main    (M => move or rename branch name )
git remote add origin https://github.com/stharavi01/gitTutorial.git
git push -u origin main (u => set up tracking relationship between local main branch and remote main branch on the origin repository)


### Push an existing repository from the command line

git remote add origin https://github.com/stharavi01/gitTutorial.git
git branch -M main
git push -u origin main


### Clone a Repository

git clone <repository-url>


### Check Repository Status

git status


### Stage Changes

git add <file>


### Commit Changes

git commit -m "Your commit message"


### View Commit History

git log


## Branching

### Create a New Branch

git branch <branch-name>


### Switch to a Branch

git checkout <branch-name>


### Create and Switch to a New Branch

git checkout -b <new-branch-name>

### Merge Branches

git merge <branch-to-merge>


## Remote Repositories

### Pull Changes from a Remote Repository

git pull origin <branch-name>


### Push Changes to a Remote Repository

git push origin <branch-name>


### Fetch Changes from a Remote Repository (Without Merging)

git fetch origin


### View Remote Repositories

git remote -v


## Advanced Operations

### Remove a File from the Staging Area

git reset <file>


### Discard Changes in a File

git checkout -- <file>


### Resolve Merge Conflicts

git merge <branch-name>
# After resolving conflicts, use 'git add' and 'git merge --continue'


### Create a Tag for a Specific Commit

git tag <tag-name> <commit-hash>


### Show Differences Between Commits, Branches, or Files

git diff <source> <destination>


## Ignore Files

### Create a .gitignore File
Add filenames or patterns to exclude them from version control.

## Miscellaneous

### Show Help and List of Commands

git --help
